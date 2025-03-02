# Indexing on Sequential Files: Dense Indexing  

## Sequential File  
- A **sequential file** is a data file where records are **sorted** based on the indexed attribute.  
- Indexing on such files is the **simplest form of indexing**.  
- This indexing is most useful when the **search key is the primary key** of the relation.  

## Dense Indexing  
- **Every record** in the data file has a corresponding **entry in the index file**.  
- Supports **queries with specific search key values** efficiently.  
- Requires checking **every entry** in the index for lookups.  

## **Advantages of Dense Indexing**  
### 1. **Fewer Blocks in Index File**  
- The **index file** has **fewer blocks** than the data file, reducing storage space.  

### 2. **Efficient Searching with Binary Search**  
- Since keys are **sorted**, **binary search** can be used.  
- This reduces search time to **O(log₂ n) comparisons**.  

### 3. **Index File Can Be Stored in Main Memory**  
- The **index file is small enough** to be **kept in RAM**, improving search speed.  
