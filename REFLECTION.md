# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer: I discovered that multithreading enables the simultaneous execution of several tasks within a single program. For this project, I simulated processes in a CPU scheduler using threads. I was aware that the Runnable interface is used to construct threads and that Thread.start() is used to start them. Additionally, I discovered how Thread.join() guarantees the correct scheduling order and how Thread.sleep() simulates execution time. One key idea I grasped is that threads are more efficient than processes since they share memory. In general, this task improved my comprehension of how threads behave in a scheduling system. **

[Write your answer here. Discuss specific concepts like thread creation, thread states, how threads execute concurrently, what surprised you, etc.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer: Implementing the waiting time feature was the most difficult aspect of this task. It involved keeping track of when each process joined the ready queue and figuring out how long it waited to be executed. It was first unclear where in the code the waiting time should be updated. I had to closely examine how processes enter and exit the queue as well as the scheduling loop. Making sure the calculation performed correctly over several execution cycles was another challenge. Debugging and logical reasoning were both needed for this section. **

[Describe the specific challenge. Was it understanding the code? Implementing a feature? Using Git? Explain what made it difficult and how it relates to the course concepts.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer: I overcome the difficulties by decomposing the issue into manageable chunks. Initially, I recognized where processes are added to the queue and comprehended how the scheduling loop operates. I then made advantage of System.I tracked time using currentTimeMillis() and thoroughly tested my code. In order to comprehend waiting time computation, I also went over course notes and examples. I was able to confirm that values were updating correctly by using debugging. I made sure the feature functioned as intended by testing various outputs.**

[Describe your problem-solving approach. Did you read documentation? Ask for help? Debug systematically? What resources did you use? What strategies worked?]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer: Real-world applications like mobile apps and web browsers frequently use multithreading. Web browsers, for instance, use threads to load several tabs at once without blocking the user interface. Similar to this, mobile apps employ threads to carry out background operations, such as data downloads, while maintaining a responsive user interface. Operating systems use threads to effectively plan numerous tasks. I gained a better understanding of how these systems handle several jobs at once thanks to this project. Additionally, it demonstrated how scheduling algorithms enhance fairness and performance.**

[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?
I want to know more about preventing race situations and thread synchronization. Additionally, I'm curious about how threads function in multi-core computers.
[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?
I consider myself to be in the middle. I still need more practice with more complex issues, but I understand the fundamentals of thread creation, scheduling, and execution.
[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment
Understanding practical multithreading principles was greatly aided by the assignment. It made the connection between theory and practice. The waiting time feature, however, was a little difficult and needed further clarification.
[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
