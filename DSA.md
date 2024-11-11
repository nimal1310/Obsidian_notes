## Dynamic programming:
- It is used to solve complex problems by breaking into small subproblems and store result in each stage to avoid redudants.
- USES
	 - Optimal Substructure
	 - Overlapping subproblems
- APPROACHES
	 - Top-Down (memoization) ->start with final solution and recursively solve it
	 - Bottom-Up (tabulation) ->start with smallest subproblems and gradually build the final result.
### Problem

```python

## Normal recursive method
def fibo(n):
	 if n<=1:
		 return n
	 else:
		 return fibo(n-1)+fibo(n-1)
if __name__=='__main__':
	n=10
	print(fib0(5))
```


- MEMOIZATION

```python
  Fibo=[]
  def fibo(n):
	  if n in Fibo:
		  return Fibo[n]
	  elif n<=1:
		  res=n 
	  else:
		  res=fibo(n-1)+fibo(n-2)
	  Fibo[n]=res
	  return res
 n=10
 print(fibo(n))

```

--- 
---
- Built in DS - list,tuples ,dictionaries , String
- User define DS  - Linked list,tree and Graph


### LIST :
- Ordered collections of arrays(which follow a specific order)
- Collections of different datatypes inside a list
- Allow duplicates
- *Insertion and deletion in an array are costly*
- Operations on list 
	- Creation ,Insertion,deletion and selection  

```Python
#LIST CREATION
list1=[1,2,'ordered',['allow duplicate']]

#using constructor

list2 =list((1,3.14,'constructor'))

#list with * operator

list3= [2]*5
list4=['s']*5

#ACCESSING ELE IN LIST
a=list1[3]
b=list2[1]

#MODIFYING LIST(append ,extend ,insert(idx,ele))
new_list=[]
new_list.append(5)
new_list.insert(0,10)
new_list.extend([20,15])
new_list.append([30,25])

print(new_list)

#UPDATE ELE IN LIST
list1[1]=3.14
print(list1)

#REMOVING ELE IN (remove,pop,del)
#remove the first occurence of an element
list1.remove(1)
list2.pop(2)
del list3[4]

print(list1,list2,list3)
```


### SET 
- It wont allow duplicate
- It is unordered 
- It is mutable ,it is used in membership testing
- Set were created using `hash table` data structure.

```Python

#CREATION
set1={1,'not allow duplicate','unordered',3.14}
set2=set([1,'hash table',2,True])
print(set1,set2)

#IMMUTABLE set1[0]=2 not possible
#ADDING ELE IN A SET

set1.add('new ele')

#frozen set are specific kind of set that wont allow for modification of set after it was created

#UNION OF SETS(| or union)
set_union=set1.union(set2) #set1 |set2
print(set_union)
#INTERSECTION
set_intersection=set1&set2 # set1.intersection(set2)
print(set_intersection)
#DIFFERENCE
set_diff=set1 -set2 # set1.difference(set2)
print(set_diff)

#CLEARING A SET
set1.clear()
print(set1)
```

### DICTIONARY 
- Unordered collection of data
- Mutable 
- <key,value > pair 

```Python
#CREATING A DICT
dict1={'name':'nimal','age':21}
print(dict1)
dict2=dict([('char1',"mutable"),("char2","unordered"),(1,'number')])
print(dict2)

#ADDING ELE IN DICT
dict3={}
dict3[0]=1
dict3['value']=1,2,2,3
print(dict3)

#NESTED DICT
new_dict={'D1':dict1,'D2':dict2}
print(new_dict['D1'])

#UPDATING DICT
dict3[0]='index zero'
print(dict3)
print(dict3.get('value'))

#ACCESS ELE IN DICT
print(dict1['name'])
print(dict3['value'][0])

#DELETING DICT
del(dict1)
del(dict2['char1'])
```

*Different operations*
- dict.clear()
- dict.copy()
- dict.items()  [(k1,v1),(k2,v2)]
- dict.keys()
- dict.values()
- pop() - remove element with specific key
- popItem() -remove the last added key,value
- dict.has_key() -check for particular key
--- 

### TUPLE:
- It is similar to list but its is immutable
- It allow duplicate and Ordered
- We cant append or extend in tuple and also cant remove items once it is created

```Python
#CREATING A TUPLE
tup1=('a','b')
tup2=(1,2,3.14)
print(tup1,tup2)
tup3=tup1+tup2
print(tup3)
nested_tup=tuple((tup1,tup2))
print(nested_tup)

print(tuple('string'))
#('s', 't', 'r', 'i', 'n', 'g')
  
#ACCESSING VALUES(- and + indexing)
print(tup1[0],tup2[-1])
#SLICING
print(tup1[0:])
#DELETION
del tup1
```


### STRING:
- It is immutable array of bytes
- It doesn't have char type so a single char consider as string with length 1.
```Python
#CREATION OF STRING
string1="creation of string"
string2='''string with "double qoutes"'''
print(string2)

#ACCESSING CHARACTER IN STRING
print(string1[0])
print(string1[::-1])
r="".join(reversed(string1))
print(r)

#UPDATION OF LIST
l=list(string1)
print(l)
l.append('s')
print(l)
string1=''.join(l)
print(string1)
string2="updated string"
print(string2[0:3])

#DELETION OF STRING
del string1
# print(string1)
rs=10
print(f"the value of pen is {rs:.3f}")
print("{} {k} {g}".format('hello',k='i am',g='nimal'))
print("{1:.2f}".format(9/2,3/2))
```

### LINKED LIST:

- It is a linear data structure.
- It contain two parts (data,Reference or next address)
```Python
class Node:
	def __init__(self,data):
	
		self.data=data
		self.next=None

class Linkedlist:

	def __init__(self):

		self.head=None
	def printlst(self):

		temp=self.head

		while(temp):
		
			print(temp.data)
			temp=temp.next

if __name__=='__main__':
	llist=Linkedlist()
	llist.head=Node(1)
	second=Node(2)
	third=Node(3)
	
	llist.head.next=second
	print(llist.head.next)
	second.next=third
	llist.printlst()
```

### STACK 
- It follow `FILO` or `LIFO` 
- Methods:
	- empty(),size(),top(),push(),pop()

### QUEUE
- It follow `FIFO` or `LILO`
- It is a linear data structure.
- Methods:
	- Enqueue - add the element at the last
	- Dequeue - remove the element from the queue.
	- Front ,Rear

### PRIORITY QUEUES:
- It is a abstract data structure
- It has data/value with certain priority
- Priority queue is an extension of the queue it *dequeue the element with highest priority first and if 2 ele have same priority they serve according to order*

### HEAP:
- heapq provides the head data structure that mainly used to represent a priority queue.
- Property:
	- Always pop the smallest element and heap[0]  is always smallest
	- max-heap - key value of root node is always max 
	- min-heap - key value of root node is always min 
### BINARY TREE 
- It is hierarchical data structure.
- It has top node as root node ,bottom node as leaf node and intermediate node as parent nodes.
- Binary tree have at most two children(left and right children).
	- Data ,pointer to left child and pointer to the right child.

### TREE TRAVERSAL 
-  In-order (Left,Root,Right)
- pre-order(root,left ,right )
- post-order(Left,right,root)

### BINARY SEARCH 
- It is node based data structure.
- It is based on binary tree data structure.
- It has 2 elements left and right child .It has lesser value in left subtree and greater value in right subtree.

### GRAPH 
- It is non linear data structure consisting of nodes and edges.
- Nodes is aka vertices and edges are lines or arc that connect any two node in the graph.
	- Adjacency matrix (It contain matrix V x V contain the edges detail.)
	- Adjacency list (It contain array of value)

### DFS & BFS 
| Parameters            | BFS                                                                                                                                                                                | DFS                                                                                                                                                                                                                      |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Stands for            | BFS stands for Breadth First Search.                                                                                                                                               | DFS stands for Depth First Search.                                                                                                                                                                                       |
| Data Structure        | BFS(Breadth First Search) uses Queue data structure for finding the shortest path.                                                                                                 | DFS(Depth First Search) uses Stack data structure.                                                                                                                                                                       |
| Definition            | BFS is a traversal approach in which we first walk through all nodes on the same level before moving on to the next level.                                                         | DFS is also a traversal approach in which the traverse begins at the root node and proceeds through the nodes as far as possible until we reach the node with no unvisited nearby nodes.                                 |
| Conceptual Difference | BFS builds the tree level by level.                                                                                                                                                | DFS builds the tree sub-tree by sub-tree.                                                                                                                                                                                |
| Approach used         | It works on the concept of FIFO (First In First Out).                                                                                                                              | It works on the concept of LIFO (Last In First Out).                                                                                                                                                                     |
| Suitable for          | BFS is more suitable for searching vertices closer to the given source.                                                                                                            | DFS is more suitable when there are solutions away from source.                                                                                                                                                          |
| Applications          | BFS is used in various applications such as bipartite graphs, shortest paths, etc. If weight of every edge is same, then BFS gives shortest pat from source to every other vertex. | DFS is used in various applications such as acyclic graphs and finding strongly connected components etc. There are many applications where both BFS and DFS can be used like Topological Sorting, Cycle Detection, etc. |

### RECURSION:
- When any function is called from main(), the memory is allocated to it on the stack. A recursive function calls itself, the memory for a called function is *allocated on top of memory allocated* to the calling function and a *different copy of local variables is created* for each function call. When the base case is reached, the function returns its value to the function by whom it is called and memory is de-allocated and the process continues.
### DYNAMIC PROGRAMMING:
- It is mainly used to optimize the recursion solution for a problem by storing the solution in each stage and use it for later when needed.
- TABULATION
	- It is bottom-up approach.
	- It start with base state and reached the topmost desired state.
- MEMOIZATION:
	- It is top-down approach
	- It is start form state dp[n] and instead of starting from the base state that is dp[0]

### SEARCHING ALGORITHM:
- Linear search - O(n)
- Binary search - O(log(n))

### SORTING ALGORITHM 

1. IN-PLACE SORTING 

- **Selection sort** 
	- It work on unsorted array .It find the  minimum element from the unsorted array and move it to beginning.
	- $Time complexity: O(n^2)$
	- $Space complexity: O(1)$
	
	
- **Bubble sort**
	- It sort the array by repeatedly swapping the adjacent element in wrong order
	- $Time complexity : O(n^2)$

- **Insertion Sort**
	- It iterate from 1 -> n over the array.
	- Compare the current key to predecessor if key < predecessor move the predecessor to one position front and make space for smaller element.
- **Shell sort**
	- It is a variation of insertion sort.
	- It allow to exchange of far items.
	- An array is said to be h-sorted if all sublists of every hth element is sorted.
	- $Time Complexity:O(n^2)$
- **Heap sort**
	- It is a comparison based sorting algorithm based on binary heap data.
	- It  first convert the array into max heap using `heapify`.
	- remove the top element which is the maximum element.
	- repeat the process until the heap is empty.
	- $O(nlogn)$


2. NOT IN-PLACE SORTING:

- **Merge sort**
	- Divide and conquer.
	- It divide the array into two halves and then merge the two sorted halves
	- $Time complexity : O(n(logn))$
- **Quick sort**
	- It is also divide and conquer algorithm.
	- It select the pivot element and partition the array and place the smallest value at left and largest value at the right.
	- It select the pivot element 


---
---

###   OOPS CONCEPTS 


**Purpose** 
- It is used by the developers to build modular,maintainable ,scalable applications.

**OOPS concepts**
- Classes and objects
- Inheritance 
- Polymorphism
- Encapsulation
- Abstraction

**Benefits**
- Scalability 
- Re usability 
- Efficiency 

`Ex:`
 - It is used in a manufacturing system simulation s/w.

## Class:
- Class is a collection of objects.
- It is prototype or blueprints and its is a logical entity that contains some *attributes and methods.*
- Attribute are variables that can be accessed by objects.

```Python
class Dog:
	method definition
```

## Objects:
- It is an real world entity that has a state and behavior associated with it.
- It may be any real-world object like a mouse, keyboard, chair, table, pen, etc. Integers, strings, floating-point numbers, even arrays, and dictionaries, are all objects.
- It consists of *state,behavior and identity*.
- `Ex` Switch is a object the has the behavior turn on and off.

- **Self** - extra argument need to be specify in the class methods.
- **__init__** - It is constructor in python similar to c++ and java.

```Python
class torchlight:
	def __init__(self,a):
		self.name=a
	
	def on(self):
		print(f"{self.name} turned on.")
	
	def off(self):
		print(f"{self.name} turned off.")

switch=torchlight('Bulb A')
switch.on()
switch.off()
```

**Instance class** - the value of variable assigned inside the constructor.

```Python

class Dog:
	animal = 'dog'

	def __init__(self, breed):
		self.breed = breed
	
	def setColor(self, color):
		self.color = color
	
	def getColor(self):
		return self.color

Rodger = Dog("pug")
Rodger.setColor("brown")
print(Rodger.getColor())
```


## Python Inheritance:
- Inheritance is the capability of one class to derive or inherit the properties from another class.
- Base class or parent class contain properties which derived to child class.
- A child class can also modify the behavior of the parent class as seen through the details() method
- Types:
	- *Single inheritance* - single parent-child relationship
	- *Multilevel inheritance* - a child inherit from parents which in turn inherit from his parent class.
	- *Hierarchical inheritance* - More than one class inherit from one base class
	- *Multiple inheritance* - One derived class inherit from more than one base class.

![[Pasted image 20241031144522.png]]


## Encapsulation:

- Encapsulation is a process of hiding the information or data from unauthorized user by using convention instead of access specifier(private,protected) used in c++,java.
- It is a process of wrapping data and the methods that work on data within one unit.
- It restrict access of variable within the method.It prevent **accidental changes like deletion,modification of data**
- It allow modification on variables (private variable ) only by using the `object methods`.
```python

class Tree:
   def __init__(self, height):
       self._height = height

pine = Tree(20)
pine._height  # 20

#private member

class Tree:
   def __init__(self, height):
       self.__height = height


pine = Tree(20)
pine.__height ## AttributeError: 'Tree' object has no attribute '__height'

## It can only accessed by object methods.

class Tree:
   def __init__(self, height):
       self.__height = height

   def get_height(self):
       return self.__height

   def set_height(self, new_height):
       if not isinstance(new_height, int):
           raise TypeError("Tree height must be an integer")
       if 0 < new_height <= 40:
           self.__height = new_height
       else:
           raise ValueError("Invalid height for a pine tree")


pine = Tree(20)
pine.get_height()  # 20



```

## Polymorphism:

- It is used to represent different data by using same function name but variable size of signature or parameters.
- We define a `Logger` class, then create different loggers based on where we want to store the logs. This allows us to change logging behavior as needed without modifying the core application.
- It has two types *Compile time and run time*
- Compile time 
	- object bound to its method during compilation
	- Static or early binding
	- method overloading
- Run time
	- in which the object bound to method during runtime
	- Dynamic or late binding.
	- method overriding

## Abstraction:

- It hides unnecessary and internal functionalities from users and provide access to helpful information.
- User aware of `what a function does` without knowing `how it does it`
- Hide sensitive implementation details, like password encryption, from the rest of the application.we create a private method `__encrypt_password` that’s only used internally.
- Class without implementation is called *abstract class*

- `Example` 
	- In a banking application, abstraction helps define a clear structure and set of operations that different bank account types (like Savings, Checking, and Fixed Deposit) must adhere to, while allowing each account type to implement those operations in a specific way

```python

from abc import ABC, abstractmethod

# Abstract base class for all bank accounts
class BankAccount(ABC):
    def __init__(self, account_number, balance=0):
        self.account_number = account_number
        self.balance = balance

    @abstractmethod
    def deposit(self, amount):
        """Deposit a certain amount into the account."""
        pass

    @abstractmethod
    def withdraw(self, amount):
        """Withdraw a certain amount from the account."""
        pass

    def check_balance(self):
        """Check current balance."""
        return f"Account {self.account_number}: Balance is {self.balance}"

# Concrete class for a Savings Account
class SavingsAccount(BankAccount):
    def deposit(self, amount):
        self.balance += amount
        return f"Deposited {amount} to Savings Account {self.account_number}"

    def withdraw(self, amount):
        if amount > self.balance:
            return "Insufficient funds"
        self.balance -= amount
        return f"Withdrew {amount} from Savings Account {self.account_number}"

# Concrete class for a Checking Account
class CheckingAccount(BankAccount):
    def deposit(self, amount):
        self.balance += amount
        return f"Deposited {amount} to Checking Account {self.account_number}"

    def withdraw(self, amount):
        if amount > self.balance:
            return "Insufficient funds"
        self.balance -= amount
        return f"Withdrew {amount} from Checking Account {self.account_number}"

# Testing the application
savings = SavingsAccount(account_number=12345, balance=1000)
checking = CheckingAccount(account_number=54321, balance=500)

print(savings.deposit(200))       # Deposited 200 to Savings Account 12345
print(savings.withdraw(500))      # Withdrew 500 from Savings Account 12345
print(savings.check_balance())    # Account 12345: Balance is 700

print(checking.deposit(300))      # Deposited 300 to Checking Account 54321
print(checking.withdraw(1000))    # Insufficient funds
print(checking.check_balance())   # Account 54321: Balance is 800

```

---
---
# DBMS


## Entity Relational Model:

- The **Entity-Relationship (ER) Model** is a high-level conceptual data model used to define the structure of data within a database.
- *Entities*
- *Attributes*
- *Relationships*
- *ER Diagram*
- *ER Diagram*: A diagrammatic representation of entities, attributes, and relationships, usually represented by rectangles (entities), ovals (attributes), and diamonds (relationships).

1. Recursive relationship - Relationship b/w two entity of similar entity type
2. Impedance mismatch - the problem that arises when two systems or components that are supposed to work together have different data models, structures, or interfaces that make communication difficult or inefficient.
	`ex:` *impedance mismatch refers to the discrepancy between the object-oriented programming (OOP) model used in application code and the relational model used in database management systems (DBMS).*
## Relational model

- The **Relational Model** organizes data into tables (relations) with rows and columns. Each table has a unique name and holds data on a particular entity type.
- **Table (Relation)** 
- **Tuple (Row)**
- **Attribute (Column)**
- **Schema**
## Relational Algebra
- It is a procedural Language. It consists of a set of operators that can be performed on relations.
- Relational algebra has mainly 9 types of operators.

- [UNION](https://www.geeksforgeeks.org/union-c/)
- [INTERSECTION](https://www.geeksforgeeks.org/sql-intersect-clause/)
- [MINUS](https://www.geeksforgeeks.org/sql-minus-operator/)
- [TIMES](https://www.geeksforgeeks.org/concept-of-time-in-database/)
- [SELECTION](https://www.geeksforgeeks.org/difference-between-selection-and-projection-in-dbms/) In general SELECT operation is denoted by (σ)(R)
- [PROJECTION](https://www.geeksforgeeks.org/difference-between-selection-and-projection-in-dbms/) It displays some specified columns in a relation. “π”
- [JOIN](https://www.geeksforgeeks.org/sql-join-set-1-inner-left-right-and-full-joins/)
- [DIVISION](https://www.geeksforgeeks.org/sql-division/)
- [RENAME](https://www.geeksforgeeks.org/sql-alter-rename/)  It gives another name to the relation.****(ρ)****
## Codd’s Rules in DBMS

- *It is used to maintain the integrity ,usability ,security of the data in the database*
- *Totally 12 rules*
	- The Foundation Rule
	- Information Rule
	- Guaranteed Access Rule
	- Systematic Treatment of Null Values
	- Active/Dynamic Online Catalog based on the relational model
	-  Comprehensive Data SubLanguage Rule
	-  View Updating Rule
	- High-Level Insert, Update and delete
	- Physical Data Independence Rule
	- Logical Data Independence Rule
	- Integrity Independence Rule
	-  Distribution Independence Rule
	-  Non-submersion rule 

## Functional Dependency:

- A **Functional Dependency** is a constraint between two sets of attributes in a relation from a database
- STUD_NO->STUD_NAME, STUD_NO->STUD_PHONE *hold*
- STUD_NAME->STUD_STATE *do not hold*
- **Types of Functional Dependencies**:

	- **Trivial FD**: A→A or any subset of `A`.
	- **Non-trivial FD**: When A→B, but B is not a subset of `A`.
	- **Multivalued Dependency**: When one attribute determines multiple values of another attribute independently.

- **Attribute Closure** Attribute closure of an attribute set can be defined as set of attributes which can be functionally determined from it.
- Attributes which are parts of any candidate key of relation are called as prime attribute, others are non-prime attributes
## Armstrong axioms:
- It contain set of rules or axioms to determine the functional dependency or logical implication of data.
- **Axiom of Reflexivity**
- **Axiom of Augmentation**
- **Axiom of Transitivity:**

- ### Secondary Rules
- **Union** If **X→Y**and **X→Z** then **X→YZ**
- **Composition:**
- **Decomposition:**
- **Pseudo Transitivity:** If **A→B** holds and **BC→D** holds, then **AC→D** holds. If **X→Y** and **YZ→W**then **XZ→W**
- **Self Determination:** It is similar to the Axiom of Reflexivity, i.e. **A→A** for any A.
- **Extensivity:** Extensivity is a case of augmentation. If **AC→A,** and **A→B** then **AC→B**. Similarly, **AC→ABC** and **ABC→BC** This leads to **AC→BC**.

## Normalization 

- It is used to reduce the redudancy of the data and avoid the anomalies in the data.
- 1NF,2NF,3NF, BCNF, 4NF &5NF
## Transaction and Concurrency Control

**Transaction**:
- A set of logically related operations is known as a transaction.
- Read(A) & Write(A)
- **Properties of transactions**
	- Atomicity -As a transaction is a set of logically related operations, *either all of them should be executed or none*
	
	- Consistency - execution of concurrent operation like read and write lead to consistency. write before read.
	
	- Isolation -The result of a transaction should not be visible to others before the transaction is committed
	
	- Durability - Once the database has committed a transaction, the changes made by the transaction should be permanent.

**Schedule**
- A schedule is a series of operations from one or more transactions. A schedule can be of two types
- *Serial and concurrent*


**Concurrency Control in DBMS**

- simultaneous execution or manipulation of data by several processes or user without resulting in data inconsistency
- The fundamental goal of database concurrency control is to ensure that concurrent execution of transactions does not result in a loss of database consistency.
- **Concurrency Control Problems**
	- Dirty read problem(write -read conflict)
	- Lost update Problem
		- Lost update problem occurs when two or more transactions modify the same data, resulting in the update being overwritten or lost by another transaction
	
- **Concurrency controls protocols**

	- Locked based concurrency control protocol
	
		- shared lock -read lock(allow only read)
		- exclusive lock - write lock(allow only to write)
		- **Two Phase Locking Protocol**
		- **Strict Two Phase Locking  Protocol**
	
	- Timestamp based concurrency control protocol
	
		- In this protocol each transaction has a [timestamp](https://www.geeksforgeeks.org/timestamp-based-concurrency-control/) attached to it. Timestamp is nothing but the time in which a transaction enters into the system

- **Starvation** or Livelock is the situation when a transaction has to wait for an indefinite period of time to acquire a lock.