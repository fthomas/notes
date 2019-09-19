https://www.youtube.com/watch?v=x5_MmZVLiSM

## Chapter 1:

Async process: process that continues execution in different place or time than the one it startd in
* Async boundary: resuming somewhere else. An async process has an async boundary.

Concurrency: multiple logical threads, whose effects are interleaved

Logical thread: seq of discrete steps

Scheduling: interleaving the steps of multiple logical threads
* M:N Threading is scheduling (M > N)
* multiple towers of logical threads

Threads are abstractions
* logical threads offer synchronous interface to async process
* sync steps at higher level are async at lower level after scheduling

Blocking
* blocking at one level means suspending at the level below. blocking -> async boundary at level below

## Chapter 2:

Concurrency: interleaving discrete steps
Parallelism: discrete steps running simultaneously

Layers:
* OS processes
* OS/JVM threads
* Fibers

JVM threads are a scarce resource
Fibers aren't scarce
Blocking a Fiber doesn't block the underlying thread, it just suspends the step on the thread -> that is semantic blocking

Scheduling
* preemptive: scheduler suspends tasks (preemption: Bevorrechtigung)
* cooperative: tasks suspend themselves

M:N cooperative scheduling = Fibers

## Chapter 3:

IO API
* FFI: wraps side-effects
* combinators: compose IO values
* Runners

Runloop
* recursive functions that executes instructions one at a time
* keeps track of current IO and stack of binds

* error handler drops binds that do not handle the current error

## Chapter 4:

* async function does not introduce asynchrony but wraps an already async process
* ( A => Unit) => Unit: callback with a continuation

## Chapter 5:



