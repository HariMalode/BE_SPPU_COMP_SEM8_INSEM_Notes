### Q1. Explain different characteristics of tasks. [4]

### **Tasks in Parallel Computing**  

#### **Definition:**  
- A task is a small unit of work or computation that is part of a larger process.
- Tasks are used in parallel computing, operating Systems & distributed systems to break down complex problems into smaller, manageable parts.
- Fox eg, in a parallel program, sorting a large dataset can be divided into multiple tasks, where each task sorts small portion of data.

### **Characteristics of Tasks**  

Tasks in parallel computing have several key characteristics that determine how they interact, execute, and contribute to overall performance.  

#### **1. Granularity**  
- **Definition:** The size of a task in terms of computation time and complexity.  
- **Types:**  
  - **Fine-Grained Tasks** – Small tasks that require frequent communication.  
  - **Coarse-Grained Tasks** – Large tasks with minimal communication overhead.  

#### **2. Dependency**  
- **Definition:** Some tasks may depend on the output of others before they can execute.  
- **Types:**  
  - **Independent Tasks** – Can execute in parallel without waiting for other tasks.  
  - **Dependent Tasks** – Require synchronization due to data dependencies.  
- • Foreg, In image processing, filtering can be done independently, but encoding requires previous steps.

#### **3. Synchronization**  
- **Definition:** The coordination between tasks to ensure correct execution.  
- **Types:**  
  - **Synchronous Execution** – Tasks must communicate and wait for each other (e.g., barrier synchronization).  
  - **Asynchronous Execution** – Tasks run independently without waiting for others.  

#### **4. Load Balancing**  
- **Definition:** The even distribution of tasks among processors to prevent idle time.  
- **Types:**  
  - **Static Load Balancing** – Tasks are assigned before execution begins (fixed workload distribution).  
  - **Dynamic Load Balancing** – Tasks are assigned at runtime based on processor availability.  

#### **6. Scalability**  
- **Definition:** The ability of a parallel system to handle increased workload efficiently as the number of processors grows.  


### **Conclusion**  
Tasks are essential components of **parallel computing**, and their characteristics directly influence **performance, efficiency, and scalability**. Efficient **task management, synchronization, and scheduling** are crucial for achieving **high-performance parallel processing**. 🚀

### Q2. Explain process. Diff between process and tasks

- A process is a Xunning on a program that is currently computer.
- It includes progiam code, data & resources needed for execution.


### **Task vs Process**

| **Task** | **Process** |
|-----------|------------|
| **i)** A task is a small unit of work within a process. | **i)** A process is a running program that consists of multiple tasks. |
| **ii)** It can be independent or dependent on other tasks. | **ii)** It runs independently but can communicate with other processes. |
| **iii)** It is smaller and lighter compared to a process. | **iii)** It is larger as it includes program code and memory. |
| **iv)** It can run as a part of a process or in parallel with other tasks. | **iv)** It runs separately and can create multiple tasks/threads. |
| **v)** It uses fewer resources as it is a part of a process. | **v)** It uses more system resources like CPU & memory. |
| **vi)** **Example:** Sorting a part of a dataset in parallel computing. | **vi)** **Example:** Running a web browser. |

---

### Q3. Explain any three decomposition technique with example? [6]

### **Decomposition Techniques**  
Decomposition is the process of breaking a large computational problem into smaller tasks that can be executed concurrently to achieve parallelism. This helps in improving efficiency, scalability, and performance in parallel computing.  

### **Types of Decomposition Techniques**  

1. **Data Decomposition**  
   - The problem is divided based on the data, and each processor handles a portion of the data independently.  
   - **Example:** Matrix multiplication, where each processor handles a subset of matrix rows.  

2. **Task Decomposition**  
   - The problem is divided into different tasks, and each task is assigned to different processors.  
   - **Example:** A compiler with different stages like lexical analysis, parsing, and code generation, each handled by different processors.  

3. **Recursive Decomposition**  
   - In recursive decomposition, the problem is repeatedly divided into smaller subproblems until they become small enough to be processed by individual processors.  
   - **Example:** Merge Sort, where the array is recursively divided and sorted in parallel.  

4. **Geometric Decomposition**  
   - The problem is divided based on the geometric structure of the data, where each processor handles a specific region.  
   - **Example:** Weather simulation, where different regions of the atmosphere are processed separately.  

5. **Hybrid Decomposition**  
   - A combination of multiple decomposition techniques (such as data and task decomposition) to optimize parallel performance.  
   - **Example:** In large-scale scientific simulations, data decomposition is used for spatial distribution, and task decomposition is used for handling different simulation processes.  

---

### Q4. What are the characteristics of Inter-Task Interactions? [4]
### **Inter-Task Interactions**  
Inter-task interactions refer to the communication and dependencies between different tasks in a parallel computing environment. Since tasks often need to share data or synchronize their operations, understanding their interactions is crucial for efficient parallel execution.  

### **Characteristics of Inter-Task Interactions**  

1. **Dependency**  
   - Some tasks depend on the output of other tasks, requiring proper synchronization and data exchange.  
   - **Example:** In numerical simulations, later computations may rely on previous results.  

2. **Synchronization**  
   - Tasks must coordinate their execution to ensure correct results, often using mechanisms like barriers, locks, or semaphores.  
   - **Example:** In parallel sorting, tasks synchronizing after each merge step.  

3. **Communication Overhead**  
   - Data exchange between tasks introduces latency, which can affect performance. Efficient communication mechanisms help minimize this overhead.  
   - **Example:** Message passing in distributed computing systems.  

4. **Granularity**  
   - Defines the level of interaction between tasks—coarse-grained tasks have minimal communication, while fine-grained tasks require frequent interactions.  
   - **Example:** GPU computations often use fine-grained parallelism.  

5. **Load Balancing**  
   - Proper distribution of work among tasks ensures efficient utilization of resources, preventing bottlenecks.  
   - **Example:** Dynamic task scheduling in parallel applications.  

6. **Scalability**  
   - Efficient inter-task interaction ensures that adding more processors improves performance rather than increasing communication costs.  
   - **Example:** Cloud-based parallel computing frameworks like MPI or Hadoop.  

----

### Q5.  What are mapping techniques for load balancing? Explain at least two mapping techniques. [5]

### **Mapping Techniques for Load Balancing**  
- In parallel computing, load balancing ensures that computational work is distributed evenly across multiple processors or machines.
- This prevents some processors from being overloaded while others remain idle, improving efficiency & performance .

### **Types of Mapping Techniques:**  

#### **1. Static Mapping**  
- In static mapping, tasks are assigned to processors before execution begins, and the assignment remains fixed throughout.  
- This approach works well when the workload is predictable and does not change over time.  

🔹 **Example:**  
   - In matrix multiplication, where the workload is evenly distributed among processors.  
   - A 4x4 matrix can be divided into four equal 2x2 blocks, each assigned to a processor.  

🔹 **Advantages:**  
   - Low overhead since task allocation is precomputed.  
   - Works efficiently when task execution times are known in advance.  

🔹 **Disadvantages:**  
   - Not suitable for dynamic workloads where task execution times vary.  
   - If one processor finishes early, it remains idle while others are still working.  

---

#### **2. Dynamic Mapping**  
- In dynamic mapping, tasks are assigned to processors during execution based on current load conditions.  
- It is useful when workloads are unpredictable or vary over time.  

🔹 **Example:**  
   - In web servers handling HTTP requests, requests are dynamically distributed to available servers based on current traffic load.  

🔹 **Advantages:**  
   - Efficient for uneven workloads where task execution times are not known beforehand.  
   - Ensures better resource utilization by balancing the load dynamically.  

🔹 **Disadvantages:**  
   - Higher overhead due to real-time decision-making and task migration.  
   - More complex implementation compared to static mapping.  

---

### Q6. Explain classification of Dynamic mapping techniques. [5]

### **Classification of Dynamic Mapping Techniques**  

- Dynamic mapping techniques assign tasks to processors at runtime based on workload conditions.
- This helps balance the load efficiently, especially when workloads time
- They help achieve better load balancing, resource utilization, and system performance. These techniques can be classified into the following categories:

---

### **1. Centralized Dynamic Mapping**  
- A central scheduler is responsible for distributing tasks among all processors.  
- It collects information about system load and assigns tasks accordingly.
- When a processor finishes a task, it informs the scheduler, which then assigns new tasks.
- Efficient task distribution when the number of processors is small
- Not scalable for large distributed systems.

### **2. Distributed Dynamic Mapping**  
- Each processor makes its own scheduling decisions without relying on a central scheduler.  
- Processors exchange workload information between each other to balance the load.
- Each processor decides when to migrate tasks based on its own load.
- Suitable for large-scale distributed systems.
- Requires communication between processors, increasing overhead.

### **3. Sender-Initiated Mapping**  
- A heavily loaded processor (sender) actively sends tasks to underutilized processors.  
- Task migration is initiated when the sender detects an overload condition.  

### **4. Receiver-Initiated Mapping**  
- An underloaded processor (receiver) requests tasks from overloaded processors.  
- It actively searches for tasks to execute when idle.  

### **5. Hybrid Mapping**  
- Combines both sender-initiated and receiver-initiated strategies.  
- Load balancing decisions are made based on system state and workload patterns.  

----

### Q7. Explain the different methods for Containing Interaction Overheads. [5]
### **Methods for Containing Interaction Overheads**  

- Interaction overheads in parallel computing arise due to communication, synchronization, and data dependencies among tasks.
- These overheads can significantly impact performance.
- To optimize parallel execution, various methods are used to minimize these overheads.  

### **1. Minimizing Communication Overhead**  
- **Definition:** Reducing the time spent in data transfer between processors.  
- **Methods:**  
  - **Message Aggregation:** Combining multiple small messages into a single larger message to reduce communication frequency.  

### **2. Reducing Synchronization Overhead**  
- **Definition:** Decreasing delays caused by waiting for other tasks to complete.  
- **Methods:**  
  - **Reducing Critical Sections:** Keeping shared resource access minimal to avoid contention.  
  - **Asynchronous Execution:** Using non-blocking synchronization techniques to allow some tasks to progress while waiting for others.  

### **3. Load Balancing Techniques**  
- **Definition:** Distributing work evenly among processors to avoid idle time and bottlenecks.  
- **Methods:**  
  - **Static Load Balancing:** Assigning tasks at the beginning based on workload predictions.  
  - **Dynamic Load Balancing:** Adjusting task assignments at runtime to accommodate variations in execution time.  

### **4. Optimizing Data Locality**  
- **Definition:** Ensuring that data is accessed from nearby memory locations to reduce access time.  
- **Methods:**  
  - **Cache Optimization:** Arranging data to improve cache utilization.  
  - **Minimizing Remote Memory Access:** Using techniques like NUMA-aware scheduling to keep tasks and data close together.  

### **5. Reducing Redundant Computations**  
- **Definition:** Avoiding unnecessary calculations that lead to increased execution time and resource usage.  
🔹 **Example:**  
   - In numerical simulations, reusing previously computed results instead of recalculating matrix elements multiple times.  

---

### Q8. Explain in details parallel algorithm models with suitable examples? [6]

### **Parallel Algorithm Models**  
Parallel algorithm models define the **structure and organization** of tasks to efficiently execute computations on parallel systems. These models help in dividing, distributing, and synchronizing tasks among multiple processors to maximize performance and minimize execution time.  

### **Types of Parallel Algorithm Models**  

### **1. Data Parallel Model**  
- This model divides the **data set into smaller parts** and assigns each part to different processors.  
- All processors perform **the same operation** on different parts of the data simultaneously.  

#### **Example:**  
- Matrix Multiplication: Each processor computes the multiplication of a specific row of matrix A with matrix B.  

### **2. Task Parallel Model**  
- This model divides the problem into **independent tasks** that can run in parallel.  
- Each processor executes **different tasks** at the same time.  

#### **Example:**  
- Image processing: One processor applies filters, another resizes the image, and another adjusts brightness.  

### **3. Pipeline Model**  
- The problem is divided into **a sequence of stages**, where each stage performs part of the computation.  
- The output of one stage is passed as input to the next stage.  

### **4. Divide and Conquer Model**  
- The problem is recursively divided into **smaller subproblems**, solved independently, and combined for the final result.  

#### **Example:**  
- Merge Sort:  
  
### **5. Hybrid Model**  
- This model combines **two or more algorithm models** to improve performance and flexibility.  

#### **Example:**  
- Weather Simulation:  
  - Data decomposition to divide the geographical region  
  - Task decomposition to model wind speed, temperature, and humidity separately  

---

### Q9. Draw the task-dependency graph for finding the minimum number in the sequence {4, 9, 1, 7, 8, 11, 2, 12} where each node in the tree represents the task of finding the minimum of a pair of numbers. Compare this with serial version of finding minimum number from an array. [5]


### **Step 1: Task Dependency Graph (Parallel Approach)**
In the **parallel approach**, we compare elements in pairs simultaneously and reduce the number of comparisons in each step.

1. **Level 1:** Compare adjacent pairs:  
   - `(4,9) → 4`  
   - `(1,7) → 1`  
   - `(8,11) → 8`  
   - `(2,12) → 2`

2. **Level 2:** Compare the results from Level 1:  
   - `(4,1) → 1`  
   - `(8,2) → 2`

3. **Level 3:** Final comparison to find the minimum:  
   - `(1,2) → 1`

```
          (1)
         /   \
       (1)   (2)
      /  \   /  \
    (4)  (1)(8) (2)
   /  \  /  \ /  \ /  \
  (4) (9)(1)(7)(8)(11)(2)(12)
```
- The **height of the tree** is **log₂N**, making the time complexity **O(log N)**.

---

### **Step 2: Serial Approach**
In a **serial approach**, we iterate through the array **sequentially** and compare each element.

1. Initialize `min = 4`
2. Compare with `9` → `min = 4`
3. Compare with `1` → `min = 1`
4. Compare with `7` → `min = 1`
5. Compare with `8` → `min = 1`
6. Compare with `11` → `min = 1`
7. Compare with `2` → `min = 1`
8. Compare with `12` → `min = 1`

- **Total comparisons** = `N - 1 = 7`
- **Time Complexity** = **O(N)**

---

### **Comparison: Parallel vs. Serial Approach**
| Approach | Number of Comparisons | Time Complexity | Speed |
|----------|----------------------|----------------|--------|
| **Serial** | `N - 1 = 7` | **O(N)** | Slower |
| **Parallel** | `N - 1 = 7`, but in parallel **O(log N) levels** | **O(log N)** | Faster |

### **Conclusion**
- The **parallel approach** significantly reduces **execution time** as multiple comparisons happen simultaneously.  
- The **serial approach** takes **linear time (O(N))**, while the **parallel approach** takes **logarithmic time (O(log N))**, making it much more efficient for large datasets.

Would you like me to generate a proper visual diagram for the task-dependency graph? 😊