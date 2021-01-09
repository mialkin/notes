# Concurrency

**Concurrency** is doing more than one thing at a time.<sup>1</sup>

There are several kinds of concurrency:

* parallel
* asynchronous
* reactive
* dataflow

## Mutlithreading

**Multithreading** is a form of concurrency that uses multiple threads of execution.

> Multithreading refers to literally using multiple threads. As demonstrated in many recipes in this book, multithreading is *one* form of concurrency, but certainly not the only one. In fact, direct use of low-level threading types has almost no purpose in a modern application; higher-level abstractions are more powerful and more efficient than old-school multithreading. For that reason, I’ll minimize my coverage of outdated
techniques. None of the multithreading recipes in this book use the
`Thread` or `BackgroundWorker` types; they have been replaced with superior alternatives.<sup>2</sup>

> **WARNING:** As soon as you type `new Thread()`, it’s over; your project already has legacy code.<sup>3</sup>

> But don’t get the idea that multithreading is dead! Multithreading lives on in the *thread pool*, a useful place to queue work that automatically adjusts itself according to demand. In turn, the thread pool enables another important form of concurrency: *parallel processing*.<sup>4</sup>

### Parallel processing

**Parallel processing** or **parallel programming** is doing lots of work by dividing it up among multiple threads that run concurrently.

Parallel processing uses multithreading to maximize the use of multiple processor cores. Parallel processing splits the work among multiple threads, which can each run independently on a different core.

Parallel processing is one type of multithreading, and multithreading is one type of concurrency.

## Asynchronous programming

**Asynchronous programming** is a form of concurrency that uses *futures* or callbacks to avoid unnecessary threads.

A **future** (or **promise**) is a type that represents some operation that will complete in the future.

Some modern future types in .NET are `Task` and `Task<TResult>`
. Older asynchronous APIs use callbacks or events instead of futures.

**Asynchronous operation** is some operation that is started that will complete some time later. While the operation is in progress, it doesn’t block the original thread; the thread that starts the operation is free to do other work.

## Reactive programming

Another form of concurrency is *reactive programming*. Asynchronous programming implies that the application will start an operation that will complete once at a later time. Reactive programming is closely related to asynchronous programming but is built on *asynchronous events* instead of *asynchronous operations*. Asynchronous events may not have an actual “start,” may happen at any time, and may be raised multiple times. One example is user input.

**Reactive programming** is a declarative style of programming where the application reacts to events.

> Reactive programming isn’t necessarily concurrent, but it is closely related to concurrency, so this book covers the basics.<sup>5</sup>

Usually, a mixture of techniques is used when writing a concurrent program. Most applications at least use multithreading (via the thread pool) and asynchronous programming.

<hr>

<sup>1,2,3,4,5</sup> Stephen Cleary, Concurrency in C# Cookbook: Asynchronous, Parallel, and Multithreaded Programming, Second edition (O’Reilly Media, 2019).