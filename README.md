
# 🔒Simulating and Analyzing Deadlock and Memory Allocation Strategies in Operating Systems

This program simulates memory management and deadlock detection in an operating system using Python. It defines `Process` and `MemoryBlock` classes to model system processes and memory, then uses a `DeadlockDetector` to identify circular waits using graph traversal. The `MemoryManager` class implements **First Fit** and **Best Fit** strategies to allocate memory while tracking performance, fragmentation, and allocation time. Simulation results are visualized with graphs to show how different strategies affect efficiency and system safety.


## 👥Team Members

 - **Michael Zander Boncodin** - Video editing and final polishing  
 - **Celestino Lontoc** - Program Tester
 - **Shana Eve Gonzales** - Documentation
 - **Jon Renzo Toledo** - Main Programmer
 - **Louise Ann Yap** - Report writing


## 🤖Classes

### **Process**
Represents a system process with memory and resource requirements.

**Parameters:**
- `pid` (int): Process ID
- `memory_requirement` (int: MB): Memory Needed by the Process
- `resources_needed` (array): Actions/Resources the Process Needed
- `execution_time` (int: optional) : Time the process excecutes 

**Example:**
```python
processes = [
    Process(1, 100, ['Printer', 'Scanner']),
    Process(2, 150, ['Scanner', 'Network']),
    Process(3, 120, ['Network', 'Printer']),
    Process(4, 80, ['Database', 'FileSystem']),
    Process(5, 200, ['FileSystem', 'Network'])
]
```

### **MemoryBlock**
Represents chunks of system memory and their allocation status.

**Parameters:**
- `start` (int): Memory Index
- `size` (int: MB): Total Memory Size
- `is_free` (boolean: optional): Check if Memory is free
 

**Example:**
```python
# Allocation of Memory
new_block = MemoryBlock(
    block.start + process.memory_requirement,
    block.size - process.memory_requirement
)
```

### **DeadlockDetector**
Manages resource requests and allocations.


**Example:**
```python
# Instance of Deadlock Detector
detector = DeadlockDetector()
detector.request_resource(process_id, resource)
```

### **MemoryManager**
Tracks memory fragmentation and allocation performance for analysis.

**Parameters:**
- `total_memory` (int: MB): Memory Size

**Example:**
```python
# Instance of Memory Manager
manager = MemoryManager(1200)
```


## 📸Screenshots
![simulation](https://github.com/user-attachments/assets/aa240e6e-bea7-4a82-9696-1ea63479e223)
![{23AF554E-2AA1-4BB9-9AFF-0E146AD5551A}](https://github.com/user-attachments/assets/e0bb1dd2-1d99-4038-9037-fea53638b62c)

![analysis](https://github.com/user-attachments/assets/e791a89e-668f-4f6a-b439-8558883c9e9b)
![{7BC776DE-70D2-4BBD-82B9-02F442CF48CB}](https://github.com/user-attachments/assets/ff862b09-9a0c-4833-a6c4-0a7effc2058a)



