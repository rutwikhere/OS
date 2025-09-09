OS Process Flow Simulator
An interactive, web-based simulator designed to visualize fundamental operating system concepts like process scheduling, CPU execution, interrupts, and memory management. This single-file application is built with vanilla JavaScript and styled with Tailwind CSS, making it lightweight and easy to run.

(You can replace the image link above with a screenshot of your running application)

✨ Features
Dynamic Process Creation: Add new processes with custom names and instructions on the fly.

Process State Visualization: Watch processes move through New, Ready, Running, Waiting, and Terminated states.

Round Robin CPU Scheduling: The CPU uses a time-slice-based Round Robin algorithm to ensure fairness.

Interrupt Simulation:

Timer Interrupts: Processes are preempted when their time slice expires.

I/O Interrupts: Processes that request I/O are moved to a waiting queue, freeing the CPU for other tasks.

Memory Management: A simple visual representation of primary memory (RAM) using a first-fit allocation algorithm.

Interactive Controls: Start, stop, reset, and control the speed of the simulation.

Detailed System Log: A real-time log that explains every action the simulated OS takes, from context switching to memory allocation.

🚀 How to Use
Open the Simulator: Simply open the os_simulator.html file in any modern web browser.

Add Processes:

Enter a Process Name (e.g., P1, WebTask).

Define its Instructions as a comma-separated list. The valid instructions are:

EXEC: A standard CPU task.

IO: An I/O request that will trigger an interrupt.

END: The final instruction to terminate the process.

Click "Add Process". The new process will be allocated in memory and placed in the Ready Queue.

Run the Simulation:

Click the "Start" button to begin the simulation.

Use the Speed slider to adjust the clock tick frequency.

Modify the Time Slice value to see how it affects the Round Robin scheduler.

Observe:

Watch the CPU block to see the currently running process.

Monitor the Ready and Waiting queues.

Observe the Primary Memory visualization to see how space is used.

Read the System Log for a detailed, step-by-step breakdown of all events.

🧠 OS Concepts Demonstrated
This simulator provides a visual learning tool for the following concepts:

Process Lifecycle: The complete journey of a process from creation to termination.

CPU Scheduling: Specifically, preemptive Round Robin scheduling. You can see how the scheduler selects the next process from the Ready Queue.

Context Switching: The log explicitly announces when the CPU stops one process and starts another.

Interrupts: The simulator clearly distinguishes between timer interrupts (time slice expired) and I/O interrupts (resource request).

Memory Allocation & De-allocation: See how the OS allocates a contiguous block of memory when a process is created and frees it upon termination.

Process Control Block (PCB): The "Process Control Blocks" table acts as a simplified representation of the PCBs, storing the state and program counter (PC) for each process.

🛠️ Technologies Used
HTML5

CSS3 with Tailwind CSS for styling.

Vanilla JavaScript (ES6+) for all the simulation logic.

📂 How to Run Locally
No complex setup required!

Clone the repository or download the os_simulator.html file.

Open the os_simulator.html file directly in your web browser (e.g., Chrome, Firefox, Edge).

💡 Future Improvements
Implement additional scheduling algorithms (e.g., FCFS, SJF, Priority).

Introduce a virtual memory system with paging.

Add support for multi-core CPUs.

Allow for dynamic process priority settings.
