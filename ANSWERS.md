# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer: A thread is a small unit of execution inside a process that shares memory and resources with other threads, whereas a process is an independent program in operation with its own memory and resources. Because they share memory, threads are quicker and more effective than processes, which are more costly to generate and maintain. Because the simulation calls for quick task switching without significant overhead, threads were employed in place of processes in this assignment. The Round-Robin scheduling simulation is compatible with the use of threads since they facilitate quicker execution and simpler communication. Additionally, because every process uses the same environment, threads make the architecture simpler.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:In Round-Robin scheduling, if a process does not finish within its time quantum, it is paused and moved back to the end of the ready queue. This ensures fairness by giving all processes equal CPU time.

Example from my output: 
⏸ P1 completed quantum 3000ms │ Overall progress: 41%
Remaining time: 4160ms
↻ P1 yields CPU for context switch

➕ P1 (Priority: 2) added to ready queue │ Burst time: 7160ms **

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. New: P1 is in the New state when the thread object is first created using new Thread(process) before calling start(). At this point, it has not yet begun execution.

2. Runnable: After calling currentThread.start(), P1 enters the Runnable state. In this state, it is ready to be scheduled by the CPU but may not be executing yet.

3. Running: P1 enters the Running state when the scheduler selects it and starts executing its run() method, as shown in the output:
▶ P1 executing quantum [3000ms]

4. Waiting: P1 enters the Waiting state when Thread.sleep() is called inside the run() method to simulate execution time. During this period, the thread is paused and not using CPU.

5. Terminated: P1 enters the Terminated state after completing all its execution when its remaining time becomes zero, as shown in the output:
✓ P1 finished execution!

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Server

**Description**: A web server handles multiple client requests simultaneously, where each request can be processed as a separate thread.


**Why Round-Robin works well here**: 
Round-Robin ensures fairness by giving each request a small time slice, preventing one request from blocking others. It improves responsiveness and ensures all clients are served efficiently.

### Example 2: Operating System Task Scheduling

**Description**: 
An operating system schedules multiple user processes and background tasks using threads

**Why Round-Robin works well here**: 
Round-Robin provides equal CPU time for all processes, ensuring fairness and avoiding starvation. It also improves system responsiveness, especially in time-sharing systems.

---

## Summary

**Key concepts I understood through these questions:
1. Difference between threads and processes
2. How Round-Robin scheduling works
3. Thread lifecycle and execution flow

**Concepts I need to study more:
1. Advanced thread synchronization
2. Multi-core parallel execution
