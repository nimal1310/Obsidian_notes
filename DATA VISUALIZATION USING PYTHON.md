

> **Unit -1**
> Introduction-Classification of Visual Data Analysis Techniques-Data Type to be Visualized-Visualization Techniques-
Interaction Techniques-Specific Visual Data Analysis Techniques 

# UNIT-1 VISUALIZATION

- **What is data visualization ?**
	- It is art and science combined -where the power of analysis meet the beauty and design.
  
- **why data visualization ?**
	- To gain insight
	- Provide quality overview 
	- Help to find the interesting region and suitable parameters and visual proof.
	- It help to find the patterns,outliers and trends in data.

- **Uses of data visualization**
	 - Simplifying the complex data
	 - Identifying the patterns and trends
	 - Facilitating comparisons
	 - Enhancing communication
	 - Aiding in decision making
- **Types of Dataset**
	- Record data(Row & Col ,Documents)
		- relational data ,data matrix,transaction data
		- Field-value pairs(json,bson and xml)
	- Graph and Networks
		- molecular structure ,www,transportation network ,social network
	- Ordered data(sequence or continuous data)
		- Video data ,time series data ,genetic sequence data
	- Spatial ,image ,multimedia data(maps ,image ,video data)
- **Important characteristics of structure data**
	- Dimensionality ,sparsity,resolution and distribution

- **Data Objects** 
	- It is represented as entity
	- Data object are described by attributes
	- It is rows value present in table
- **Attributes**
	- It is the column or features or dimension or variable present in table  `Eg:` name ,address
	- Attributes types - Nominal ,Binary,ordinal
	- Numeric attributes - Interval ,ratio
	- Discrete vs Continuous attributes
- **Visual data mining**


## Classification of visual data analysis techniques:

- It has been done based 3 criteria 
	- The data type to be visualized 
	- The visualization techniques
	- The interaction techniques used

1. **Data type to be visualized:**
	- 1D,2D, 
	- Multidimensional data(satellite photography ,topography maps ,GPS)
		1. Parallel coordinates(*each variable represent by vertical axis  and each data points show as line that connects across the axes* )
		2. Scatterplot matrix(pair plot) - Different scatter plots are formed as a matrix
		3. Heat map and Dendrogram 
		4. Dimensionality reduction
		5. Radial plot
	
	- Text and Hypertext 
		1. Text is linear ,sequential information presented in structured format(linear flow - st.line)
		2. Hypertext is Non linear information represented in different pathway(network visualization)
	
	- Hierarchies and graphs (Telephone call is hierarchy in nature.It stored in tree like structure parent- child relationships.)
		1. Hierarchies -Tree map 
		2. Graph - Network visualization
	
	- Algorithms and S/W. 
		- It is used to visualize the flow of code useful for changes and corrections
			 1. flowchart ,pseudo code ui mockup ,architecture diagram


2. **Visualization techniques:**
	- Standard 2D or 3D displays 
		- 2D - line,bar,histogram,box,scatter plot
		- 3D - Surface,volume,network plot
	
	- Geometrically  transformed displays
		- Direct data visualization (*It is technique for analyzing image data using method like the slice histogram and growing entourage plot* )
		- Multidimensional scaling and PCA
		- Scatter plot matrices
		- Landscapes
- 
	- Icon based displays
		1. Data points are represented as icon of small graphical elements instead of points or bars.It is useful in visualize the multivariate data.
		2.  *chernoff faces ,stick figures ,star glyphs(radar charts) color icons and tilebars*
	
	- Dense pixel displays
		- The idea is to map each dimension values to a colored pixel and group the pixel belong to each dimension into adjacent areas.
		- Mapping each data point to a small pixel in a grid.
			1. Heat maps
			2. Recursive pattern techniques
			3. Circle segment techniques
	
	- Stacking displays
		- It involves  layering different visual elements to represent multiple dimensions of data in a single display ,make easier to compare different set of data
			1. Dimensional stacking 
			2. Worlds within worlds
			3. Tree map - partition the screen based on the attributes values
			4. Infocubes - 3D visualization techniques where hierarchical information is displayed as nested semi-transparent cubes
			5. 3D cones tree - It work well on thousands of nodes or so . 1st build 2D circle tree that arranges its nodes in concentric circles center on the **root node**



1. **Interaction techniques**
	- Dynamic Projection
		- It refers to the ability to interactively change the projection or perspective of data ,allowing user to explore different view or pattern in high dimensional data.
		- *PCA projection and scatter plot matrix.*
	
	- Interactive filtering 
		- Allow users to refine or narrow down the data displayed by applying filter,highlighting specific subsets of interest while excluding others
		- *Range slider and Brushing*
		- TOOLS: Magic tools ,infocrystal ,Dynamic queries & polaris.
	
	- Zooming 
		- Zooming allows users to explore different levels of details in a dataset by zooming in area of interest and zooming out to see a broader context.
		- It allow users to see the dataset at different resolution.
		- *Semantic zoom and Geometric zoom*
		- TableLens , PAD++,IVEE/spotfire ,dataspace\
	
	- Distortion
		- It modify the visual representation of data to emphasize certain areas of interest while still maintaining an overall view of the data.
		- To shows portions of the data with a high level of detail while others are shown with a lower level of detail.
		- Tech : *Hyperbolic and spherical distortion.*
	
	- Linking & brushing  
		 1. Combine different visualization scatterplot,bar chart ,parallel coordinates ,pixel displays and maps.
		 2. Changes made in one visualization reflect in other visualization also with linking.
		 3. Brushing means selecting a subset of data items with an input device.
		 4. *Scatter plot & parallel coordinates ,Geographical and statistical views*
		 5. Systems : S+ ,XGobi ,XmdvTool and datadesk
	
## Specific visual data analysis techniques:
- Associations rule generation
- Classification
- Clustering


	 1. **Association rule generation**
		 - It is used to find the interesting patterns and trends in transaction database.It is data mining techniques used to find the relationship between different variable in large datasets.
		 - It find the relationship between two or more items.
		 - `Eg:` association rule in super market basket scenario 70% of customers who buy bread also purchase milk.
		 - Key concepts 
			 1. **Confidence** : It is ratio of the number of transactions that contains both items to the number of transactions of that contain the first item.Measure of strength b/w two items.
			 2. **Support** : The % of transaction in which the items co-occur.
		- Types of Association rule:
			1. Single level  association rule
			2. Multilevel association rule 
			3. Quantitative association rule   
				-  It form the rule based on condition with numeric value. if age>30 and income >50k -> buy luxury goods
		- Visualization techniques:
			- **SGI minesets rule visualizer**
				- Map the left and ride sides of the rules to the x and y axes
				- confidence - represented by the height of the bar
				- support- represented by height of the discs 
				- color indicate the rules interestingness.
				- Number of rules that can be visualize is limited and it does not support combination of items on left and right hands sides.
			- **Mosaic and Double Decker plots**:
				1. Mosaic 
					- It is used to display the relationship between two or more categorical variable .t divide the area of plot into tiles or rectangles.
					- *Rectangle size* - freq of corresponding categories in the dataset.
					- *Height* - parameter values
					- *color* - It is used to highlights pattern in the data(strength of association b/w variables)
					- `EXAMPLE`
						- **Product Type (Fruits, Vegetables, Dairy)**
						- **Day of the Week (Weekday, Weekend)**
						- **Interpretation:** If a large rectangle corresponds to **Fruits on the Weekend**, it shows that fruits are frequently bought on weekends. Small rectangles represent rare combinations.
				
				2. Double Decker plot:
					- It is enhance of mosaic plot by showing the conditional probabilities and focuses on one specific category or variable of interest which is placed on the y axis
					- `Example`
						- **Product (Bread, Milk, Butter)**
						- **Store Type (Online, Physical)**
						- **Day of the Week (Weekday, Weekend)**
						- **Interpretation:** This allows you to drill down into the data hierarchically. For instance, you could see that for online stores, milk is bought more often on weekends, while in physical stores, bread is the most popular item on weekdays.
				
			- Graph based visualization
			- Association matrix visualization
	
	2. **Classification**
	    - It is supervised learning because the training set is used to each the system how to classify the data.
	    - Most algorithm work as black box approach ,its often difficult to understand and optimize the decision model.
	    - `Algo:` IDS ,CART,ID5 ,C4.5 SLIQ and SPRINT
	    - Visualization techniques:
		    - *SGI minesets system* -It allow interactive selection of the attributes shown and helps the users to understand the decision tree.
		    - Decision Tree 
			    - To show the each attributes value by a colored pixel and arrange them in bars.
			    - It take the attribute with purest value as split variable and perform it repeatedly until no purest form attributes
			    - *Size of nodes*
			    - *Quality of split(purity of attributes)*
			    - *Class distribution*
	
	1. **Clustering:**
		- It is a process of finding a partitioning of the data set into homogeneous subset called clusters.
		- Unsupervised learning ,it is easy to visualize and understand on 2 or 3 D space but its difficult in higher dimensional space 
		- Visualization technique for high dimensional cluster - OPTICS (ordering points to identify the clustering structure )
		
		- *Reachability Distance:* 
			- It is a visualization techniques used in density based structure of the data by plotting reachability distances which reflect how close or far apart data points are from one another.
			- *Low valley* for dense clusters(low rechability distance indicate the points are close to each other)
			- *High peaks* for noise or sparse data(High reachability distance due to lack of nearby points)
		- **HD-Eyes** 
			- It is visualization and exploration tool designed for analyzing high dimensional data using clustering techniques.
			- It is not a specific clustering algorithm rather than its a visual analytics system that combine clustering with interactive visualization methods helps user to explore complex and High dimensional datasets
			- Specially for high dimensional dataset with different features which are not visualized using 2 or 3D plotting techniques.
			- *Number of icons* - Number of peaks in the projection
			- *Color* - Number of data points belong to the maximum(dark color -large maxima and bright color - small maxima)
			- *Spike shape* - sharp spike ->well separated maxima ,blunt spike - weak separated maxima
			- Dimensionality reduction (PCA & t-SNE),parameter adjustment(no of cluster , threshold distances) ,parallel coordinates.
			- `Example`
			- *Consider a dataset with 1000 features describing customer behavior for an e-commerce website. It is challenging to visualize such high-dimensional data directly. HD-Eye can project this data onto a 2D plane using t-SNE, allowing the user to:*
				- See how customers naturally cluster based on their behavior (e.g., frequent shoppers vs. occasional browsers)
				- Adjust the clustering parameters interactively (e.g., changing the distance metric) to see how the clusters evolve.

---
---




## Unit 2  NUMPY

>NUMPY 5
Understanding Data Types in Python-The Basics of NumPy Arrays-Computation on NumPy Arrays: Universal
Functions-Aggregations: Min, Max, and Everything In Between-Computation on Arrays: Broadcasting-Comparisons,
Masks, and Boolean Logic-Fancy Indexing-Sorting Arrays-Structured Data: NumPy's Structured Arrays

### Understanding data types in Python

- While a statically-typed language like C or Java requires each variable to be explicitly declared, a dynamically-typed language like Python skips this specification

```c
int result = 0;
for(int i=0; i<100; i++){
    result += i;
}
```

```python
result = 0
for i in range(100):
    result += i
```

**A Python Integer Is More Than Just an Integer**
- The standard Python implementation is written in C.
- This means that every Python object is simply a cleverly-disguised C structure, which contains not only its value, but other information as well.
```c
struct _longobject {
    long ob_refcnt;
    PyTypeObject *ob_type;
    size_t ob_size;
    long ob_digit[1];
};
```


![[Pasted image 20241020190811.png]]


- **A Python List Is More Than Just a List**

- List - is heterogeneous data set
- Array - same as list its is much faster compare to list
```python 
L2 = [str(c) for c in L]
L2
L3 = [True, "2", 3.0, 4]
[type(item) for item in L3]
```

![[Pasted image 20241020184906.png]]
- At the implementation level, the array essentially contains a single pointer to one contiguous block of data. The Python list, on the other hand, contains a pointer to a block of pointers, each of which in turn points to a full Python object like the Python integer we saw earlier.

- **Fixed-Type Arrays in Python**
	- 