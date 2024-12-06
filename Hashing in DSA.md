Hashing in Data Structures and Algorithms (DSA) is a technique used to map data of arbitrary size (keys) to fixed-size values (hash values) in a way that supports efficient insertion, deletion, and lookup operations
## Hash Tables
- Let, for a string, sum of characters' ASCII value is divided by their sum 
- The remainder is taken as hashing key
- So against each key there can be 1/more elements
- elements with the same hash key are stored in a linked list `(Hash Chaining)`

```mermaid
graph TD
    A["Alice"] -->|Hash Function| B[Hash Value: 1]
    C["Bob"] -->|Hash Function| D[Hash Value: 2]
    E["Charlie"] -->|Hash Function| F[Hash Value: 1]
    G["David"] -->|Hash Function| H[Hash Value: 3]

    subgraph Hash Table
        I[Bucket 1] --> J["Alice -> Value 1"]
        I --> K["Charlie -> Value 3"]
        L[Bucket 2] --> M["Bob -> Value 2"]
        N[Bucket 3] --> O["David -> Value 4"]
    end

    B --> I
    D --> L
    F --> I
    H --> N


```
### Diagram Explanation:
1. **Keys** (e.g., "Alice", "Bob", etc.) are input into the **hash function**, which generates a **hash value**.
2. The **hash value** determines the **bucket index** in the hash table.
3. Multiple keys (e.g., "Alice" and "Charlie") can map to the same bucket due to collisions. These are managed using **chaining** (storing items in a list at the bucket index).





