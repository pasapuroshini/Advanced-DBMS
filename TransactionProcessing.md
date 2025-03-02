### **Transaction Processing in DBMS**

A **transaction** is a **logical unit of work** in a database that consists of one or more queries or operations that must be executed **as a single unit**.

### **What is a Transaction?**

*   A transaction groups multiple **queries or actions** into a **single logical unit**.
    
*   Example: A bank transfer involves:
    
    1.  Deducting money from Account A
        
    2.  Adding money to Account B
        
    3.  If one step fails, the whole process should be rolled back.
        

### **ACID Properties of Transactions**

Transaction processing must ensure **ACID properties** to maintain data integrity:

1.  **Atomicity** → "All or Nothing"
    
    *   A transaction should either **execute all operations successfully** or **roll back completely** if any step fails.
        
2.  **Consistency** → "Data Integrity"
    
    *   The database should remain in a **valid state** before and after the transaction.
        
3.  **Isolation** → "Concurrency Handling"
    
    *   Transactions executing at the same time should **not interfere** with each other.
        
4.  **Durability** → "Permanent Changes"
    
    *   Once a transaction is committed, its changes **must persist** even in case of system failures.
        

### **Transaction Processing Components**

#### **1\. Concurrency Control Manager (Scheduler)**

*   Ensures **multiple transactions can run concurrently** without conflicts.
    
*   Uses techniques like **locking, timestamp ordering, and serialization** to prevent data inconsistency.
    

#### **2\. Logging and Recovery Manager**

*   **Logging:** Maintains a **log file** that records all changes made by a transaction.
    
*   **Recovery:** Ensures the database can recover from **failures (e.g., power loss, system crash)** by rolling back incomplete transactions.
    

#### **3\. Deadlock Resolution**

*   **Deadlocks** occur when transactions **wait for each other’s locked resources indefinitely**.
    
*   DBMS handles deadlocks using:
    
    *   **Deadlock Prevention** (avoiding unsafe states).
        
    *   **Deadlock Detection and Recovery** (killing a transaction to free resources).
        

### **Transaction Lifecycle**

1.  **Start Transaction** → Begins execution.
    
2.  **Read & Write Operations** → Access database.
    
3.  **Commit Transaction** → If all operations succeed, changes are made permanent.
    
4.  **Rollback Transaction** → If an error occurs, all changes are undone.
    

### **Conclusion**

Transaction processing ensures **data consistency, integrity, and concurrent execution** while handling failures and deadlocks effectively.
