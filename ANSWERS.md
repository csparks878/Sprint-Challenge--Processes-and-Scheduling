1. List all of the main states a process may be in at any point in time on a
   standard Unix system. Briefly explain what each of these states mean.
   I belive they are:
   Waiting: Waiting to be executed in a queue
   Running: Currently being executed by the CPU
   Terminated: Done running and has issued an exit command to it's parent queue.

2. What is a Zombie Process? How does it get created? How does it get destroyed?
    A Zombie Process is when a process has finished its action on the CPU, but has not yet been terminated/dequed. The process is 100% finished once it sends the exit command to the parent, but as long as that hasn't happened, it's a zombie.

3. Describe the job of the Scheduler in the OS in general.
    As I understand it, the OS Scheduler really functions to manage all of the different processes that are vying for the attention of the CPU. It does this by assigning priority to certain processes over others and dividing them into multiple different queues.

4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.
    A traditional Round Robin shares the CPU execution with all processes immediately; however, it does nothing to check or assign priority. The MLFQ does have a system of assigning priority, AND it makes use of the Round Robin in particular circumstances (i.e. when two processes come up that are of equal priority.);