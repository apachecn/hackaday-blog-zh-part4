# 小心线程:并发 Python 介绍

> 原文：<https://hackaday.com/2018/12/18/thread-carefully-an-introduction-to-concurrent-python/>

在许多情况下，并行执行代码的能力至关重要。并发编程是 web 服务器、生产者/消费者模型、批量数据处理以及几乎任何应用程序被资源阻塞的时候的关键资产。

可悲的是，编写高质量的并发代码确实令人头疼，但本文旨在展示开始用 Python 编写线程程序是多么容易。由于标准库中有大量的模块可以帮助解决这类问题，所以通常情况下，简单的并发任务实现起来会非常快。

在回顾您可以采用的一些不同方法以及它们最适合的情况之前，我们将在 Python 环境中介绍线程和进程之间的区别。

( [Python 3 用于文章](https://hackaday.com/2018/08/15/stop-using-python-2-what-you-need-to-know-about-python-3/)的持续时间。)

# 全局解释器锁

谈到 Python 中的并发编程，不可能不提到全局解释器锁，或 GIL。这是因为它对您在编写异步 Python 时选择哪种方法有很大的影响。需要注意的最重要的一点是，它只是 CPython(广泛使用的“参考”Python 实现)的一个特性，而不是该语言的一个特性。在其他实现中，Jython 和 IronPython 没有 GIL。

GIL 是有争议的，因为它一次只允许一个线程访问 Python 解释器。这意味着线程通常不可能利用多核系统。请注意，如果 Python 之外发生了阻塞操作，例如 I/O 等长时间等待的任务，那么 GIL 就不是瓶颈，编写线程化的程序仍然会有好处。然而，如果阻塞操作大量处理 CPython 字节码，那么 GIL 就会成为瓶颈。

为什么要引进 GIL 呢？它使内存管理更加简单，没有同时访问或竞争的可能性，并且使 C 扩展更容易编写和包装。

所有这一切的结果是，如果您需要真正的并行性，需要利用多核 CPU，线程不会削减它，您需要使用进程。一个独立的进程意味着一个独立的解释器，它有独立的内存、自己的 GIL 和真正的并行性。本指南将给出线程和进程架构的例子。

# concurrent.futures 模块

在 Python 中,`concurrent.futures`模块是一个保守得很好的秘密，但是它提供了一种实现线程和进程的非常简单的方法。对于许多基本应用程序，这里提供的易于使用的`Pool`接口就足够了。

这里有一个例子，我们想下载一些网页，如果并行完成，会快得多。

```

'''Download webpages in threads'''
import requests
from concurrent.futures import ThreadPoolExecutor

download_list = [
    {'name': 'google', 'url': 'http://google.com'},
    {'name': 'reddit', 'url': 'http://reddit.com'},
    {'name': 'ebay', 'url': 'http://ebay.com'},
    {'name': 'bbc', 'url': 'http://bbc.co.uk'}
]

def download_page(page_info):
    '''Download and save webpage'''
    r = requests.get(page_info['url'])
    with open(page_info['name'] + '.html', 'w') as save_file:
        save_file.write(r.text)

if __name__ == '__main__':
    pool = ThreadPoolExecutor(max_workers=10)

    for download in download_list:
        pool.submit(download_page, download)

```

大部分代码只是设置我们的下载器示例；它只是包含线程特定代码的最后一个块。注意使用`ThreadPoolExecutor`创建一个动态的工人池并提交一个任务是多么容易。我们甚至可以使用`map`将最后两行简化为一行:

```

    pool.map(download_page, download_list)

```

在这种情况下使用线程效果很好，因为受益于并发性的阻塞操作是获取网页的动作。这意味着 GIL 不是问题，线程是理想的解决方案。但是，如果所讨论的操作在 Python 中是 CPU 密集型的，那么由于 GIL 的限制，processes 可能更合适。在这种情况下，我们可以简单地用`ProcessPoolExecutor`替换掉`ThreadPoolExecutor`。

# 线程模块

虽然`concurrent.futures`模块提供了一种快速起步的好方法，但有时需要对不同的线程进行更多的控制，这就是无处不在的`threading`模块的用武之地。

让我们重新实现上面制作的网站下载器，这次使用的是`threading`模块。

```

'''Download webpages in threads, using `threading`.'''
import requests
import time
import threading

download_list = [
    {'name': 'google', 'url': 'http://google.com'},
    {'name': 'reddit', 'url': 'http://reddit.com'},
    {'name': 'ebay', 'url': 'http://ebay.com'},
    {'name': 'bbc', 'url': 'http://bbc.co.uk'}
]

def status_update():
    '''Print 'Still downloading' at regular intervals.'''
    while True:
        print('Still downloading')
        time.sleep(0.1)

def download_page(page_info):
    '''Download and save webpage.'''
    r = requests.get(page_info['url'])
    with open(page_info['name'] + '.html', 'w') as save_file:
        save_file.write(r.text)

if __name__ == '__main__':
    for download in download_list:
        downloader = threading.Thread(target=download_page, args=(download,))
        downloader.start()

    status = threading.Thread(target=status_update)
    status.start()

```

对于我们想要创建的每个线程，我们创建一个`threading.Thread`类的实例，指定我们希望我们的工人函数是什么，以及所需的参数。

请注意，我们还添加了一个状态更新线程。这样做的目的是重复打印“仍在下载”,直到我们获取完所有的网页。不幸的是，由于 Python 在退出前会等待所有线程执行完毕，所以程序永远不会退出，状态更新线程也永远不会停止打印。

这是一个说明`threading`模块的众多选项何时有用的例子:我们可以将更新线程标记为守护线程，这意味着当*只剩下守护线程*运行时，Python 将退出。

```

    status = threading.Thread(target=status_update)
    status.daemon = True
    status.start()

```

程序现在成功地停止打印，并在所有下载线程完成时退出。

守护进程线程通常对后台任务和重复功能最有用，这些任务和功能只有在主程序运行时才需要，因为守护进程可能随时被终止，从而导致数据丢失。

# 线程和队列的结合

到目前为止，我们只研究了当我们启动线程时，我们确切地知道我们希望线程在做什么的情况。然而，通常情况下，我们需要启动一组工作线程，然后在它们到达时向它们提供任务。

处理这些任务的最佳数据结构当然是队列，Python 提供了一个专门面向线程应用的[队列模块](https://docs.python.org/3/library/queue.html)。FIFO、LIFO 和优先级队列可用。

使用一个`queue.Queue`对象来添加、获取和标记任务，就像下面这样简单:

```

from queue import Queue

# maxsize=0 means infinite size limit
tasks = Queue(maxsize=0)

tasks.put('a task')
tasks.put('another task')

while not tasks.empty():
    print(tasks.get())
    # execute task
    tasks.task_done()

```

好了，这是最基本的。现在让我们用它来为我们的网站下载器创建一个任务队列。我们将创建一组工作线程，它们都可以访问队列并等待任务进入。

```

'''Download webpages in threads, using `threading` and `queue`.'''
import requests
import threading
from queue import Queue

NUM_WORKER_THREADS = 3

def download_page(page_info):
    '''Download and save webpage.'''
    r = requests.get(page_info['url'])
    with open(page_info['name'] + '.html', 'w') as save_file:
        save_file.write(r.text)

def handle_tasks(tasks_queue):
    '''Monitor tasks queue and execute tasks as appropriate.'''
    while True:
        download_page(tasks_queue.get())
        tasks_queue.task_done()

if __name__ == '__main__':
    tasks = Queue(maxsize=0)

    # Create and start worker threads
    for i in range(NUM_WORKER_THREADS):
        worker = threading.Thread(target=handle_tasks, args=(tasks,))
        worker.daemon = True
        worker.start()

    # Add some tasks to the queue
    tasks.put({'name': 'google', 'url': 'http://google.com'})
    tasks.put({'name': 'reddit', 'url': 'http://reddit.com'})
    tasks.put({'name': 'ebay', 'url': 'http://ebay.com'})
    tasks.put({'name': 'bbc', 'url': 'http://bbc.co.uk'})

    tasks.join()

```

注意，在这个例子中，为了简洁起见，所有的任务都是一次性添加的，但是在一个实际的应用程序中，任务可以以任何速度缓慢加入。这里，当任务队列完全完成时，我们使用`.join()`方法退出程序。

# 多重处理模块

对于线程的详细控制来说,`threading`模块很棒，但是如果我们想要对进程进行更精细的控制呢？你可能会认为这更具挑战性，因为一旦进程启动，它就完全分离和独立——比留在当前解释器和内存空间中的新线程更难控制。

幸运的是，Python 开发人员努力创建了一个`multiprocessing`模块，它的接口几乎与`threading`模块相同。这意味着启动流程遵循与上述示例完全相同的语法。我们简单的下载器会变成这样:

```

'''Download webpages in threads, using `multiprocessing`.'''
import requests
import time
import multiprocessing

download_list = [
    {'name': 'google', 'url': 'http://google.com'},
    {'name': 'reddit', 'url': 'http://reddit.com'},
    {'name': 'ebay', 'url': 'http://ebay.com'},
    {'name': 'bbc', 'url': 'http://bbc.co.uk'}
]

def status_update():
    '''Print 'Still downloading' at regular intervals.'''
    while True:
        print('Still downloading')
        time.sleep(0.1)

def download_page(page_info):
    '''Download and save webpage.'''
    r = requests.get(page_info['url'])
    with open(page_info['name'] + '.html', 'w') as save_file:
        save_file.write(r.text)

if __name__ == '__main__':
    for download in download_list:
        downloader = multiprocessing.Process(target=download_page,
                                             args=(download,))
        downloader.start()

    status = multiprocessing.Process(target=status_update)
    status.daemon = True
    status.start()

```

我们认为 Python 能够在`threading`和`multiprocessing`模块之间保持相同的语法是很棒的，而实际发生的行为是如此的不同。

当涉及到在进程间分配数据时，我们用于线程化的`queue.Queue`将不能在进程间工作。这是因为`queue.Queue`基本上只是当前流程中的一个数据结构——尽管它被巧妙地锁定和互斥。幸好有一个`multiprocessing.Queue`，它是[专门为进程间通信](https://docs.python.org/3.4/library/multiprocessing.html#multiprocessing.Queue)设计的。在幕后，这将序列化您的数据，并通过进程间的管道发送它——这是一个非常方便的抽象。

# 摘要

用 Python 编写并发代码会很有趣，因为内置的语言特性可以抽象出很多问题。这并不意味着无法实现详细的控制水平，而是降低了从简单任务开始的障碍。因此，当你在开始下一个过程之前一直在等待一个过程结束时，试试这些技巧中的一个。