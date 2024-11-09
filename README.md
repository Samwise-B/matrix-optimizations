# GPU Programming and Cluster Computing

This project involved two main topics: **GPU Programming** using OpenMP for matrix computation tasks and **Cluster Computing** using MPI and other parallel computing techniques. Through the completion of these tasks, I gained hands-on experience with GPU programming, performance optimization, parallel computing, and managing computational resources on clusters. Below is a detailed overview of the project, showcasing my learning and problem-solving abilities.

## GPU Programming

### Overview
The objective of Task 1 was to parallelize a matrix computation algorithm using **OpenMP** and **GPU programming techniques**. This task involved porting an existing sequential program to utilize **OpenMP** directives for multi-threading and **GPU** computing for performance optimization.

### Key Steps and Concepts

1. **Time Measurement with OpenMP**:
   - Used OpenMP's time measurement routines to profile the execution time of different functions in the `magic_matrix.cpp` program. This profiling helped identify which functions were computational bottlenecks and would benefit most from parallelization.

2. **GPU Implementation**:
   - Ported the original CPU-based code to a **GPU implementation** using OpenMP and GPU-specific directives to achieve parallelization. The goal was to utilize the **GPU’s parallel architecture** to speed up the matrix computation, particularly for larger matrix sizes.
   - Focused on correctly managing parallel execution, ensuring the code remained thread-safe and maintained the correctness of results under concurrent execution.

3. **Code Optimization**:
   - Applied optimizations such as memory management techniques and the use of **shared memory** in GPU programming to minimize latency and maximize throughput.
   - Justified the use of specific OpenMP directives for parallelization and explained the changes made to the program structure for improved performance.

### Learnings
- **Parallel Programming**: I learned how to effectively use OpenMP for both CPU and GPU parallelization, balancing workload distribution across cores and handling synchronization between threads.
- **Optimization**: Through profiling and optimization, I improved the performance of the matrix computation algorithm, achieving significant speed-ups when moving from CPU to GPU.
- **Performance Comparison**: I learned how to analyze and compare the performance of parallel implementations with sequential code, highlighting the importance of selecting the right parallelization techniques for different hardware.

### Key Tools & Technologies
- **OpenMP**: Used for parallelization and performance optimization.
- **GPU Programming**: Utilized for leveraging parallel computing resources on the GPU for matrix computation.
- **Profiling and Optimization**: Time measurement techniques and memory management were key to optimizing code execution.

---

## Cluster Computing

### Overview
The second part of the project focused on parallelizing the `magic_matrix.cpp` program on a **cluster** using **MPI (Message Passing Interface)** and managing computational resources using **numactl** for data locality optimization.

### Key Steps and Concepts

1. **Cluster Execution with sbatch**:
   - Wrote a shell script (`run_all_magic_matrix.sh`) for parallel execution of the `magic_matrix.cpp` program across multiple compute nodes in the cluster.
   - Focused on managing parallel jobs and data distribution efficiently across nodes for different data sets.

2. **MPI Parallelization**:
   - In the report, I proposed an MPI-based parallelization strategy for the `magic_matrix.cpp` program. The strategy focused on distributing matrix computation tasks across multiple nodes, using MPI functions to handle communication and synchronization between the processes.
   - Designed a data distribution approach where each node computes a portion of the matrix, with MPI used to handle communication between these distributed tasks.

3. **Installing and Using numactl**:
   - Wrote a script (`install_numactl.sh`) to build and install **numactl** from source. This tool allows for analysis and optimization of data locality, which is crucial in high-performance computing tasks.
   - Documented the installation process and output from `numactl -H` to analyze memory architecture and data locality on the cluster.

4. **PVM Installation Strategy**:
   - In the final report, I proposed an approach for installing the `magic_matrix.cpp` program on a cluster's virtual machine (PVM). I discussed the advantages and disadvantages of different installation methods, emphasizing ease of access and maintenance for multiple users.

### Learnings
- **Cluster Computing with MPI**: I gained hands-on experience with parallel computing in a cluster environment, learning how to distribute tasks efficiently and handle communication between processes.
- **Data Locality Optimization**: Through the use of **numactl**, I learned how to optimize memory usage and ensure data locality on multi-node clusters to improve performance.
- **Resource Management**: The project helped me understand how to manage computational resources across clusters, ensuring that multiple tasks can run in parallel without conflicts or resource bottlenecks.

### Key Tools & Technologies
- **MPI**: Used for parallelizing tasks across a cluster, allowing for distributed computation.
- **numactl**: A tool used to analyze and manage data locality on multi-node systems.
- **sbatch**: A script used for submitting jobs to a cluster, ensuring that multiple tasks can be executed concurrently.

---

## Summary of Skills and Insights Gained

Through the project, I developed proficiency in the following areas:
- **GPU Programming and Parallelization**: I gained hands-on experience in parallel programming using OpenMP and optimized computation on GPUs. I successfully transitioned from a CPU-based program to one utilizing GPU resources, learning techniques to improve performance and scalability.
- **Cluster Computing with MPI**: I deepened my understanding of parallel programming across compute clusters, leveraging MPI for distributed computing. I also learned the importance of data locality and resource management in high-performance environments.
- **Performance Optimization**: By profiling the code and testing different parallelization strategies, I learned to identify bottlenecks and apply targeted optimizations for faster execution.
- **Linux/Cluster Management**: I improved my shell scripting skills, managing cluster jobs and installing software in a shared environment.

These tasks provided a strong foundation in parallel computing techniques, resource management, and performance optimization, all of which are crucial skills in modern computing environments.

---
**Keywords**: GPU Programming, OpenMP, MPI, Cluster Computing, Parallel Programming, Performance Optimization, Data Locality, Resource Management
