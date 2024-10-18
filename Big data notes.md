
- ## Unit-1 introduction to big data & hadoop

>Big data -concepts, needs and challenges, types and sources of big data, History of Hadoop, Apache Hadoop,
Analyzing
Data with Unix tools, Analyzing Data with Hadoop, Hadoop Streaming, Hadoop Echo System, IBM Big Data
Strategy, Introduction to Infosphere Big Insights and Big Sheets

- **Big data**
	- *Big Data refers to large and complex data sets that traditional data processing applications cannot handle effectively. It involves capturing, storing, analyzing, and managing vast volumes of structured, semi-structured, and unstructured data.*
	- ` Needs` : To extract the meaningful information from larger amount of data.
	- `Challenges` : Data storage,processing speed ,data privacy.
	
- **Types and source of big data**
	- 4 types of data mainly 3
		1. structured
			- Aka relational data
			- Rows and columns ,spreadsheet.
			- Need sql query
			- *Excel sheets*
			
		2. unstructured
			- Aka dark data
			- *Audio,video,text documents,log files*
			
		3. semi-structured
			- Don't follow proper format but it has some structure key-value pairs.
			- It use data serialization language
			- *Json,xml,audio and zip file*
		4. streaming data
			- Continuous data streams generated in real-time from various sources, such as sensors, IoT devices, and social media feeds.
	- Source of big data:
		- Social media,sensor data,transaction data,machine data,public data.
- **History of hadoop**
- **Apache Hadoop**
	- Apache Hadoop is an open-source software framework used for distributed storage and processing of large datasets across clusters of computers.

- **Analyzing Data with Unix Tools**
	- *Unix provides command-line tools like `awk`, `sed`, and `grep` to process text data and perform basic data analysis tasks like filtering, sorting, and searching.*
	
- **Analyzing data with hadoop**
	- Map reduce work by breaking the processing into 2 phases
	- map phase and reduce phase
	>INPUT(year ,air temperature)
	(1950, 0)
	(1950, 22)
	(1950, −11)
	(1949, 111)
	(1949, 78)
	
>OUTPUT (map reduce)
>
>(1949, [111, 78])
(1950, [0, 22, −11])

![[Pasted image 20241018205505.png]]

- **Hadoop Streaming**
	- Hadoop Streaming is a utility that allows users to create and run MapReduce jobs with any executable script or program that reads input from `stdin` and outputs to `stdout`.
	- TYPES:
		- Map function 
		- Reduce function
	- Classification:
		- Custom streaming (custom code for map reducer)
		- Pre-built streaming
	- Methods:
		- Input/output stream
		- Flexible map reduce
	- Application:
		- Log processing
		- Text mining
		- Data transformation

```python 
#Map function

#!/usr/bin/env python3
import sys

# Input comes from standard input (stdin)
for line in sys.stdin:
    # Remove leading and trailing whitespace
    line = line.strip()
    # Split the line into words
    words = line.split()
    # Emit each word with a count of 1
    for word in words:
        print(f"{word}\t1")


```

```python

# Reducer function
#!/usr/bin/env python3
import sys

current_word = None
current_count = 0
word = None

# Input comes from standard input (stdin)
for line in sys.stdin:
    # Remove leading and trailing whitespace
    line = line.strip()
    # Parse the input we got from mapper.py (word \t count)
    word, count = line.split('\t', 1)

    try:
        count = int(count)
    except ValueError:
        # Ignore lines where count is not an integer
        continue

    # This is the first word we encounter
    if current_word == word:
        current_count += count
    else:
        if current_word:
            # Output the current word and its count
            print(f"{current_word}\t{current_count}")
        current_word = word
        current_count = count

# Output the last word if needed
if current_word == word:
    print(f"{current_word}\t{current_count}")

```

- **Hadoop Eco-system**
	- It consists of various tools & framework to extends the capability of hadoop to handle diverse tasks,from data storage to real-time analytics.
	- Components:
		- HDFS 
		- YARN
		- MAP REDUCCE
	- supporting tools
		- Hbase
		- Hive(query language)
		- pig (scripting language that simplifies complex data transformations.)
		- Sqoop- allow data transfer between Hadoop and relational database.
		- Oozie- job scheduler in hadoop
		- Flume - it used to ingest streams of log data into hadoop.

	- Classification
		- Data storage
		- Data processing
		- Data ingestion
	- Applications:
		- Retail - customer pattern identifications
		- Financial services - fraud detection


- **IBM big data strategy**
	- IBM's Big Data Strategy involves a comprehensive set of tools and platforms to store, manage, and analyze large datasets, aimed at solving business problems
	- KEY PILLARS:
		- Data volume
		- Data variety
		- Data Velocity
		
	- IBM Big data tools:
		- *IBM Infosphere* :A platform offering data integration, data warehousing, and analytics tools to manage Big Data.
		- *IBM big Insights* : Built on Apache Hadoop, this tool helps process and analyze Big Data in a Hadoop environment.
		- **IBM stream** : A real-time processing platform designed to analyze data in motion.
	- **Applications**:
		- Retail
		- Health care
		- Financial services
		
	- **IBM approach:**
		- Holistic data Management : 
			- different data Management systems to unified one
		- Cloud and AI : 
			- It combine cloud and AI to analysis big data.


- **Introduction to Infosphere Big insights and big sheets**
	- Big Sheets is a tool within Big Insights used for data exploration and visualization, offering a spreadsheet-like interface to analyze unstructured data.



## Unit 2 HDFS (Hadoop Distributed File System)

>The Design of HDFS, HDFS Concepts, Command Line Interface, Hadoop file system interfaces, Data flow, Data
Ingest with Flume and Scoop and Hadoop archives, Hadoop I/O: Compression, Serialization, Avro and File-Based
Data structures. Anatomy of a Map Reduce Job Run, Failures, Job Scheduling, Shuffle and Sort, Task Execution, Map
Reduce Types and Formats, Map Reduce Feature


- Introduction to HDFS:
	- What is HDFS
	- Key Features of HDFS
	
		- Distributed storage
		- Fault tolerance
		- High Availability
		
	-  Architecture of HDFS
	
		- NAME NODE:
		
			-  It is master
			- It knows where every block of data is stored
			- HDFS will not be available if name node goes down.
			
		- DATA NODE
			- It is worker node that store the actual data.
			- Follow the instruction of name node.
			
		- REPLICATION
			- HDFS keep 3 copies of each block of data by default
			- It ensure the reliability and fault tolerance.
		
	- Data Access in HDFS:

		- If client want to access data it request name node and redirect the client to Corresponding data node.
		
	- Scalability:
		- Horizontal scalability
		- As data grown more machines can be added to the systems.
		
	- Write-Once ,Read-Many
