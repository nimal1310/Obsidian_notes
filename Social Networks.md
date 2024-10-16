## WEEK -3
### 1. Introduction
- The strength of weak ties
### 2. Granovetter's strength of weak ties
The concepts of weak ties **`highlights the importance of the reach of people's networks beyond their family and close friends `**

`Eg`: In scenario of getting job people referred by the people whom they don't know very well(strength of weak ties -not close friends).

### 3. Triads, clustering coefficient and neighborhood overlap

- Triadic closure is **` the property among three nodes A, B, and C (representing people, for instance), that if the connections A-B and A-C exist, there is a tendency for the new connection B-C to be formed`**

  ![[Pasted image 20240817040625.png]]

- **CLUSTERING COEFFICIENT**=`no of connection /total no of connection between nodes`
- clustering coefficient =
  => 1 -> all the node having connection
  => 0 ->none of the node know each other 
 - **NEIGHBORHOOD OVERLAP**
   > P(A n B)/P(A u B) 


### 4. Structure of weak ties,bridges,and local bridges

>19/08/2024

- **STRONG TRIADIC CLOSURE PROPERTY** -`if node A is connected to node B and C with strong ties, it is likely that node B and C are also connected for reasons such as opportunity, trusting and incentive`

![[Pasted image 20240819042956.png]]

- **Local bridges** are ties between two nodes in a social graph that are the shortest route by which information might travel from those connected to one to those connected to the other

### 5. Validation of Granovetter's experiment using cell phone data

### 6. Embededness 
- High embedness- strong relationship
- Always High embeddness not good.
### 7. Social Capital 
- Closure
- Brokerage

### 8.Tie Strength, Social Media and Passive Engagement
>23/08/2024
- one way communication ,maintained(passive),reciprocal.
### 9.  Betweenness Measures and Graph Partitioning
### 10. Finding Communities in a graph (Brute Force Method)
- Append -> It create nested list if two list added using append()
- Extend -> It merge the elements in the two list
- ratio ->no of intra edges/no of inter edges
- barbell graph
### 11. Community Detection Using Girvan Newman Algorithm 


## WEEK 4

### 1.Introduction to Homophily - Should you watch your company ?

Homophily is **the principle that a contact between similar people occurs at a higher rate than among dissimilar people**.

### 2. Selection and Social Influence
  - Selection -> Selecting based on the common habit they possess
  - Social Influence -> changing one's habit by influence of other (doing social service by the influence of friends) 
### 3.Interplay between Selection and Social Influence

- Similarity Measures = count of similarity / total count of items
### 4. Homophily -Definition and measurement 
- Homophily ratio =1-(actual /expected)
- actual -> actual connections b/w friends ,expected -> Expected connection
> if ratio >0 "Homophily" else "Heterogeneous(no or less no of connection )"

- heterogeneous happen only if the denominator >numerator
### 5. Foci Closure and Membership Closure
- **Foci closure** -Aka focal closure this type of connection happen due to two or more person connect with each other because of living in same place or learning in same institution (common place) Ex: school friends
- **Membership closure** - I am member of a club or institution i make my friend to join a member in the same institution.
### 6. Introduction to Fatman Evolutionary model
- The Fatman model is a model that explains how social media grows and changes over time.
### 7. Fatman Evolutionary Model- The Base Code (Adding Social Foci)
### 8. Fatman Evolutionary Model- Implementing Homophily
- greater the difference lower the probability
- lesser the difference higher the probability
### 9.Quantifying the Effect of Triadic Closure

## WEEK 5

### 1.Spatial Segregation: An Introduction
- Segregation refers to the act of separation of people from others or the main group.

- Spatial Segregation refers to the distribution of social groups or any other elements in space. In Spatial Segregation, people tend to migrate to other places where they have more neighbors who are like them.

	![[Pasted image 20240903045344.png]]              
 Locality with all different neighbors from you
 
	![[Pasted image 20240903045541.png]]
	
	he person will stay here as t =3(t=threshold which means atleast t people surrounded by same group)
### 2.Spatial Segregation: Simulation of the Schelling Model
- Schelling Model segregation website
### 3. Spatial Segregation: Conclusion
### 4. Schelling Model Implementation-1(Introduction)
- This model is used to find the notes which are satisfied with the number neighbors and which are not unsatisfied.

```python
N=10
G=nx.grid_2d_graph(N,N)
import matplotlib.pyplot as plt
nx.draw(G)
plt.show()
```

```python
# grid sturcture
pos=dict((n,n) for n in G.nodes())
nx.draw(G,pos)
plt.show()
```


### 5.Schelling Model Implementation- Visualization and Getting a list of boundary and internal nodes
 - Different types of nodes in separate list
 - Draw a graph using those different nodes list and also empty list
 - Find the boundary nodes
 - INTERNAL NODES=total nodes-boundary nodes

### 6. Schelling Model Implementation - Getting a list of unsatisfied nodes
- Find the unsatisfied nodes
### 7.Schelling Model Implementation - Shifting the unsatisfied nodes and visualizing the final graph
### 8.Positive and Negative Relationships - Introduction
### 9.Enemy's Enemy is a friend
- 1 friend and 2 hatred or 3 friends ->stable
-  2 friends and 1 hatred or 3 hatreds -> unstable
### 10 Balance theorem and proof of it

### 11.Outline of Implementation
1. create a graph with n nodes
2. connect all the possible edges and assign '+' or '-' to all the edges.
3. count unstable triangle 
### 12. Creating graph ,displaying it and counting unstable triangles.
 - nx.draw_networks_edge_labels()
 - nx.relabel_nodes()
 - nx.circular_layout()
 - user define functions
	 - get_signs_of_tris(tris_list,G)-find the sign between each nodes in every possible triagles  
		  - tris_list=[[1,2,3,]]
		  - all_signs=[['+','-','+']]
	 - count_of_stable()
		 - count("+")== 1 or 3 -> stable
		 - count("-")== 1 or 3 -> unstable
- *Inverting the sign of any one edges will make the triangle stable*
### 13.Forming two coalitions
- *A coalition is formed when two or more people or groups **temporarily work together to achieve a common goal.***
- `Ex`: In political this term coalitions mostly used two different parties were joined together to do achieve a goal.
- 

## week 6
### Collecting web graph,Equal coin distribution,Random coin Dropping

- Equal coin distribution = Random coin dropping 
- Google page rank algorithm - it increase the count of gold coin based and marked it as highest
	`Ex:` In google search each website assign with rank based on most visited by users Based on the rank the result display on the web page once the user search with a keyword.
- Random walk method for page rank - work on directed graph
-  Page rank vs Degree rank
	- Pagerank()  

## Week 7

## 
