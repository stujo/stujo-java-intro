# Multiple Threads

* Where possible simplify your life by using your custom objects on single threads, otherwise:
* [Concurrency](http://docs.oracle.com/javase/tutorial/essential/concurrency/)
* ``synchronized`` - Ensure only a single thread is active at a given time
* ``notify`` and ``wait``
* When threads are holding the object's monitor (Inside a ``synchronized`` block)...
* [Example](http://www.journaldev.com/1037/java-thread-wait-notify-and-notifyall-example)
* [wait() and notify()](http://stackoverflow.com/questions/2536692/a-simple-scenario-using-wait-and-notify-in-java#2537117)


