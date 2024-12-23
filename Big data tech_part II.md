
**2.5(a) Design and Architecture of HDFS with a Neat Diagram and Ensuring Data Reliability**

### **Introduction to HDFS**

Hadoop Distributed File System (HDFS) is a highly fault-tolerant, distributed storage system designed to run on commodity hardware. Its primary goal is to provide scalable, reliable, and efficient storage for massive datasets in Big Data environments. HDFS follows the "write once, read many" principle and is optimized for high-throughput access rather than low-latency operations.

### **Design and Architecture of HDFS**

HDFS comprises several components that work together to ensure distributed storage and reliability:

1. **NameNode (Master Node):**

   - Stores metadata, such as directory structures, file permissions, and block locations.
   - Controls access to files and manages namespace operations.
   - Does not store the actual data.

2. **DataNode (Slave Nodes):**

   - Stores the actual data in the form of blocks.
   - Sends periodic heartbeats and block reports to the NameNode.

3. **Secondary NameNode:**

   - Acts as a checkpoint to periodically merge the NameNode’s namespace and edit logs.
   - Not a backup but helps in metadata recovery during NameNode failure.

4. **Client:**

   - Interfaces with HDFS for file operations.
   - Divides files into blocks and coordinates with NameNode and DataNodes for storage and retrieval.

### **Diagram of HDFS Architecture**

```
         Client
           |
    -----------------
    |               |
NameNode      Secondary NameNode
    |
---------------------
|         |         |
DataNode  DataNode  DataNode
```

### **Key Features Ensuring Data Reliability**

1. **Data Replication:**

   - Each data block is replicated across multiple DataNodes (default replication factor: 3).
   - Ensures high availability even in case of node failure.

2. **Heartbeat Mechanism:**

   - DataNodes send periodic heartbeats to the NameNode to confirm they are operational.
   - The absence of a heartbeat triggers replication of blocks from other nodes.

3. **Rack Awareness:**

   - Data replication is distributed across racks to prevent data loss due to rack-level failures.

4. **Data Integrity:**

   - HDFS calculates and verifies checksums for data blocks.
   - Corrupt blocks are automatically detected and replaced using replicas.

5. **Automatic Failover:**

   - In case of node failures, HDFS automatically reassigns tasks and ensures continuous operation.

### **Applications**

- Large-scale data storage for analytics (e.g., social media data).
- Distributed log storage for real-time processing.

---

**2.5(b) Data Compression in Hadoop I/O and Its Impact on Data Storage Efficiency**

### **Introduction to Data Compression**

Data compression in Hadoop reduces the size of datasets, leading to improved storage efficiency, faster data transfers, and optimized processing in distributed environments.

### **Techniques and Tools for Data Compression in Hadoop**

1. **Compression Codecs:**

   - Hadoop supports several codecs, including:
     - **Gzip:** High compression ratio but slower.
     - **Bzip2:** Better compression ratio than Gzip but even slower.
     - **Snappy:** Fast compression with moderate compression ratio.
     - **LZO:** Balanced speed and compression, ideal for real-time processing.

2. **File Formats with Built-in Compression:**

   - **SequenceFile:** Supports record and block-level compression.
   - **Avro and Parquet:** Schema-based formats designed for efficient storage and query execution.

### **Impact on Data Storage Efficiency**

1. **Reduced Storage Requirements:**

   - Compressing data reduces storage costs, especially for massive datasets.

2. **Optimized Data Transfer:**

   - Smaller files result in faster network transfers between Hadoop nodes.

3. **Improved Processing Speed:**

   - Compression reduces the volume of data processed by MapReduce jobs.

4. **Trade-Off:**

   - Compression introduces CPU overhead for encoding/decoding, which must be balanced with storage and processing needs.

### **Applications**

- Archiving historical data.
- Faster data processing in analytical pipelines.

---

**2.6(a) Execution of a MapReduce Job: Task Execution and Fault Tolerance**

### **Introduction to MapReduce**

MapReduce is a programming model in Hadoop used for processing large datasets in a distributed environment. It divides tasks into Map and Reduce phases.

### **Execution Workflow of a MapReduce Job**

1. **Job Submission:**

   - The client submits a job to the JobTracker (YARN ResourceManager in newer versions).
   - Input data is split into InputSplits and assigned to Mapper tasks.

2. **Map Phase:**

   - Each Mapper processes its InputSplit and generates intermediate key-value pairs.

3. **Shuffle and Sort Phase:**

   - Intermediate data is grouped and sorted by key.
   - The sorted data is sent to Reducers.

4. **Reduce Phase:**

   - Reducers aggregate the data and produce the final output.
   - Results are stored in HDFS.

### **Fault Tolerance Mechanisms**

1. **Task Reattempt:**

   - Failed tasks are automatically re-executed on another node.

2. **Speculative Execution:**

   - Slow-running tasks are redundantly executed on multiple nodes, and the first successful result is accepted.

3. **Data Replication:**

   - HDFS ensures that input data is replicated, preventing data loss.

4. **Heartbeat Monitoring:**

   - The JobTracker monitors node health through heartbeats.

---

**2.6(b) Data Ingestion with Sqoop and Its Integration with Hadoop**

### **Introduction to Sqoop**

Apache Sqoop is a data ingestion tool that efficiently transfers data between structured databases (e.g., MySQL, Oracle) and Hadoop ecosystems.

### **Process of Data Ingestion**

1. **Importing Data:**

   - Sqoop imports data from relational databases into HDFS, Hive, or HBase.
   - Supports parallel import for faster execution.

2. **Exporting Data:**

   - Sqoop exports processed data from HDFS back to relational databases.

### **Integration with Hadoop**

- **MapReduce Framework:** Sqoop uses MapReduce for parallel data transfers, ensuring scalability.
- **File Formats:** Supports Avro, Parquet, and SequenceFile formats.

**Diagram of Sqoop Integration:**

```
   [RDBMS] --> [Sqoop] --> [HDFS/Hive/HBase]
```

---

**3.3(a) Concept of Graph Databases and Their Application in Big Data Analytics**

### **Introduction to Graph Databases**

Graph databases are specialized databases that use graph structures (nodes, edges, and properties) to store and query data. They are optimized for analyzing relationships.

### **Key Features**

1. **Nodes and Edges:** Represent entities and relationships.
2. **Schema-Free:** Flexible for evolving datasets.
3. **Query Language:** Supports languages like Cypher for complex queries.

### **Applications in Big Data Analytics**

1. **Social Networks:** Analyze user connections and behavior.
2. **Fraud Detection:** Identify anomalous patterns in transactions.
3. **Recommendation Engines:** Suggest products or services based on user preferences.

---

**3.3(b) Sharding Mechanism in NoSQL Databases for Scaling**

### **Introduction to Sharding**

Sharding is a database partitioning technique that divides data into smaller, manageable units called shards.

### **How Sharding Works**

1. **Shard Key:** Determines how data is distributed across shards.
2. **Independent Shards:** Each shard functions as an independent database.

### **Benefits of Sharding**

1. **Scalability:** Distributes data across multiple servers, handling large datasets.
2. **Performance:** Reduces the load on individual nodes.
3. **Fault Tolerance:** Failure of one shard doesn’t affect others.

### **Applications**

- E-commerce platforms.
- Social media applications with high user activity.

nice&#x20;




---
---


## UNIT-III NoSQL

#### Introduction to NoSQL

NoSQL, which stands for "Not Only SQL," is a category of database management systems that provide a flexible schema design and are optimized for large-scale data storage and retrieval. Unlike traditional relational databases, NoSQL databases are designed to handle unstructured, semi-structured, and structured data, making them ideal for Big Data applications. They are highly scalable, distributed, and capable of supporting high throughput operations. NoSQL databases are classified into four primary types: key-value stores, document stores, column-family stores, and graph databases. 

##### Characteristics of NoSQL Databases:

1. **Schema Agility**: No fixed schema; data structure can evolve without the need for schema migrations.
2. **Horizontal Scalability**: Data is distributed across servers to handle growing datasets and increased traffic.
3. **High Availability**: Built-in mechanisms ensure fault tolerance and minimal downtime.
4. **Consistency Trade-offs**: Often emphasize eventual consistency over strict ACID compliance to optimize performance.
5. **Polyglot Persistence**: Encourages using different types of databases for different parts of a system based on data requirements.

##### Limitations of NoSQL:

- Lack of standardization compared to SQL.
- Limited support for complex joins and transactions.
- Steeper learning curve for relational database practitioners.

##### Real-World Examples:

- **Google BigTable**: Powers Google Search and Maps.
- **Amazon DynamoDB**: Supports real-time applications like e-commerce.
- **Cassandra**: Handles large-scale social media data
##### Features of NoSQL:
1. **Scalability**: Horizontally scalable to handle massive volumes of data.
2. **Flexibility**: Schema-less nature allows for easier adaptation to changing data structures.
3. **High Performance**: Optimized for high-speed read and write operations.
4. **Distributed Architecture**: Data is spread across multiple nodes for fault tolerance and redundancy.

##### Use Cases:
- Social Media Platforms
- Real-Time Analytics
- Internet of Things (IoT)
- Content Management Systems

---

#### Aggregate Data Models

The aggregate data model in NoSQL organizes data into aggregates, which are collections of related data grouped together. Aggregates are often used in distributed databases to enable efficient access and manipulation.

##### Key Concepts:
- **Aggregate**: A collection of data treated as a single unit for read/write operations.
- **Boundaries**: Define how data is grouped to align with query patterns.
- **Consistency**: Operations are performed within the scope of an aggregate to ensure data consistency.

##### Benefits:
- Improved query performance due to pre-grouped data.
- Better alignment with application needs for specific data access patterns.
##### Use Cases:

- Shopping carts (e.g., aggregating product details, prices, and quantities in a single document).
- Sensor data from IoT devices grouped by time intervals.


---

#### Key-Value and Document Data Models

##### Key-Value Data Model:
- Stores data as a collection of key-value pairs.
- Each key is unique and acts as an identifier for its associated value.
- Simple and fast, making it ideal for caching, session storage, and real-time analytics.

###### Features:

- Keys must be unique, ensuring quick lookups.
- Values can be simple (e.g., strings) or complex (e.g., JSON objects).

###### Optimizations:

- In-memory databases like **Redis** or **Memcached** store data in memory for ultra-fast retrieval.
- Persistent key-value stores, such as **Riak**, write data to disk for durability.

**Example:**
```
{
  "userID_123": "John Doe",
  "userID_124": "Jane Smith"
}
```

**Applications:**
- Caching layers (e.g., Redis, Memcached)
- E-commerce product catalogs

##### Document Data Model:
- A document data model organizes data into semi-structured documents, usually stored in JSON, BSON, or XML format. These documents allow hierarchical relationships and nested structures, making them more expressive than flat key-value pairs.

###### Benefits:

- Supports indexing on nested attributes for faster queries.
- Flexible schema enables easy modifications to data structures.

###### Real-World Applications:

- **Content Management Systems (CMS)**: Dynamically structured content like blog posts or product catalogs.
- **User Profiles**: Complex user data, including preferences, transaction history, and settings.

**Example:**
```
{
  "userID": "123",
  "name": "John Doe",
  "address": {
    "city": "New York",
    "zip": "10001"
  }
}
```



---

#### Relationships

While NoSQL databases are not inherently relational, they do allow for the modeling of relationships between entities. These can be represented in different ways depending on the database type.

##### Techniques for Modeling Relationships:
- **Embedded Documents**: Storing related data within the same document.
	- Pros: Fast read performance as all data is co-located.
	- Cons: Redundant data if the relationship changes frequently.
	
```json

{
  "orderID": "A123",
  "customer": {
    "name": "Alice",
    "email": "alice@example.com"
  }
}

```

- **References**: Using keys to point to related documents.
	- Pros: Reduces data duplication.
	- Cons: Slower reads due to multiple lookups.

```json
{
  "orderID": "A123",
  "customerID": "C456"
}

```

**Example in Document Model:**

```
{
  "userID": "123",
  "orders": [
    { "orderID": "A1", "amount": 250 },
    { "orderID": "B2", "amount": 100 }
  ]
}
```

---

#### Graph Databases
Graph databases are specialized NoSQL databases designed to handle data with complex relationships. They represent data as nodes (entities) and edges (relationships) and are particularly useful for applications requiring relationship analysis.

##### Features:
1. **Node**: Represents an entity (e.g., user, product).
2. **Edge**: Represents a relationship between nodes (e.g., "follows," "buys").
3. **Properties**: Metadata or attributes associated with nodes and edges.

##### Advanced Features:

- **Traversal Algorithms**: Graph databases provide built-in support for BFS, DFS, and shortest path algorithms.
- **ACID Compliance**: Many graph databases like Neo4j support ACID transactions.
- **Schema Flexibility**: Easily accommodates evolving data relationships
##### Applications:
- Social networks (e.g., LinkedIn, Facebook)
- Fraud detection
- Recommendation systems

**Example:**
```
(Alice) -[FRIENDS]-> (Bob)
(Bob) -[LIKES]-> (Movie: Inception)
```

---

#### Schema-Less Databases
Schema-less databases, also known as schema-free databases, do not enforce a fixed schema for the data they store. This flexibility allows for dynamic and evolving data structures.

##### Key Features:

- **Dynamic Data Models**: Each record/document can have a unique structure.
- **Rapid Prototyping**: Supports iterative development cycles.

##### Advantages:
- Adaptable to rapidly changing requirements.
- Reduces overhead for database migrations.
- Ideal for storing heterogeneous datasets.
##### Limitations:

- Data integrity checks are often left to the application layer.
- Increased complexity in querying heterogeneous data.

##### Examples of Schema-Less Databases:
- **MongoDB**: Stores semi-structured JSON-like documents.
- **Couchbase**: Offers a distributed, schema-less architecture.

##### Use Cases:
- Mobile app development
- Real-time data processing

In conclusion, NoSQL databases provide diverse and powerful tools for handling Big Data, catering to a variety of use cases with their unique data models and flexibility.


---

#### Materialized Views

Materialized views are database objects that store the results of a query physically. Unlike regular views, which are virtual and require recalculating data every time they are accessed, materialized views precompute and store the results, enabling faster query performance.

#### **Key Features**

1. **Precomputed Data**: Results are calculated and stored in advance.
2. **Refresh Options**:
    - **Manual Refresh**: Requires explicit action to update the data.
    - **Automatic Refresh**: Uses triggers or scheduled tasks to keep the materialized view up to date.
3. **Indexed Access**: Materialized views can have indexes to further optimize query performance.
#### **Advantages**

1. **Improved Performance**: Eliminates the need to recompute complex joins or aggregations repeatedly.
2. **Reduced Computation Costs**: Minimizes database workload for frequently accessed queries.
3. **Data Snapshot**: Provides a consistent view of data at a specific point in time.
#### **Challenges**

1. **Storage Overhead**: Requires additional storage space.
2. **Stale Data**: Materialized views can become outdated if not refreshed regularly.

##### Applications:
- Data Warehousing: Used to summarize large datasets.
- Reporting: Optimizes frequently accessed data for dashboards.
- Aggregation Queries: Improves performance for complex queries involving aggregations.
- **Business Intelligence**: Precomputing results for dashboards and reports.
- **ETL Processes**: Summarizing raw data into meaningful insights.

##### Example:
```sql
CREATE MATERIALIZED VIEW sales_summary AS
SELECT product_id, SUM(quantity) AS total_sold
FROM sales
GROUP BY product_id;
```

---

#### Distribution Models

Distribution models define how data is distributed across nodes in a distributed database system. They ensure scalability, fault tolerance, and efficient query execution.

#### **Types of Distribution Models**

1. **Range-Based Distribution**:
    
    - Data is distributed based on specific value ranges of a key (e.g., date ranges or alphabetical ranges).
    - Ideal for time-series data.
2. **Hash-Based Distribution**:
    
    - A hash function is applied to a key to determine the node where the data will reside.
    - Ensures even distribution of data.
3. **Replication-Based Distribution**:
    
    - Data is copied across multiple nodes to ensure high availability and fault tolerance.
    - Common in distributed systems like Cassandra and MongoDB.
4. **Geographic Distribution**:
    
    - Data is stored closer to users based on geographic proximity to reduce latency.
    - Widely used in content delivery networks (CDNs).

#### **Benefits**

1. **Fault Tolerance**: Ensures data availability even in the event of node failure.
2. **Scalability**: Supports the addition of more nodes to handle growing data volumes.
3. **Performance**: Reduces data access time by distributing the load across multiple nodes

##### Applications:
- Cloud Databases (e.g., Amazon Aurora, Google BigQuery)
- Distributed File Systems (e.g., HDFS, Cassandra)
#### **Challenges**

1. **Data Skew**: Uneven distribution can lead to imbalanced workloads.
2. **Complexity**: Requires careful design to ensure efficient query execution.

---

#### Sharding

Sharding is the process of dividing a large dataset into smaller, more manageable pieces called shards, which are distributed across multiple servers. Each shard acts as an independent database.

#### **How It Works**

1. **Shard Key**: A specific attribute (e.g., user ID) is used to determine the shard for each record.
2. **Shard Placement**: Each shard is stored on a separate server.
3. **Query Routing**: The database system routes queries to the appropriate shard based on the shard key.

#### **Benefits**

1. **Scalability**: Enables horizontal scaling by distributing data across servers.
2. **Improved Performance**: Reduces the amount of data processed by individual nodes.
3. **Fault Isolation**: Failure in one shard does not impact others.

#### **Challenges**

1. **Complex Querying**: Cross-shard queries can be slower and more complex.
2. **Rebalancing**: Adding or removing shards requires data redistribution.

#### **Example**

In an e-commerce database, orders might be sharded by customer ID:

- Customers 1–1000 → Shard 1
- Customers 1001–2000 → Shard 2

---

#### Master-Slave Replication
Master-slave replication is a replication model where one node (the master) is responsible for handling write operations, and multiple slave nodes replicate the master’s data to handle read operations.

##### Key Features:

1. **Master Node**: Handles write operations.
2. **Slave Nodes**: Handle read operations and replicate data from the master.
3. **Centralized Writes**: All write operations occur on the master node.
4. **Read Scalability**: Read requests are distributed among slave nodes.
5. **Asynchronous Replication**: Updates are propagated from the master to slaves, sometimes with a delay.
#### **Advantages**

1. **Improved Read Performance**: Reduces the load on the master node by distributing read requests.
2. **Data Redundancy**: Provides backups for disaster recovery.
##### Applications:
- High Availability: Ensures data redundancy.
- Load Balancing: Distributes read requests across slaves.

##### Challenges:
- Write Bottleneck: All writes are handled by the master.
- Potential for Lag: Slaves may lag behind the master.

---

#### Peer-to-Peer Replication

In peer-to-peer replication, all nodes are equal and can act as both a master and a slave. Each node can handle read and write operations.

#### **Advantages**

1. **No Single Point of Failure**: All nodes can handle read and write requests.
2. **High Availability**: Ensures continuous operation even if some nodes fail.

#### **Challenges**

1. **Conflict Resolution**: Concurrent updates may lead to conflicts.
2. **High Complexity**: Managing synchronization across nodes is challenging.
##### Benefits:
- High Availability: No single point of failure.
- Scalability: Supports a decentralized architecture.

##### Applications:
- Collaborative Applications (e.g., Google Docs)
- Distributed Databases (e.g., Couchbase, Cassandra)

---

#### Sharding and Replication

Combining sharding and replication enhances the scalability and fault tolerance of distributed databases. Each shard is replicated across multiple nodes.

##### Advantages:
1. **Fault Tolerance**: Ensures data redundancy within shards.
2. **Scalability**: Distributes data across shards and replicas.
3. **Efficient Load Balancing**: Distributes both read and write loads.

---

### **Consistency in Distributed Databases**

Consistency in distributed databases refers to ensuring that all nodes in a distributed system reflect the same data at a given point in time after a write operation. It is one of the key components of the **CAP theorem**, which states that a distributed system can achieve only two out of the three guarantees: **Consistency**, **Availability**, and **Partition Tolerance**.

#### Types of Consistency:

1. **Strong Consistency**:
    
    - Guarantees that after a write, all subsequent reads will reflect the most recent write.
    - The system enforces strict synchronization among all nodes.
    - Used in systems where correctness is critical (e.g., financial systems).
    - **Example**: Relational databases using ACID properties.
2. **Eventual Consistency**:
    
    - Ensures that, in the absence of new updates, all replicas will converge to the same state eventually.
    - Faster write operations but may temporarily allow stale reads.
    - Common in highly available, partition-tolerant systems like NoSQL databases.
    - **Example**: DNS systems or Amazon DynamoDB.
3. **Causal Consistency**:
    
    - Maintains the order of causally related operations (e.g., if operation A leads to operation B, then A must be visible before B).
    - More relaxed than strong consistency but stricter than eventual consistency.
4. **Read-Your-Writes Consistency**:
    
    - Guarantees that a user will always see the result of their own write operations immediately, regardless of the state of the system.
5. **Monotonic Read Consistency**:
    
    - Ensures that if a process reads a value, subsequent reads by the same process will not return an older value.

---

### **Relaxing Consistency**

Relaxing consistency refers to compromising on strict consistency guarantees to achieve better performance, scalability, or availability in distributed systems. This is often necessary in modern large-scale systems where the trade-offs of the **CAP theorem** and the **BASE model** (Basic Availability, Soft State, Eventual Consistency) come into play.

#### Why Relax Consistency?

1. **Latency Reduction**:
    - Strict consistency often requires synchronization across geographically distributed nodes, increasing latency.
2. **Partition Tolerance**:
    - In the presence of network partitions, relaxing consistency ensures the system remains available.
3. **Scalability**:
    - Systems can handle more requests simultaneously without waiting for all nodes to synchronize.

#### Techniques for Relaxing Consistency:

1. **Stale Reads**:
    
    - Allow nodes to serve slightly outdated data to reduce read latency.
2. **Quorum-Based Protocols**:
    
    - Instead of synchronizing all nodes, a subset of nodes (quorum) must agree on a read/write operation.
    - **Example**: In a 5-node system, a write may be considered successful if 3 nodes (majority quorum) confirm it.
3. **Vector Clocks**:
    
    - Keep track of version histories across nodes to handle conflicts while avoiding strict synchronization.
4. **Conflict Resolution**:
    
    - Handle inconsistencies through automatic or manual resolution, such as **last write wins** or application-specific logic.

#### Examples of Relaxed Consistency:

- **Amazon DynamoDB**: Optimized for availability with eventual consistency.
- **Cassandra**: Allows configurable consistency levels (e.g., ONE, QUORUM, ALL).

---

### **Version Stamps**

Version stamps (or version vectors) are mechanisms used in distributed systems to keep track of the version history of data. They are essential for resolving conflicts and maintaining consistency when updates occur across multiple replicas in the absence of strict synchronization.

#### Purpose of Version Stamps:

1. **Conflict Detection**:
    - Identify conflicting writes when updates occur on different replicas simultaneously.
2. **Causal Ordering**:
    - Establish the order of operations to ensure causal consistency.
3. **Efficient Synchronization**:
    - Avoid redundant updates by comparing version histories.

#### Types of Version Stamps:

1. **Logical Timestamps**:
    
    - Use a single counter to represent the sequence of operations.
    - **Lamport Timestamps**:
        - A scalar value that increments with each operation.
        - Does not capture causal relationships between events.
2. **Vector Clocks**:
    
    - A vector of counters, one for each node, to track causal relationships.
    - When an update occurs at a node, the counter for that node is incremented.
    - **Conflict Detection**:
        - Two vector clocks are compared. If neither dominates (i.e., one clock has higher values in all positions), a conflict is detected.
    - **Example**:
        - Node A's vector clock: `[2, 0, 0]`
        - Node B's vector clock: `[1, 1, 0]`
        - Conflict resolution involves merging the states or application-specific logic.
3. **Hybrid Timestamps**:
    
    - Combine physical time (e.g., UTC) with logical timestamps to improve consistency and conflict resolution.

#### Use Cases of Version Stamps:

1. **Distributed Databases**:
    - Detect conflicts in eventual consistency models.
    - Examples: Amazon DynamoDB, Cassandra.
2. **Version Control Systems**:
    - Track changes and manage merges in systems like Git.
3. **Event Sourcing**:
    - Maintain an ordered history of events in distributed event-driven systems.

---

#### Map-Reduce
Map-Reduce is a programming model for processing large datasets in parallel.

##### Components:
1. **Mapper**: Processes input data and emits key-value pairs.
2. **Reducer**: Aggregates values associated with the same key.

##### Example:
- Input: List of words
- Mapper: Emits (word, 1)
- Reducer: Sums the counts for each word.

---

### **MapReduce**

MapReduce is a programming model and a processing framework designed to handle large-scale data processing across distributed systems. It was introduced by Google and is widely used in distributed computing systems like Hadoop.

#### **Key Concepts**

1. **Map Function**:
    
    - The "Map" step takes input data, processes it, and outputs a set of intermediate key-value pairs.
    - Each piece of input data is independently transformed into a key-value pair by the map function.
    
    Example:
    
    - Input: A list of words in a document.
    - Map Output: Each word becomes a key, and its occurrence count becomes the value.
    
```vbnet
Input: ["cat", "dog", "cat", "dog", "mouse"]
Output: [("cat", 1), ("dog", 1), ("cat", 1), ("dog", 1), ("mouse", 1)]
```

1. **Reduce Function**:
    
    - The "Reduce" step takes intermediate key-value pairs, groups them by key, and performs an aggregation operation.
    - Example: Summing up all counts for each key.
    
    Example:
    
    - Input: [("cat", 1), ("dog", 1), ("cat", 1), ("dog", 1), ("mouse", 1)]
    - Reduce Output: [("cat", 2), ("dog", 2), ("mouse", 1)]
2. **Shuffle and Sort**:
    
    - Between the Map and Reduce phases, data is grouped by keys and sent to appropriate reducers (shuffling).
    - The key-value pairs are then sorted by key before being processed by reducers.

#### **Advantages**

- Scalability: Handles petabytes of data by distributing tasks across multiple nodes.
- Fault Tolerance: Automatically reassigns tasks to other nodes in case of failure.
- Simplicity: Programmers only need to write map and reduce functions.

#### **Applications**

- Counting word frequencies in documents.
- Aggregating log data for analysis.
- Processing sensor data in IoT applications.

---

### **Partitioning and Combining**

#### **Partitioning**

Partitioning determines how intermediate key-value pairs (generated by the map function) are distributed among the reducers.

1. **Purpose**:
    
    - Ensures data with the same key goes to the same reducer.
    - Balances the workload among reducers.
2. **How it Works**:
    
    - A **Partitioner** function assigns each key-value pair to a specific reducer based on the key.
    - Example: A hash function like `hash(key) % number_of_reducers` is commonly used.
3. **Challenges**:
    
    - Skewed data distribution: Some reducers may get more data than others, leading to bottlenecks.
    - Efficient partitioning requires knowledge of the data distribution.
4. **Example**:
    
    - If there are three reducers and keys are `a`, `b`, `c`, and `d`, partitioning might work as follows:

```less

Reducer 0: [("a", 1), ("d", 1)]
Reducer 1: [("b", 1)]
Reducer 2: [("c", 1)]

```

#### **Combining**

Combining is an optimization technique that reduces the amount of data transferred during the shuffle phase.

1. **Purpose**:
    
    - Minimizes network congestion by performing partial aggregation on intermediate data locally at each mapper.
2. **How it Works**:
    
    - A **Combiner** function operates like a mini-reducer.
    - It aggregates intermediate key-value pairs before sending them to the reducers.
3. **Example**:
    
    - In a word count problem:

```less

Mapper Output: [("cat", 1), ("cat", 1), ("dog", 1)]
Combiner Output: [("cat", 2), ("dog", 1)]

```

1. **Limitations**:
    
    - Not all problems can use combiners.
    - Combiners must be **idempotent**, meaning the order of combining should not affect the result.

---

### **Composing MapReduce Calculations**

Composing MapReduce calculations involves chaining multiple MapReduce jobs to solve complex problems. Each job produces an output that becomes the input for the next job.

#### **Why Compose MapReduce Jobs?**

1. **Complex Workflows**:
    - Some problems require multiple stages of computation (e.g., join operations, sorting, filtering).
2. **Data Dependencies**:
    - Intermediate outputs from one job are used for further processing in another job.

#### **How it Works**

1. **Job Chaining**:
    
    - The output of the first MapReduce job is stored in HDFS (or a similar distributed file system).
    - The next job reads this output as input and performs its computations.
2. **Examples**:
    
    - **Log Analysis**:
        - Job 1: Extract and count error codes from logs.
        - Job 2: Sort error codes by frequency.
    - **Graph Processing**:
        - Job 1: Compute adjacency lists for graph nodes.
        - Job 2: Calculate shortest paths using adjacency lists.

#### **Optimization Techniques**

1. **Data Locality**:
    - Ensure jobs are scheduled on nodes where the data resides to reduce data transfer costs.
2. **Intermediate Compression**:
    - Compress intermediate data to reduce shuffle time.
3. **Multi-Stage Jobs**:
    - Combine logic to minimize the number of jobs when possible.

---

### **Example: Word Frequency Analysis with Composed Jobs**

1. **Job 1: Tokenize and Count Words**
    
    - Map: Split text into words and emit `(word, 1)`.
    - Reduce: Aggregate counts for each word.
2. **Job 2: Sort by Frequency**
    
    - Map: Swap key and value to emit `(count, word)`.
    - Reduce: Sort and aggregate by count.
    
    Output: A list of words sorted by frequency.
    

---

### **Challenges and Best Practices**

1. **Challenges**:
    - High I/O Overhead: Intermediate data must be written to disk.
    - Job Dependencies: Mismanagement of dependencies can lead to inefficient workflows.
2. **Best Practices**:
    - Use combiners to reduce shuffle data size.
    - Optimize partitioning for balanced workloads.
    - Chain jobs efficiently to avoid redundant computations.+


---
---

>**UNIT-IV Fundamentals of Apache Pig, Hive ,and HBase**
>
 Pig: Introduction to PIG, Execution Modes of Pig, Comparison of Pig with Databases, Grunt, Pig Latin, User Defined
 Functions, Data Processing operators. Hive: Hive Shell, Hive Services, Hive Meta store, Comparison with Traditional
 Databases, HiveQL, Tables, Querying Data and User Defined Functions.   HBase: HBase Concepts, Clients, Example,
 HBase Versus RDBMS.                                                                                                      

### **Execution Modes of Pig**

Apache Pig is a high-level platform for analyzing large datasets. It uses a scripting language called Pig Latin, which is compiled into MapReduce jobs and executed on Hadoop. Pig offers two primary execution modes that cater to different development and production needs.

---

#### **1. Local Mode**

In this mode, Pig runs entirely on the local machine and uses the local filesystem.

- **Use Case**:
    
    - Best suited for development, debugging, and testing Pig scripts on small datasets.
    - Eliminates the need for Hadoop, making it lightweight and fast for testing.
- **How It Works**:
    
    - Pig scripts are executed without connecting to a Hadoop cluster.
    - Input and output files are stored and processed on the local filesystem.
- **Advantages**:
    
    - Faster execution for small datasets.
    - No Hadoop setup required.
    - Ideal for script development and testing.
- **Limitations**:
    
    - Cannot handle large datasets due to resource constraints.
    - Not suitable for production environments.

---

#### **2. MapReduce Mode (Distributed Mode)**

In this mode, Pig executes scripts on a Hadoop cluster, leveraging HDFS and MapReduce for distributed processing.

- **Use Case**:
    
    - Designed for processing large-scale datasets in production environments.
    - Fully utilizes Hadoop's distributed capabilities for scalability and fault tolerance.
- **How It Works**:
    
    - Pig connects to a Hadoop cluster.
    - Scripts are translated into MapReduce jobs that are executed on the cluster.
    - Input and output files are stored in HDFS.
- **Advantages**:
    
    - Can process terabytes of data across multiple nodes.
    - Fault tolerance provided by Hadoop.
    - Scalability to handle growing data sizes.
- **Limitations**:
    
    - Requires a functional Hadoop cluster.
    - Slower development cycle due to higher execution overhead.

---

#### **Choosing the Right Execution Mode**

- **Local Mode**: Use for script development, debugging, and testing with small datasets.
- **MapReduce Mode**: Use for large-scale data processing in production environments.

---

### **Comparison of Pig with Databases**

Pig and traditional relational databases (RDBMS) serve overlapping yet distinct purposes in data processing. Below is a detailed comparison to highlight their differences and strengths.

---

#### **1. Data Model**

- **Pig**:
    
    - Works with a flexible schema.
    - Supports semi-structured and unstructured data formats (e.g., JSON, XML, plain text).
    - Data is represented as tuples, bags, and maps.
- **Databases**:
    
    - Rely on a strict schema defined in advance.
    - Primarily handle structured data organized in rows and columns (tables).

---

#### **2. Processing Paradigm**

- **Pig**:
    
    - Designed for batch processing of large-scale data using Hadoop.
    - Scripts are converted into MapReduce jobs for parallel execution.
- **Databases**:
    
    - Use SQL for real-time or near-real-time querying and transaction processing.
    - Optimized for quick lookups and updates in structured datasets.

---

#### **3. Scalability**

- **Pig**:
    
    - Highly scalable due to Hadoop's distributed architecture.
    - Can process petabytes of data across a cluster.
- **Databases**:
    
    - Limited scalability, although distributed databases like NoSQL (e.g., MongoDB, Cassandra) and NewSQL improve scalability.
    - Traditional RDBMS struggle with very large datasets.

---

#### **4. Schema Flexibility**

- **Pig**:
    
    - Schema is optional and inferred during processing.
    - Handles schema-less data or datasets with evolving schemas.
- **Databases**:
    
    - Enforces a rigid schema.
    - Schema changes require migrations and can be complex.

---

#### **5. Data Processing**

- **Pig**:
    
    - Ideal for ETL (Extract, Transform, Load) tasks and complex data transformations.
    - Supports batch processing with high throughput.
- **Databases**:
    
    - Focus on CRUD operations (Create, Read, Update, Delete) and ACID transactions.
    - Efficient for ad-hoc queries.

---

#### **6. Language**

- **Pig**:
    
    - Uses Pig Latin, a high-level procedural language.
    - Easy to learn for data engineers and developers.
- **Databases**:
    
    - Use SQL, a declarative language.
    - SQL is widely adopted and has extensive support across tools and platforms.

---

#### **7. Fault Tolerance**

- **Pig**:
    
    - Provides built-in fault tolerance through Hadoop.
    - Automatically retries failed tasks and recovers from node failures.
- **Databases**:
    
    - Rely on replication and backup mechanisms for fault tolerance.
    - Failures during transactions may lead to rollbacks.

---

#### **8. Cost**

- **Pig**:
    
    - Open-source and cost-effective.
    - Can be run on commodity hardware using Hadoop.
- **Databases**:
    
    - Enterprise RDBMS solutions like Oracle or Microsoft SQL Server may be expensive.
    - Open-source alternatives like MySQL and PostgreSQL are cost-effective.

---

#### **9. Example Use Cases**

- **Pig**:
    
    - Processing and analyzing large logs for trends.
    - Cleaning and transforming data for data lakes.
- **Databases**:
    
    - Managing customer information in a CRM.
    - Real-time financial transactions.

---

### **When to Use Pig vs. Databases**

- **Pig**: Use for large-scale batch processing, ETL workflows, and handling semi-structured or unstructured data.
- **Databases**: Use for structured data, real-time queries, and transactional workloads.

### **Grunt**

Grunt is the interactive shell for Apache Pig. It is used to execute Pig Latin commands step-by-step, providing a way to debug and test scripts interactively before running them in batch mode. Grunt simplifies script development by offering immediate feedback for each command.

---

#### **Key Features of Grunt**

1. **Interactive Execution**: Grunt allows users to execute Pig Latin commands one at a time and see intermediate results.
2. **Auto-completion**: Provides command auto-completion, making it easier to navigate through scripts.
3. **Debugging**: Facilitates debugging by letting users analyze data at intermediate stages of processing.
4. **Embedded Commands**: Users can run HDFS commands directly from Grunt.

---

#### **Grunt Commands**

- **File System Commands**: Commands like `fs -ls` or `fs -rm` to interact with the Hadoop filesystem
- **Help Command**: Provides a list of available commands.
- **Execution Control**: Use commands like `run`, `exec`, and `explain` to execute Pig scripts
- **Data Exploration**: Use `dump` to view data or `describe` to display schema information.

```bash

grunt> fs -ls /data
grunt> help
grunt> exec myscript.pig
grunt> dump alias_name

```


### **Pig Latin**

Pig Latin is the scripting language for Apache Pig. It is a high-level, data flow language used to write data processing tasks that are compiled into MapReduce jobs. Pig Latin is declarative and designed for simplicity, scalability, and flexibility.

---

#### **Key Features of Pig Latin**

1. **Data Flow Language**: Describes how data is transformed through a series of steps.
2. **Handles Complex Data**: Works seamlessly with structured, semi-structured, and unstructured data.
3. **Extensibility**: Supports User Defined Functions (UDFs) for custom logic.

---

#### **Basic Syntax in Pig Latin**

1. **Loading Data**: Use the `LOAD` keyword to bring data into Pig.
2. **Transforming Data**: Apply transformations using operators like `FILTER`, `FOREACH`, and `GROUP`.
3. **Storing Data**: Save the results back to HDFS using the `STORE` keyword.

```pig

data = LOAD 'hdfs://path/to/file' USING PigStorage(',') AS (id:int, name:chararray, age:int);

adults = FILTER data BY age > 18;

STORE adults INTO 'hdfs://output/path' USING PigStorage(',');



```


### **User Defined Functions (UDFs)**

UDFs in Apache Pig allow users to extend Pig Latin's capabilities by writing custom functions. These are particularly useful for implementing complex business logic that Pig's built-in functions cannot handle.

---

#### **Creating UDFs**

1. **Language Support**: UDFs can be written in Java, Python, or other languages that support the JVM.
2. **Types of UDFs**:
    - **Eval Functions**: Process each input record and return an output (e.g., custom transformations).
    - **Aggregate Functions**: Process a group of records and return a single value (e.g., sum, average).
    - **Filter Functions**: Evaluate conditions to filter data.

---

#### **Steps to Use UDFs**

1. Write the UDF in Java or Python.
2. Compile the UDF into a JAR or script file.
3. Register the UDF in Pig Latin using the `REGISTER` command.
4. Use the UDF in Pig Latin scripts.

```pig
REGISTER 'myudfs.jar';

transformed_data = FOREACH data GENERATE myudf(name);


```

```pig

import org.apache.pig.EvalFunc;
import org.apache.pig.data.Tuple;

public class ToUpperCase extends EvalFunc<String> {
    public String exec(Tuple input) throws IOException {
        if (input == null || input.size() == 0) return null;
        return input.get(0).toString().toUpperCase();
    }
}

```


### **Data Processing Operators**

Pig Latin includes several operators that enable data transformation, grouping, filtering, and aggregation. These operators are categorized based on their functionality:

---

#### **Relational Operators**

1. **LOAD**: Loads data from HDFS or local filesystem.
2. **FILTER**: Selects rows based on a condition
3. **FOREACH**: Transforms each record in the dataset.
4. **GROUP**: Groups records by a specified field.
5. **JOIN**: Combines datasets based on a common field.


```pig
data = LOAD 'input.txt' USING PigStorage(',');

adults = FILTER data BY age > 18;

names = FOREACH data GENERATE name, UPPER(name);

grouped_data = GROUP data BY city;

joined_data = JOIN data1 BY id, data2 BY id;



```

#### **Diagnostic Operators**

1. **DESCRIBE**: Displays the schema of a relation.
2. **DUMP**: Outputs data to the console.
#### **Combining Operators**

1. **UNION**: Combines data from multiple relations.
2. **CROSS**: Creates the Cartesian product of two datasets.

```pig
DESCRIBE data;

DUMP data;

combined_data = UNION data1, data2;

product = CROSS data1, data2;


```


### **Apache Hive**

Apache Hive is a data warehouse infrastructure built on top of Hadoop for querying and analyzing large datasets stored in Hadoop's HDFS. Hive uses a SQL-like language called **HiveQL**, which is translated into MapReduce jobs for execution on Hadoop.

---

### **Hive Shell**

The Hive Shell is the primary command-line interface for interacting with Hive. Users can execute HiveQL commands, run queries, and interact with data in HDFS.

#### **Features of Hive Shell**

1. **Interactive Query Execution**: Allows users to execute HiveQL queries and commands interactively.
2. **Script Execution**: Supports running pre-written scripts stored in files.
3. **Command History**: Maintains a history of executed commands for easy access.
4. **Session Management**: Each shell instance maintains its own session, storing temporary tables and variables.

#### **Usage**

To start the Hive shell, run the following command in the terminal:
#### **Basic Commands**

1. **Show Databases**: Displays all available databases.
2. **Create Database**: Creates a new database.
3. **Use Database**: Switches to a specific database.
4. **Run HiveQL Queries**: Queries data stored in Hive.

```bash
#To start the Hive shell, run the following command in the terminal:

hive

SHOW DATABASES;

CREATE DATABASE my_database;

USE my_database;

SELECT * FROM employees;



```

### **Hive Services**

Hive architecture is modular, comprising several services that work together to provide a seamless data warehousing solution. The main services are:

#### 1. **Hive Server**

- Provides a **Thrift interface** to execute Hive queries remotely.
- Supports multiple client applications (e.g., JDBC, ODBC) for accessing Hive.
- Versions:
    - **HiveServer1**: Deprecated, provided basic query execution.
    - **HiveServer2**: An improved version with better concurrency and security.

Example usage of HiveServer2:

```pig

beeline -u "jdbc:hive2://hostname:10000/default" -n username

```

#### 2. **Hive Driver**

- Accepts HiveQL commands from the user.
- Parses the commands, plans the execution, and generates MapReduce or Tez jobs for Hadoop.

#### 3. **Hive Compiler**

- Compiles HiveQL queries into a directed acyclic graph (DAG) of MapReduce tasks.
- Ensures efficient query execution through optimization.

#### 4. **Hive Execution Engine**

- Executes the compiled queries on Hadoop.
- Supports execution on engines like **MapReduce**, **Tez**, or **Spark** for faster processing.

#### 5. **CLI (Command-Line Interface)**

- The CLI is the default interface to interact with Hive through HiveQL commands.
- It communicates with the driver and interacts with the metastore for metadata retrieval.

---

### **Hive Metastore**

The **Hive Metastore** is a critical component that stores metadata about tables, partitions, columns, and data locations. It acts as a central repository for Hive, enabling efficient query execution and data management.

#### **Key Features**

1. **Centralized Metadata Storage**: Stores metadata in a relational database (e.g., MySQL, PostgreSQL, or Derby).
2. **Schema and Table Management**: Maintains the schema of all Hive tables.
3. **Partition Information**: Tracks partitions for optimized data querying.
4. **Data Location Tracking**: Links metadata to the physical location of data in HDFS or other storage systems.

---

#### **Metastore Components**

1. **Service API**: A Thrift service used by Hive and external tools to access metadata.
2. **Backend Database**: Stores metadata in a relational database.
3. **Metastore Client**: Interacts with the Metastore API to retrieve and update metadata.

---

#### **Metastore Workflow**

1. **Metadata Registration**: When a new table is created, its schema and metadata are registered in the metastore.


```sql
CREATE TABLE employees (id INT, name STRING) STORED AS TEXTFILE;

SELECT * FROM employees;


```

#### **Metastore Configurations**

The metastore database can be configured through the Hive configuration file (`hive-site.xml`). Key properties include:

- **hive.metastore.uris**: Specifies the URI for the metastore service.
- **javax.jdo.option.ConnectionURL**: Connection string for the backend database.

### **Apache Hive Comparison with Traditional Databases**

#### **1. Architecture**

- **Traditional Databases**:
    - Centralized system designed for **transactional processing**.
    - Relational database systems (RDBMS) follow the **ACID** (Atomicity, Consistency, Isolation, Durability) model.
    - Uses structured data storage.
- **Hive**:
    - Designed for **analytical processing** of massive datasets.
    - Built on top of Hadoop and uses distributed storage like **HDFS**.
    - Not fully ACID-compliant but supports relaxed consistency for big data.

#### **2. Query Language**

- **Traditional Databases**:
    
    - Use SQL for querying and data manipulation.
    - Focus on **transactional queries** for CRUD operations (Create, Read, Update, Delete).
- **Hive**:
    
    - Uses **HiveQL**, a SQL-like query language optimized for batch processing.
    - Primarily used for **read-heavy analytical queries** with limited support for updates and deletes.

#### **3. Storage**

- **Traditional Databases**:
    
    - Stores data in structured relational tables.
    - Designed for real-time access and manipulation.
- **Hive**:
    
    - Stores data in HDFS as files (e.g., **Parquet**, **ORC**, **Text**, **Avro**).
    - Supports large-scale distributed storage with schema-on-read (data is validated during query execution).

#### **4. Performance**

- **Traditional Databases**:
    - Optimized for **low-latency transactions** with small datasets.
- **Hive**:
    - Processes **batch queries** over massive datasets using MapReduce, Tez, or Spark engines.
    - Better suited for **high-latency, large-scale analytics**.

---

### **HiveQL (Hive Query Language)**

HiveQL is the query language used in Hive. It resembles SQL but is optimized for handling large datasets in a distributed environment.

#### **Features**

1. **Data Definition Language (DDL)**:
2. **Data Manipulation Language (DML)**:
3. **Query Execution**
4. **Custom Functions**:


```sql
CREATE TABLE employees (id INT, name STRING, salary FLOAT) STORED AS TEXTFILE;

LOAD DATA INPATH '/path/to/data' INTO TABLE employees;

SELECT department, AVG(salary) FROM employees GROUP BY department;


```

### **Tables in Hive**

Hive organizes data into **databases** and **tables** for querying and analysis.

#### **Types of Tables**

1. **Managed Tables**:
2. **External Tables**:
3. **Partitioned Tables**:

- Used to divide data into partitions for better query performance.
4. **Bucketed Tables**:

- Divides data into buckets based on a hashing function.

```pig
CREATE TABLE managed_table (id INT, name STRING);

CREATE EXTERNAL TABLE external_table (id INT, name STRING)
LOCATION '/external/data/path';

CREATE TABLE partitioned_table (id INT, name STRING)
PARTITIONED BY (year INT);


CREATE TABLE bucketed_table (id INT, name STRING)
CLUSTERED BY (id) INTO 4 BUCKETS;


```


### **User Defined Functions (UDFs) in Hive**

Hive supports custom functions written in Java to extend its query capabilities.

#### **Types of UDFs**

1. **Regular UDFs**:
    
    - Perform custom transformations on data.


```pig
public class MyUDF extends UDF {
    public String evaluate(String input) {
        return input.toUpperCase();
    }
}

```


1. **Generic UDFs**:
    
    - More flexible and can handle multiple argument types.
2. **UDAFs (User Defined Aggregate Functions)**:
    
    - Custom aggregations like sum, average, etc.
3. **UDTFs (User Defined Table-Generating Functions)**:
    
    - Generate multiple rows from a single input row.

#### **Steps to Use a UDF**

1. Write and compile the Java code for the UDF.
2. Add the UDF jar to Hive.
3. Create the UDF function in Hive.
4. Use the function in a query.

```sql

ADD JAR /path/to/udf.jar;

CREATE TEMPORARY FUNCTION my_udf AS 'com.example.MyUDF';

SELECT my_udf(name) FROM employees;


```



### **HBase Overview**

Apache HBase is a distributed, non-relational database modeled after Google’s Bigtable. It runs on top of the Hadoop Distributed File System (HDFS) and is designed for real-time read/write access to large datasets.

---

### **HBase Concepts**

#### **1. HBase Architecture**

- **HMaster**:
    - The central node responsible for managing the cluster.
    - Handles metadata operations and RegionServer assignments.
- **RegionServer**:
    - Stores and manages regions (subsets of a table's data).
    - Handles read and write requests from clients.
- **Regions**:
    - Logical partitions of a table, each storing a subset of rows.
    - Regions are split when they grow too large.
- **ZooKeeper**:
    - Ensures coordination and failure recovery in the HBase cluster.

#### **2. Data Model**

- **Tables**:
    - Similar to relational tables but stored in a sparse, distributed format.
    - Rows are identified by unique row keys.
- **Column Families**:
    - Columns are grouped into families. Each family contains a set of columns.
    - Column families are defined at table creation and influence storage.
- **Cells**:
    - Intersection of a row and a column, storing data as **key-value pairs**.
- **Timestamps**:
    - Each cell is versioned with a timestamp for historical data retrieval.

#### **3. HBase Storage**

- **HFiles**:
    - Store data on HDFS in a highly efficient, column-oriented format.
- **Write-Ahead Log (WAL)**:
    - Ensures durability of writes in case of failure.

#### **4. Data Operations**

- **Get**:
    - Retrieves a single row.
- **Put**:
    - Inserts or updates data.
- **Scan**:
    - Reads a range of rows.
- **Delete**:
    - Removes data from specific rows, columns, or timestamps.

---

### **HBase Clients**

HBase provides several APIs and clients for interacting with the database:

#### **1. Java API**

- The primary method for programmatic access.
- Example for inserting data:

```java

Connection connection = ConnectionFactory.createConnection(config);
Table table = connection.getTable(TableName.valueOf("my_table"));

Put put = new Put(Bytes.toBytes("row1"));
put.addColumn(Bytes.toBytes("cf1"), Bytes.toBytes("col1"), Bytes.toBytes("value1"));
table.put(put);

table.close();
connection.close();

```

#### **REST API**

- Allows access to HBase using standard HTTP methods (GET, POST, PUT, DELETE).

#### **3. Thrift API**

- Enables lightweight, cross-language access to HBase.

#### **4. HBase Shell**

- Command-line interface for administrative tasks and querying.
- Examples:

```shell

create 'my_table', 'cf1'
put 'my_table', 'row1', 'cf1:col1', 'value1'
get 'my_table', 'row1'

```

### **HBase Example**

**Use Case**: Managing sensor data with real-time updates.

1. **Create a Table**:
2. Insert Data
3. **Retrieve Data**:
4. **Scan the Table**:

```shell
create 'sensors', 'data'

put 'sensors', 'sensor1', 'data:temperature', '25°C'
put 'sensors', 'sensor1', 'data:humidity', '60%'


get 'sensors', 'sensor1'

scan 'sensors'



```


### **HBase Versus RDBMS**

| **Feature**               | **HBase**                                              | **RDBMS**                                  |
|---------------------------|--------------------------------------------------------|--------------------------------------------|
| **Data Model**            | Schema-less, column-family-based.                      | Schema-driven, structured tables.          |
| **Scalability**           | Horizontally scalable across distributed systems.      | Vertically scalable with some limitations. |
| **Query Language**        | No native SQL, uses APIs and tools like Apache Phoenix.| SQL.                                       |
| **Storage**               | Distributed (HDFS), column-oriented.                   | Centralized or partitioned, row-oriented.  |
| **Use Case**              | Real-time analytics, IoT, and semi-structured data.    | OLTP systems like banking and retail.      |
