Multithreading

Use the Thread Class to Demonstrate Multithreading
In this lab, you create a simple application that counts from 1 to 10 and shows each
iteration in the console window. If you encounter a problem completing an exercise,
the completed projects are available on the companion CD in the Code folder.
Exercise: Create Multiple Threads
In this exercise, you create a simple console application and start two threads simultaneously.
1. Create a new console application, and call it SimpleThreadingDemo.
2. Create a new static method called Counting.
3. In the new class, add a using statement (or the Imports statement for Visual
Basic) to the System.Threading namespace.
4. In the new method, create a for loop that counts from 1 to 10.
5. Within the new for loop, write out the current count and the ManagedThreadId
for the current thread.
6. After writing out to the console, sleep the current thread for 10 milliseconds.
7. Go back to the Main method, and create a new ThreadStart delegate that points
to the Counting method.
8. Now create two threads, each pointing to the Counting method.
9. Start both threads.
10. Join both threads to ensure that the application doesn’t complete until the
threads are done.
11. Build the project, and resolve any errors. Verify that the console application successfully
shows the threads running concurrently. You can determine this by
checking whether each thread’s counts are intermingled with those of other
threads. The exact nature of the intermingling is dependent on the type of hardware
you have. A single processor machine will be very ordered, but a multiprocessor
(or multicore) machine will be somewhat random.