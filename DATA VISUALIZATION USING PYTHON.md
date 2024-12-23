

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
		5. Radial plot(star plot)
	
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
				1. Dimensional stacking is a technique that displays multivariate data in a two-dimensional space by collapsing dimensions in a specific order.
				2. This technique allows users to visualize trends in high-dimensional spaces by clustering similar output values together.
				3. `ex` Product and sales mapped to the vertical axis, region and month mapped to the horizontal
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
		- TOOLS: Magic lens ,infocrystal ,Dynamic queries & polaris.
	
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






---
---


>**UNIT 3  DATA MANIPULATION WITH PANDAS**
>
Introducing Pandas Objects-Data Indexing and Selection-Operating on Data in Pandas-Handling Missing Data-
Hierarchical Indexing-Combining Datasets: Concat and Append-Combining Datasets: Merge and Join-Aggregation
and Grouping-Pivot Tables-Vectorized String Operations-Working with Time Series-High-Performance Pandas: eval()
and query() (CHAPTER NO: 3 from T2)

### Indexing and selection

**Series**
- A `Series` object acts in many ways like a one-dimensional NumPy array, and in many ways like a standard Python dictionary.
```python

import pandas as pd
data=pd.Series([0,1,2,3,4],index=['a','b','c','d','e'])
data['a':'c'] # slicing by explicit index last index include
data[0:2]   # slicing by implicit integer index last index not include

data[(data>1) & (data<4)] # masking
# fancy indexing
data[['a', 'e']]

```

### Indexing:

**Boolean masking**, also called **boolean indexing**, is a feature in Python NumPy that allows for the filtering of values in `numpy` arrays.

- **Method one**: Returning the result array.  arr[arr > 5]

- **Method two**: Returning a boolean array.  mask = arr > 5

INDEXING METHODS:
- **Dataframe.[ ] ;** This function also known as indexing operator
- **Dataframe.loc[ ]** This function is used for labels.
- **Dataframe.iloc[ ]** ****:**** This function is used for positions or integer based
- **Dataframe.ix[]** This function is used for both label and integer based

- df.loc[] - It can select subset of rows and columns 
- df.iloc [] -  It use integer value to select of rows and columns

```python
import pandas as pd

# making data frame from csv file
data = pd.read_csv("nba.csv", index_col ="Name")

# retrieving row by loc method
first = data.loc["Avery Bradley"]
second = data.loc["R.J. Hunter"]
first = data.loc[["Avery Bradley", "R.J. Hunter"],
                   ["Team", "Number", "Position"]] #row & column


row2 = data.iloc[3] # row
row2 = data.iloc [[3, 5, 7]] # retrieving multiple rows
row2 = data.iloc [[3, 4], [1, 2]] # rows and columns

print(first, "\n\n\n", second)
```


### Data selection in data frame:

```python

area = pd.Series({'California': 423967, 'Texas': 695662,
                  'New York': 141297, 'Florida': 170312,
                  'Illinois': 149995})
pop = pd.Series({'California': 38332521, 'Texas': 26448193,
                 'New York': 19651127, 'Florida': 19552860,
                 'Illinois': 12882135})
data = pd.DataFrame({'area':area, 'pop':pop})
data

data.iloc[:3, :2]  # rows and columns
data.loc[:'Illinois', :'pop']
data.ix[:3, :'pop']

```

![[Pasted image 20241129163227.png]]

### Handling missing data:
- sentinel value - default value passed as value in function
- Ex : none ,nan
- The first sentinel value used by Pandas is `None`, a Python singleton object that is often used for missing data in Python code.
- `NaN` - it is a special floating-point value recognized by all systems that use the standard IEEE floating-point representation:

- aggregation of array with `none` return error whereas `nan` return NaN.
- NumPy does provide some special aggregations that will ignore these missing values
```python
np.nansum(vals2), np.nanmin(vals2), np.nanmax(vals2)
```

**Operating on Null values**
- `isnull()`: Generate a boolean mask indicating missing values
- `notnull()`: Opposite of `isnull()`
- `dropna()`: Return a filtered version of the data
- `fillna()`: Return a copy of the data with missing values filled or imputed


- We cannot drop single values from a `DataFrame`; we can only drop full rows or full columns

```python
df.dropna(axis='columns') # axis=1
df.dropna(axis='columns', how='all') # columns contain all the null value
df.dropna(axis='rows', thresh=3) # thresh shows minimum non values if a rows not contain the thresh value then it dropped

```


**Filling  null values**
- Pandas provides the `fillna()` method, which returns a copy of the array with the null values replaced.
```python
data.fillna(0)
data.fillna(method='bfill') #backward fill replace the none value with previous one in backward
data.fillna(method='ffill')
```

### Hierarchical indexing:
- Pandas does provide `Panel` and `Panel4D` objects that natively handle three-dimensional and four-dimensional data (see [Aside: Panel Data](https://jakevdp.github.io/PythonDataScienceHandbook/03.05-hierarchical-indexing.html#Aside:-Panel-Data)), a far more common pattern in practice is to make use of _hierarchical indexing_ (also known as _multi-indexing_) to incorporate multiple index _levels_ within a single index.

```python

index = pd.MultiIndex.from_tuples(index)
pop = pop.reindex(index)

```

**Methods of multi index creation**

```python

# using pandas Dataframe

df = pd.DataFrame(np.random.rand(4, 2),
                  index=[['a', 'a', 'b', 'b'], [1, 2, 1, 2]],
                  columns=['data1', 'data2'])


# using pandas series

data = {('California', 2000): 33871648,
        ('California', 2010): 37253956,
        ('Texas', 2000): 20851820,
        ('Texas', 2010): 25145561,
        ('New York', 2000): 18976457,
        ('New York', 2010): 19378102}
pd.Series(data)

# from array
pd.MultiIndex.from_arrays([['a', 'a', 'b', 'b'], [1, 2, 1, 2]])

# from tuple
pd.MultiIndex.from_tuples([('a', 1), ('a', 2), ('b', 1), ('b', 2)])

#from product
pd.MultiIndex.from_product([['a', 'b'], [1, 2]])

#multi index method
pd.MultiIndex(levels=[['a', 'b'], [1, 2]],
              labels=[[0, 0, 1, 1], [0, 1, 0, 1]])


```

**Indexing and Slicing a multi index**

```python
pop['California', 2000] # [row ,col]
pop.loc['California':'New York']
pop[pop > 22000000] # masking
pop[['California', 'Texas']] # fancy indexing


```

**Data Aggregation on multi -indices**

```python

data_mean = health_data.mean(level='year')
data_mean.mean(axis=1, level='type')

```

### Combining datasets : concat and append:

**Concatenation of numpy**

```python
# using numpy
x = [1, 2, 3]
y = [4, 5, 6]
z = [7, 8, 9]
np.concatenate([x, y, z])

#using pandas

ser1 = pd.Series(['A', 'B', 'C'], index=[1, 2, 3])
ser2 = pd.Series(['D', 'E', 'F'], index=[4, 5, 6])
pd.concat([ser1, ser2])

# using make_df Dataframe

df1 = make_df('AB', [1, 2])
df2 = make_df('AB', [3, 4])
display('df1', 'df2', 'pd.concat([df1, df2],axix='col')')


```

### Concatenation with joins

```python

df5 = make_df('ABC', [1, 2])
df6 = make_df('BCD', [3, 4])
display('df5', 'df6', 'pd.concat([df5, df6])')

#join
display('df5', 'df6',"pd.concat([df5, df6], join='inner')")

display('df5', 'df6',"pd.concat([df5, df6], join_axes=[df5.columns])") # it similar to left join all values in df5 and matching values from df6

```

**Append method**
- The `append()` method in Pandas does not modify the original object–instead it creates a new object with the combined data.

```python
display('df1', 'df2', 'df1.append(df2)')

```


### Aggregation and Grouping

- computing aggregations like `sum()`, `mean()`, `median()`, `min()`, and `max()`

```python
rng = np.random.RandomState(42)
ser = pd.Series(rng.rand(5))
ser

ser.sum()
ser.sum()
```

```python
df = pd.DataFrame({'key': ['A', 'B', 'C', 'A', 'B', 'C'],
                   'data': range(6)}, columns=['key', 'data'])

df.groupby('key').sum()

```


### Aggregate,filter ,transform,apply:

```python

df.groupby('key').aggregate(['min', np.median, max])

# filter
filtered_df = df.query('Age > 30 and Score < 90')
print(filtered_df)

or 
df.``filter``(regex` `=``'[aA]'``)
df.``filter``([``"Name"``,` `"College"``,` `"Salary"``])`

#apply
df=df.apply(fun) def fun(num):num+=10

display('df2', 'df2.groupby(str.lower).mean()')

```


### Pivot table

- A _pivot table_ is a similar operation that is commonly seen in spreadsheets and other programs that operate on tabular data.
- The pivot table takes simple column-wise data as input, and groups the entries into a two-dimensional table that provides a multidimensional summarization of the data.


### Vectorized string operations:

```python 

data = ['peter', 'Paul', 'MARY', 'gUIDO']
[s.capitalize() for s in data]


`df` `=` `pd.Series([``'night_fury1'``,` `'Is  '``,` `'Geeks, forgeeks'``,`'100'``, np.nan,` `'  Contributor '``])`

# lower()
print(df.str.lower())
#upper()
print(df.str.upper())
# string 
print('\nAfter using the strip:')
print(df.str.strip())
print``(df.``str``.split(``','``))

# concatenate

print("\nafter using cat:")
print(df.str.cat(sep='_'))

print("\nworking with NaN using cat:")
print(df.str.cat(sep='_', na_rep='#')) # nan value replaced by "#" value.

# get_dummies()
print(df.str.get_dummies()) # return 1 if exists or 0

# startswith(pattern)
print(df.str.startswith('G'))

# endswith(pattern)
print(df.str.endswith('1'))

# replace(a,b)
print(df.str.replace('Geeks', 'Gulshan'))
# repeat(value)
print(df.str.repeat(2)) # repeat the string two times

# count(pattern)
print(df.str.count('n')) # count the pattern from the Dataframe

# find(pattern)
print(df.str.find('n')) # return the position of the first occurence

# findall(pattern) in result [] indicates null list as  there is no value matching with givenpattern in particular row
print(df.str.findall('n'))

# islower()
print(df.str.islower())

# isupper()
print(df.str.isupper()) 

# isnumeric()
print(df.str.isnumeric())

# swapcase()
print(df.str.swapcase()) # swap the case of the each character

```

- **cat(sep=’ ‘):** It concatenates the data-frame index elements or each string in DataFrame with given separator.

- **get_dummies():** It returns the DataFrame with One-Hot Encoded values like we can see that it returns boolean value 1 if it exists in relative index or 0 if not exists.

- **Startswith(pattern):** It returns true if the element or string in the DataFrame Index starts with the pattern.

- **Python repeat(value) :** It repeats each element with a given number of times like below in example, there are two appearances of each string in DataFrame.

### Working with time series:
- datatime
- datautils

```python
from datetime import datetime
datetime(year=2015, month=7, day=4) # integer value is passed as parameter

from dateutil import parser
date = parser.parse("4th of July, 2015")
date # it parse the value from the string 

date.strftime('%A') # print the day of the week
datetime.strptime('31/01/22 23:59:59.999999',

                  '%d/%m/%y %H:%M:%S.%f')
datetime.datetime(2022, 1, 31, 23, 59, 59, 999999)

_.strftime('%a %d %b %Y, %I:%M%p')
'Mon 31 Jan 2022, 11:59PM'

# numpy array
import numpy as np
date = np.array('2015-07-04', dtype=np.datetime64)
date

date + np.arange(12) # add 0 to 11 value to day in data variable
# 2015-07-04 2015-07-05 2015-07-06 ....

import pandas as pd
date = pd.to_datetime("4th of July, 2015")
date   # convert the string to datatime 


```



 - `strftime(format)` and `strptime(date_str ,format)` 
 - The `datetime64` dtype encodes dates as 64-bit integers, and thus allows arrays of dates to be represented very compactly.
 
**Pandas time series : indexing by time**

```python
index = pd.DatetimeIndex(['2014-07-04', '2014-08-04',
                          '2015-07-04', '2015-08-04'])
data = pd.Series([0, 1, 2, 3], index=index)
data

data['2014-07-04':'2015-07-04']
data['2015'] # fetch the value with index as 2015 

```

**Pandas Time series data structure**

```python
dates = pd.to_datetime([datetime(2015, 7, 3), '4th of July, 2015',
                       '2015-Jul-6', '07-07-2015', '20150708'])
dates

# create a data with frequence
pd.date_range('2015-07-03', '2015-07-10') # date from 03 to 10
pd.date_range('2015-07-03', periods=8) # 8 dates from 3 to 10 here the freq='D' which is used to define the date increase by day

pd.date_range('2015-07-03', periods=8, freq='H') # increase by hours from 00 to 07

```

**Frequencies and offset**
- Fundamental to these Pandas time series tools is the concept of a frequency or date offset. Just as we saw the `D` (day) and `H` (hour) codes above, we can use such codes to specify any desired frequency spacing 

**Resampling ,Shifting and windowing**

- One common need for time series data is resampling at a higher or lower frequency.

```python
from pandas_datareader import data

goog = data.DataReader('GOOG', start='2004', end='2016',
                       data_source='google')
goog.head()


goog.plot(alpha=0.5, style='-')
goog.resample('BA').mean().plot(style=':')
goog.asfreq('BA').plot(style='--');
plt.legend(['input', 'resample', 'asfreq'],
           loc='upper left');




```

Window functions in Pandas provide a powerful way to perform operations on a series of data, allowing you to compute statistics and other aggregations over a window of data points

- **Rolling Window:** A sliding window that can be fixed or variable in size.
    
- **Weighted Window:** A non-rectangular, weighted window supplied by the scipy.signal library.
    
- **Expanding Window:** An accumulating window that includes all data points up to the current one.
    
- **Exponentially Weighted Window:** An accumulating window that applies exponential weighting to previous data points

### Eval() and query():

Pandas `dataframe.eval()` function is used to evaluate an expression in the context of the calling dataframe instance

```python
tmp1 = (x > 0.5)
tmp2 = (y < 0.5)
mask = tmp1 & tmp2

import numexpr
mask_numexpr = numexpr.evaluate('(x > 0.5) & (y < 0.5)')
np.allclose(mask, mask_numexpr) # allclose return true if both same or flase

np.allclose(df1 + df2 + df3 + df4,pd.eval('df1 + df2 + df3 + df4'))

# arithmetic operation
result1 = -df1 * df2 / (df3 + df4) - df5
result2 = pd.eval('-df1 * df2 / (df3 + df4) - df5')
np.allclose(result1, result2)

result1 = (df1 < df2) & (df2 <= df3) & (df3 != df4)
result2 = pd.eval('df1 < df2 <= df3 != df4') # it allow chained expressions df1<df2 df2<=df3

np.allclose(result1, result2) # true

# it also allow bitwise and logical and or operator

result3 = pd.eval('(df1 < 0.5) and (df2 < 0.5) or (df3 < df4)')
np.allclose(result1, result3)

result1 = (df['A'] + df['B']) / (df['C'] - 1)
result2 = pd.eval("(df.A + df.B) / (df.C - 1)")
np.allclose(result1, result2)

column_mean = df.mean(1)
result1 = df['A'] + column_mean
result2 = df.eval('A + @column_mean')
np.allclose(result1, result2)


```

- Notice that this `@` character is only supported by the `DataFrame.eval()` _method_, not by the `pandas.eval()` _function_, because the `pandas.eval()`

The `DataFrame` has another method based on evaluated strings, called the `query()` method.

```python

result1 = df[(df.A < 0.5) & (df.B < 0.5)]
result2 = pd.eval('df[(df.A < 0.5) & (df.B < 0.5)]')
np.allclose(result1, result2)

result2 = df.query('A < 0.5 and B < 0.5')
np.allclose(result1, result2)

```

--- 
--- 
>**UNIT-IV VISUALIZATION WITH MATPLOTLIB**
>
Simple Line Plots-Simple Scatter Plots-Visualizing Errors-Density and Contour Plots-Histograms, Binnings, and
Density-Customizing Plot Legends-Customizing Color bars-Multiple Subplots-Text and Annotation
Customizing Ticks-Customizing Matplotlib: Configurations and Stylesheets-Three-Dimensional Plotting in
Matplotlib-Geographic Data with Base map-Visualization with Seaborn 
(CHAPTER NO: 4 from T2)

### Simple line plots

- Perhaps the simplest of all plots is the visualization of a single function $y = f(x)$.

```python
fig = plt.figure()
ax = plt.axes()

x = np.linspace(0, 10, 1000)
ax.plot(x, np.sin(x))# sinusodial graph 

or 
plt.plot(x, np.sin(x))

#multiple lines
plt.plot(x, np.sin(x))
plt.plot(x, np.cos(x))


```

**Adjusting the color ,lines ,axes limit and labeling in charts**

```python
plt.plot(x, np.sin(x - 0), color='blue')        # specify color by name
plt.plot(x, np.sin(x - 1), color='g')   # by rgbcmyk

#STYLE 
plt.plot(x, x + 0, linestyle='solid') # dashed or -- ,dashdot or -., dotted or :

#STYLE WITH color
plt.plot(x, x + 2, '-.k') # dashdot black
plt.plot(x, x + 3, ':r');  # dotted red

# LIMIT OF THE AXIS 

plt.plot(x, np.sin(x))

plt.xlim(-1, 11) # Reverse of axis also possible (11,-1)
plt.ylim(-1.5, 1.5);

plt.plot(x, np.sin(x))
plt.axis([-1, 11, -1.5, 1.5])  # `[xmin, xmax, ymin, ymax]`:

#LABELING plot

plt.plot(x, np.sin(x))
plt.title("A Sine Curve")
plt.xlabel("x")
plt.ylabel("sin(x)");

```

- When multiple lines are being shown within a single axes, it can be useful to create a plot legend that labels each line type. Again, Matplotlib has a built-in way of quickly creating such a legend. It is done via the (you guessed it) `plt.legend()` method

```python

plt.plot(x, np.sin(x), '-g', label='sin(x)')
plt.plot(x, np.cos(x), ':b', label='cos(x)')
plt.axis('equal') # unit of x and y are equal i.e x and y axis have same axis value.

plt.legend();

```

### Scatter splot
- Another commonly used plot type is the simple scatter plot, a close cousin of the line plot. Instead of points being joined by line segments, here the points are represented individually with a dot, circle, or other shape
- 
```python

x = np.linspace(0, 10, 30)
y = np.sin(x)

plt.plot(x, y, 'o', color='black'); # o=circle

plt.plot(x, y, '-ok'); # circle connected with dots black color
```

- A second, more powerful method of creating scatter plots is the `plt.scatter` function, which can be used very similarly to the `plt.plot` function:
- plt.scatter will help to control the size ,face ,edge,color etc..

```python
plt.scatter(x, y, marker='o');


rng = np.random.RandomState(0)
x = rng.randn(100)
y = rng.randn(100)
colors = rng.rand(100)
sizes = 1000 * rng.rand(100)
plt.scatter(x, y, c=colors, s=sizes, alpha=0.3,
            cmap='viridis')
plt.colorbar();  # show color scale
```

- For large datasets, the difference between these two can lead to vastly different performance, and for this reason, `plt.plot` should be preferred over `plt.scatter` for large datasets.

### Dense & contour plots:
- Sometimes it is useful to display three-dimensional data in two dimensions using contours or color-coded regions.
- 3 functions `plt.contour ,plt.contourf, plt.imshow`

```python

x = np.linspace(0, 5, 50)
y = np.linspace(0, 5, 40)

X, Y = np.meshgrid(x, y) # form 2d grid from 1d
Z = f(X, Y)
plt.contour(X, Y, Z, colors='black')
plt.contour(X, Y, Z, 20, cmap='RdGy')# red gray

plt.contourf(X, Y, Z, 20, cmap='RdGy')
plt.colorbar();

plt.imshow(Z, extent=[0, 5, 0, 5], origin='lower',
           cmap='RdGy')
plt.colorbar()
plt.axis(aspect='image');
```

- `plt.imshow()` doesn't accept an _x_ and _y_ grid, so you must manually specify the _extent_ [_xmin_, _xmax_, _ymin_, _ymax_] of the image on the plot.

**Visualizing Errors**
- For any scientific measurement, accurate accounting for errors is nearly as important, if not more important, than accurate reporting of the number itself.
- Basic error bars 
	- A basic errorbar can be created with a single Matplotlib function call
- Continuous errors
	- `plt.fill_between` function with a light color to visualize this continuous error
	- 

```python
x = np.linspace(0, 10, 50)
dy = 0.8
y = np.sin(x) + dy * np.random.randn(50)

plt.errorbar(x, y, yerr=dy, fmt='.k'); # fmt - format code for line representation

plt.errorbar(x, y, yerr=dy, fmt='o', color='black',
             ecolor='lightgray', elinewidth=3, capsize=0); 

# continuous plot
plt.plot(xdata, ydata, 'or')
plt.plot(xfit, yfit, '-', color='gray')

plt.fill_between(xfit, yfit - dyfit, yfit + dyfit,
                 color='gray', alpha=0.2)
plt.xlim(0, 10)

```

### [Histograms,Binnings and Density:](https://jakevdp.github.io/PythonDataScienceHandbook/04.06-customizing-legends.html)

- The `hist()` function has many options to tune both the calculation and the display

```python

plt.hist(data, bins=30, normed=True, alpha=0.5,
         histtype='stepfilled', color='steelblue',
         edgecolor='none');

```

- If you would like to simply compute the histogram (that is, count the number of points in a given bin) and not display it, the `np.histogram()` function is available:

```python
counts, bin_edges = np.histogram(data, bins=5)
print(counts)

```

**Two dimensional histogram and binnings**

- Just as we create histograms in one dimension by dividing the number-line into bins, we can also create histograms in two-dimensions by dividing points among two-dimensional bins
- `plt.hist2d` - plot 2D data
- just as `plt.hist` has a counterpart in `np.histogram`, `plt.hist2d` has a counterpart in `np.histogram2d`, which can be used as follows

```python

plt.hist2d(x, y, bins=30, cmap='Blues')
cb = plt.colorbar()
cb.set_label('counts in bin')

# histogram2D
counts, xedges, yedges = np.histogram2d(x, y, bins=30)

```

**Hexagonal binnings**
- The two-dimensional histogram creates a tesselation of squares across the axes.
- `plt.hexbin` - represents a two-dimensional dataset binned within a grid of hexagons

```python

plt.hexbin(x, y, gridsize=30, cmap='Blues')
cb = plt.colorbar(label='count in bin')

```

**kernel density estimation**
- Another common method of evaluating densities in multiple dimensions is _kernel density estimation_ (KDE)
- One extremely quick and simple KDE implementation exists in the `scipy.stats` package. Here is a quick example of using the KDE on this data
- `gaussian_kde` uses a rule-of-thumb to attempt to find a nearly optimal smoothing length for the input data.
- other KDE  :`sklearn.neighbors.KernelDensity` and `statsmodels.nonparametric.kernel_density.KDEMultivariate`

```python

from scipy.stats import gaussian_kde

# fit an array of size [Ndim, Nsamples]
data = np.vstack([x, y])
kde = gaussian_kde(data)

```

### [Customizing plot legends](https://jakevdp.github.io/PythonDataScienceHandbook/04.06-customizing-legends.html)
- Plot legends give meaning to a visualization, assigning meaning to the various plot elements. `plt.legend()`
- location can be specified using  `loc`
- number of column can be specified using `ncol`
- `fancybox` it provide a Fancy box or shadow of the frame

```python
x = np.linspace(0, 10, 1000)
fig, ax = plt.subplots()
ax.plot(x, np.sin(x), '-b', label='Sine')
ax.plot(x, np.cos(x), '--r', label='Cosine')
ax.axis('equal')
leg = ax.legend()

#LOCATION
ax.legend(loc='upper left', frameon=False)
fig
ax.legend(frameon=False, loc='lower center', ncol=2)
fig

#FANCY BOX
ax.legend(fancybox=True, framealpha=1, shadow=True, borderpad=1)
fig
```

### [Customizing colorbars:](https://jakevdp.github.io/PythonDataScienceHandbook/04.07-customizing-colorbars.html)
- In Matplotlib, a colorbar is a separate axes that can provide a key for the meaning of colors in a plot
- Plot legends identify discrete labels of discrete points. For continuous labels based on the color of points, lines, or regions, a labeled colorbar can be a great tool.
- `plt.colorbar` 
- `cmap` -colormap specified  by cmap
- **CHOOSING THE COLOR MAP** 

	- _Sequential colormaps_(binary or viridis)
	- *Divergent colormaps*(RdBu or Pu0r)
	- _Qualitative colormaps_:(jet or rainbow)
	
- showing positive and negative deviations from some mean, dual-color colorbars such as `RdBu` (_Red-Blue_) can be useful.

- **COLOR LIMIT AND EXTENSION:**

	- Matplotlib allows for a large range of colorbar customization.
	- `extend` - provide a large customization for visualizing the charts
	
- **DISCRETE COLOR BARS**
	- Colormaps are by default continuous, but sometimes you'd like to represent discrete values.
	- `plt.cm.get_cmap()` - It is used to visualize the discrete value.

```python
x = np.linspace(0, 10, 1000)
I = np.sin(x) * np.cos(x[:, np.newaxis])

plt.imshow(I)
plt.colorbar()

#CMAP
plt.imshow(I, cmap='gray');

# viridis(continuous data)

view_colormap('viridis')
view_colormap('cubehelix')

#Divergent
view_colormap('RdBu')

# EXTEND
plt.subplot(1, 2, 2)
plt.imshow(I, cmap='RdBu')
plt.colorbar(extend='both')
plt.clim(-1, 1);

# DISCRETE COLOR BARS:
plt.imshow(I, cmap=plt.cm.get_cmap('Blues', 6)) # (color,bin)
plt.colorbar()
plt.clim(-1, 1);

```

**Example:Handwritten digit dataset**
- This data is included in Scikit-Learn, and consists of nearly 2,000 8×8 thumbnails showing various hand-written digits.
- `plt.imshow()`
- But visualizing relationships in such high-dimensional spaces can be extremely difficult. One way to approach this is to use a _dimensionality reduction_ technique such as manifold learning to reduce the dimensionality of the data while maintaining the relationships of interest.
- `ticks` and `clim` to improve the aesthetics of the resulting colorbar in discrete dataset

```python
# project the digits into 2 dimensions using IsoMap
from sklearn.manifold import Isomap
iso = Isomap(n_components=2)
projection = iso.fit_transform(digits.data)
```


### [Multiple subplots](https://jakevdp.github.io/PythonDataScienceHandbook/04.08-multiple-subplots.html):
- To this end, Matplotlib has the concept of _subplots_: groups of smaller axes that can exist together within a single figure
- `plt.axes` also takes an optional argument that is a list of four numbers in the figure coordinate system. These numbers represent `[left, bottom, width, height]`
- The equivalent of this command within the object-oriented interface is `fig.add_axes()`

- **Grid subplot**
	- The lowest level of these is `plt.subplot()`, which creates a single subplot within a grid.
	- his command takes three integer arguments—the number of rows, the number of columns, and the index of the plot
- `plt.subplots_adjust` - adjust the spacing between the plots. same as `fig.add_subplot()`

- **Whole grid in one Go**
	- `plt.subplots()` is the easier tool to use (note the `s` at the end of `subplots`) 
	- Rather than creating a single subplot, this function creates a full grid of subplots in a single line, returning them in a NumPy array.
	- It hides the `x` and `y` axis in the inside subplots.
	- `sharex` and `sharey` - specify the relationship between different axes.
	- Note that by specifying `sharex` and `sharey`, we've automatically removed inner labels on the grid to make the plot cleaner.
	
- **MORE COMPLICATED ARRANGEMENTS**

	- To go beyond a regular grid to subplots that span multiple rows and columns, `plt.GridSpec()` is the best tool.
	- The `plt.GridSpec()` object does not create a plot by itself; it is simply a convenient interface that is recognized by the `plt.subplot()` command.

```python
ax1 = plt.axes()  # standard axes
ax2 = plt.axes([0.65, 0.65, 0.2, 0.2])

#SUBPLOT

for i in range(1, 7):
    plt.subplot(2, 3, i) #(row,col,index)
    plt.text(0.5, 0.5, str((2, 3, i)),
             fontsize=18, ha='center')

# ADJUST 
fig = plt.figure()
fig.subplots_adjust(hspace=0.4, wspace=0.4) # height and width
for i in range(1, 7):
    ax = fig.add_subplot(2, 3, i)
    ax.text(0.5, 0.5, str((2, 3, i)),
           fontsize=18, ha='center')

# SUBPLOTS 
fig, ax = plt.subplots(2, 3, sharex='col', sharey='row')

# GRIDSPEC
grid = plt.GridSpec(2, 3, wspace=0.4, hspace=0.3) #It create a 2x3 plot with subplot and this subplots then separated with slicing 

plt.subplot(grid[0, 0])
plt.subplot(grid[0, 1:])
plt.subplot(grid[1, :2])
plt.subplot(grid[1, 2]);

```

### [Text and Annotation](https://jakevdp.github.io/PythonDataScienceHandbook/04.09-text-and-annotation.html):

- In some cases, this story can be told in an entirely visual manner, without the need for added text, but in others, small textual cues and labels are necessary.
- `plt.text`/`ax.text` - used to add the text to the charts.
- The `ax.text` method takes an x position, a y position, a string, and then optional keywords specifying the color, size, style, alignment, and other properties of the text
- `ha='right'` and `ha='center'` - horizontal alignment specify by `ha`

- **Transform and text position**
	- Sometimes it's preferable to anchor the text to a position on the axes or figure, independent of the data. In Matplotlib, this is done by modifying the _transform_.
	- `ax.transData`: Transform associated with data coordinates
	- `ax.transAxes`: Transform associated with the axes (in units of axes dimensions)
	- `fig.transFigure`: Transform associated with the figure (in units of figure dimensions)

- **Arrow and annotations**
	- Drawing arrows in Matplotlib is often much harder than you'd bargain for. While there is a `plt.arrow()`
	- Instead, I'd suggest using the `plt.annotate()` function. This function creates some text and an arrow, and the arrows can be very flexibly specified.
	- `arrowprops` 


```python
fig, ax = plt.subplots(figsize=(12, 4))
births_by_date.plot(ax=ax)

# Add labels to the plot
style = dict(size=10, color='gray')

ax.text('2012-1-1', 3950, "New Year's Day", **style)
ax.text('2012-7-4', 4250, "Independence Day", ha='center', **style)
ax.text('2012-9-4', 4850, "Labor Day", ha='center', **style)
ax.text('2012-10-31', 4600, "Halloween", ha='right', **style)
ax.text('2012-11-25', 4450, "Thanksgiving", ha='center', **style)
ax.text('2012-12-25', 3850, "Christmas ", ha='right', **style)

# Label the axes
ax.set(title='USA births by day of year (1969-1988)',
       ylabel='average daily births')

# TRANSFORM 
ax.text(1, 5, ". Data: (1, 5)", transform=ax.transData)
ax.text(0.5, 0.1, ". Axes: (0.5, 0.1)", transform=ax.transAxes)
ax.text(0.2, 0.2, ". Figure: (0.2, 0.2)", transform=fig.transFigure)


# ANNOTATE METHOD 

ax.annotate('local maximum', xy=(6.28, 1), xytext=(10, 4),
            arrowprops=dict(facecolor='black', shrink=0.05))

ax.annotate('local minimum', xy=(5 * np.pi, -1), xytext=(2, -6),
            arrowprops=dict(arrowstyle="->",
                            connectionstyle="angle3,angleA=0,angleB=-90"))



ax.annotate('Christmas', xy=('2012-12-25', 3850),  xycoords='data',
             xytext=(-30, 0), textcoords='offset points',
             size=13, ha='right', va="center",
             bbox=dict(boxstyle="round", alpha=0.1),
             arrowprops=dict(arrowstyle="wedge,tail_width=0.5", alpha=0.1));

```

### [CUSTOMIZING MATPLOTLIB: CONFIGURATION AND STYLESHEETS](https://jakevdp.github.io/PythonDataScienceHandbook/04.11-settings-and-stylesheets.html)

- we've seen how it is possible to tweak individual plot settings to end up with something that looks a little bit nicer than the default.
- Each time Matplotlib loads, it defines a runtime configuration (rc) containing the default styles for every plot element you create. This configuration can be adjusted at any time using the `plt.rc` convenience routine.
- **STYLESHEET**
	- `style` - Which provide different style
	- plt.style.available[:5]
	- ['fivethirtyeight',
		'seaborn-pastel',
		'seaborn-whitegrid',
		'ggplot',
		'grayscale']


```python

ax = plt.axes(axisbg='#E6E6E6')
ax.set_axisbelow(True)

# draw solid white grid lines
plt.grid(color='w', linestyle='solid')

# hide axis spines
for spine in ax.spines.values():
    spine.set_visible(False)
    
# hide top and right ticks
ax.xaxis.tick_bottom()
ax.yaxis.tick_left()

# lighten ticks and labels
ax.tick_params(colors='gray', direction='out')
for tick in ax.get_xticklabels():
    tick.set_color('gray')
for tick in ax.get_yticklabels():
    tick.set_color('gray')
    
# control face and edge color of histogram
ax.hist(x, edgecolor='#E6E6E6', color='#EE6666')


# PLT.RC

plt.rc('grid', color='w', linestyle='solid')
plt.rc('xtick', direction='out', color='gray')
plt.rc('ytick', direction='out', color='gray')
plt.hist(x);


#STYLE SHEETS 
plt.style.available[:5] #list all available style sheets
plt.style.use('stylename') # specify the style sheets
plt.rcParams.update(IPython_default);

```

### [Customizing ticks](https://jakevdp.github.io/PythonDataScienceHandbook/04.10-customizing-ticks.html)

- Matplotlib's default tick locators and formatters are designed to be generally sufficient in many common situations, but are in no way optimal for every plot.
- Major and Minor ticks 
	- ticks is the scale value in the axes which can be customized using ticks methods in matplotlib
- the `formatter` and `locator` objects of each axis which is used to locate and format the ticks
- **Hiding ticks or labels**
	- Perhaps the most common tick/label formatting operation is the act of hiding ticks or labels.
	- `plt.NullLocator()` and `plt.NullFormatter()` - which remove the ticks and labels in the axes.
	
- **Reducing or increasing the number of ticks**
	- One common problem with the default settings is that smaller subplots can end up with crowded labels
	- *fig, ax = plt.subplots(4, 4, sharex=True, sharey=True)* this provide a default plot with ticks it may overlap and difficult to interpret or decipher
	- `plt.MaxNLocator()` it allow to specify the maximum number of ticks and `plt.MultipleLocator` provide more customization
- **Fancy ticks formats**
	- Matplotlib's default tick formatting can leave a lot to be desired: it works well as a broad default, but sometimes you'd like do do something more.
	- 

```python
ax = plt.axes(xscale='log', yscale='log')
ax.grid();

# formater and locator

print(ax.xaxis.get_major_locator())
print(ax.xaxis.get_minor_locator())

print(ax.xaxis.get_major_formatter())
print(ax.xaxis.get_minor_formatter())

# ticks adjustment
# For every axis, set the x and y major locator
for axi in ax.flat:
    axi.xaxis.set_major_locator(plt.MaxNLocator(3))
    axi.yaxis.set_major_locator(plt.MaxNLocator(3))
fig
# Fancy ticks

ax.xaxis.set_major_locator(plt.MultipleLocator(np.pi / 2))
ax.xaxis.set_minor_locator(plt.MultipleLocator(np.pi / 4))
fig

```


### [Three dimensional plotting in matplotlib:](https://jakevdp.github.io/PythonDataScienceHandbook/04.12-three-dimensional-plotting.html)

- `mplot3d` -It enable the three dimensional plotting
- A three-dimensional axes can be created by passing the keyword `projection='3d'`
- **3D points and lines**
	- The most basic three-dimensional plot is a line or collection of scatter plot created from sets of (x, y, z) triples. `ax.plot3D` and `ax.scatter3D` used to create 3D plot
	
- **3D countour plots**
	- Like two-dimensional `ax.contour` plots, `ax.contour3D` requires all the input data to be in the form of two-dimensional regular grids, with the Z data evaluated at each point.
	
 - **Wireframes and Surface plots**
	 - Two other types of three-dimensional plots that work on gridded data are wireframes and surface plots.
	 
- **Surface triangulation**
	- The evenly sampled grids required by the above routines is overly restrictive and inconvenient. In these situations, the triangulation-based plots can be very useful.
	- `ax.plot_trisurf`, which creates a surface by first finding a set of triangles formed between adjacent points
	- 

```python
from mpl_toolkits import mplot3d
fig = plt.figure()
ax = plt.axes(projection='3d')

# 3D LINE PLOT
ax = plt.axes(projection='3d')

# Data for a three-dimensional line
zline = np.linspace(0, 15, 1000)
xline = np.sin(zline)
yline = np.cos(zline)
ax.plot3D(xline, yline, zline, 'gray')


#Add color to the surface chart
ax = plt.axes(projection='3d')
ax.plot_surface(X, Y, Z, rstride=1, cstride=1,
                cmap='viridis', edgecolor='none')
ax.set_title('surface');


```

**Example**
A **Möbius strip** is similar to a strip of paper glued into a loop with a half-twist. Topologically, it's quite interesting because despite appearances it has only a single side!

### [ Geographic data with Basemap:](https://jakevdp.github.io/PythonDataScienceHandbook/04.13-geographic-data-with-basemap.html)

- Matplotlib's main tool for this type of visualization is the Basemap toolkit, which is one of several Matplotlib toolkits which lives under the `mpl_toolkits` namespace.
- More modern solutions such as leaflet or the Google Maps API may be a better choice for more intensive map visualizations. Still, Basemap is a useful tool for Python users to have in their virtual toolbelts.

### [Visualization with seaborn](https://jakevdp.github.io/PythonDataScienceHandbook/04.14-visualization-with-seaborn.html)

- Matplotlib predated Pandas by more than a decade, and thus is not designed for use with Pandas `DataFrame`s. In order to visualize data from a Pandas `DataFrame`, you must extract each `Series` and often concatenate them together into the right format
- An answer to these problems is [Seaborn](http://seaborn.pydata.org/). Seaborn provides an API on top of Matplotlib that offers sane choices for plot style and color defaults, defines simple high-level functions for common statistical plot types, and integrates with the functionality provided by Pandas `DataFrame`
- **Exploring seaborn plots**
	- The main idea of Seaborn is that it provides high-level commands to create a variety of plot types useful for statistical data exploration, and even some statistical model fitting
	- Histogram ,KDE and desities
	- We can see the joint distribution and the marginal distributions together using `sns.jointplot`.
- **Pair plot**
	- When you generalize joint plots to datasets of larger dimensions, you end up with _pair plots_.
- **Faceted histogram**
	- Sometimes the best way to view data is via histograms of subsets. Seaborn's `FacetGrid` makes this extremely simple.similar to pair plot.
- **Factor plot**
	- Factor plots can be useful for this kind of visualization as well. This allows you to view the distribution of a parameter within bins defined by any other parameter
- **Joint distribution**
	- Similar to the pairplot we saw earlier, we can use `sns.jointplot` to show the joint distribution between different datasets, along with the associated marginal distributions:

```python
import seaborn as sns
sns.set()
# same plotting code as above!
plt.plot(x, y)
plt.legend('ABCDEF', ncol=2, loc='upper left');

#Histogram ,KDE and desities
data = np.random.multivariate_normal([0, 0], [[5, 2], [2, 2]], size=2000)
data = pd.DataFrame(data, columns=['x', 'y'])

for col in 'xy':
    plt.hist(data[col], normed=True, alpha=0.5)

for col in 'xy':
    sns.kdeplot(data[col], shade=True)

sns.distplot(data['x'])
sns.distplot(data['y']);

#jointplot

with sns.axes_style('white'):
    sns.jointplot("x", "y", data, kind='kde');

#PAIR plot
sns.pairplot(iris, hue='species', size=2.5);

# FACETED 

tips['tip_pct'] = 100 * tips['tip'] / tips['total_bill']

grid = sns.FacetGrid(tips, row="sex", col="time", margin_titles=True)
grid.map(plt.hist, "tip_pct", bins=np.linspace(0, 40, 15));


# factor plot
with sns.axes_style(style='ticks'):
    g = sns.factorplot("day", "total_bill", "sex", data=tips, kind="box")
    g.set_axis_labels("Day", "Total Bill");

# JOINT DISTRIBUTION  

sns.jointplot("total_bill", "tip", data=tips, kind='reg');

#BAR PLOT 

with sns.axes_style('white'):
    g = sns.factorplot("year", data=planets, aspect=2,
                       kind="count", color='steelblue')
    g.set_xticklabels(step=5)


```

---
---
>**UNIT-V MACHINE LEARNING**
>
Machine Learning-Introducing Scikit-Learn-Hyperparameters and Model Validation-Feature Engineering-Naive
Bayes Classification-Linear Regression-Support Vector Machines-Decision Trees and Random Forests-Principal
Component Analysis-Manifold Learning-k-Means Clustering-Gaussian Mixture Models-Kernel Density Estimation


### [Introduction to scikit-learn:](https://jakevdp.github.io/PythonDataScienceHandbook/05.02-introducing-scikit-learn.html)

- Scikit-Learn in one of the best library provides efficient versions of a large number of common algorithms.
- A **benefit** of this uniformity is that once you understand the basic use and syntax of Scikit-Learn for one type of model, switching to a new model or algorithm is very straightforward.

- **Data representation in scikit-learn**

	- *Data as table* (rows and columns)  `eg` iris dataset
		- The rows of the matrix as _samples_, and the number of rows as `n_samples`
		- The columns of the matrix as _features_, and the number of columns as `n_features`.
	- *Features matrix*
		- This table layout makes clear that the information can be thought of as a two-dimensional numerical array or matrix, which we will call the _features matrix_.
		- shape =`[n_samples, n_features]`
	- *Target array*
		- In addition to the feature matrix `X`, we also generally work with a _label_ or _target_ array, which by convention we will usually call `y`. The target array is usually one dimensional, with length `n_samples`, and is generally contained in a NumPy array or Pandas `Series`.
	
```python 
import seaborn as sns
iris = sns.load_dataset('iris')
iris.head()

X_iris = iris.drop('species', axis=1)
X_iris.shape

y_iris = iris['species'] # target 
y_iris.shape
```

- **Scikit-learn Estimator API**
	- The Scikit-Learn API is designed with the following guiding principles
	- _Consistency_,_Inspection_ ,_Limited object hierarchy_ ,_Composition_ ,_Sensible defaults_ 
	- Basics of the API
		- `fit(),predict(),transform(),`
	- Supervised learning `eg:` Simple linear regression
	
```python
# Choose a class of model
from sklearn.linear_model import LinearRegression

#### Choose model hyperparameters
model = LinearRegression(fit_intercept=True)
model

#### Arrange data into a features matrix and target vector
X = x[:, np.newaxis]
X.shape

#### 4. Fit the model to your data
model.fit(X, y)
model.coef_
model.intercept_

#### Predict labels for unknown data
xfit = np.linspace(-1, 11)
Xfit = xfit[:, np.newaxis]
yfit = model.predict(Xfit)

```

`Example` Supervised: Iris Classification

```python
from sklearn.cross_validation import train_test_split
Xtrain, Xtest, ytrain, ytest = train_test_split(X_iris, y_iris,
                                                random_state=1

from sklearn.naive_bayes import GaussianNB # 1. choose model class
model = GaussianNB()                       # 2. instantiate model
model.fit(Xtrain, ytrain)                  # 3. fit model to data
y_model = model.predict(Xtest)

from sklearn.metrics import accuracy_score
accuracy_score(ytest, y_model)

```

- **Unsupervised Learning** : Iris Dimensionality

```python
from sklearn.decomposition import PCA  # 1. Choose the model class
model = PCA(n_components=2)            # 2. Instantiate the model with hyperparameters
model.fit(X_iris)                      # 3. Fit to data. Notice y is not specified!
X_2D = model.transform(X_iris)

iris['PCA1'] = X_2D[:, 0]
iris['PCA2'] = X_2D[:, 1]
sns.lmplot("PCA1", "PCA2", hue='species', data=iris, fit_reg=False);

```

**Application:** Exploring hand-written digits

### Hyper parameters and model validation:

*Hyperparameters in Machine learning are those parameters that are explicitly defined by the user to control the learning process.*
- "hyper" suggests that the parameters are top-level parameters that are used in controlling the learning process.
- Some examples of Hyperparameters in Machine Learning

	- The k in kNN or K-Nearest Neighbour algorithm
	- Learning rate for training a neural network
	- Train-test split ratio
	- Batch Size
	- Number of Epochs
	- Branches in Decision Tree
	- Number of clusters in Clustering Algorithm
- Methods
	- **Hyperparameter for Optimization**
		- The process of selecting the best hyperparameters to use is known as hyperparameter tuning, and the tuning process is also known as hyperparameter optimization. Optimization parameters are used for optimizing the model.
		
		- Hyperparameter tuning are:
			- **Grid search** can be considered as a “brute force” approach to hyperparameter optimization. We fit the model using all possible combinations after creating a grid of potential discrete hyperparameter values.
			
			- **RandomizedSearchCV** name suggests, the random search method selects values at random as opposed to the grid search method’s use of a predetermined set of numbers. Every iteration, random search attempts a different set of hyperparameters and logs the model’s performance
			
			- **Bayesian Optimization** :Grid search and random search are often inefficient because they evaluate many unsuitable hyperparameter combinations without considering the previous iterations’ results. Bayesian optimization, on the other hand, treats the search for optimal hyperparameters as an optimization problem.
		
    - **Hyperparameter for Specific Models**
	    - Hyperparameters that are involved in the structure of the model are known as hyperparameters for specific models.

- **Model validation**: 
	- Holdout -`train_test_split`
	- Cross validation - each subset of data is used for both training set and validation set(k fold cross validation )

```python 
from sklearn.cross_validation import cross_val_score
cross_val_score(model, X, y, cv=5)

```

- Evaluation metrics for classification task:
	- Accuracy ,precision & recall 
	- F1 score - If we increase the precision, recall decreases and vice versa.
	- Confusion matrix
	- AUC-ROC curve 
	
		- AUC (Area Under Curve) is an evaluation metric that is used to analyze the classification model at different threshold values. The [Receiver Operating Characteristic](https://www.geeksforgeeks.org/receiver-operating-characteristic-roc-with-cross-validation-in-scikit-learn/)(ROC) curve is a probabilistic curve used to highlight the model’s performance. The curve has two parameters:

		- TPR: It stands for True positive rate. It basically follows the formula of Recall.
		- FPR: It stands for False Positive rate. It is defined as the ratio of False positives to the summation of false positives and True negatives.
	
	- Evaluation metrics for regression task
		- Mean absolute error = ∑|ypred-yactual| / N
		- Mean squared error  = ∑(ypred - yactual)2 / N
		- RMSE                         = √(∑(ypred - yactual)2 / N)
		- MAPE                        = ∑((ypred-yactual) / yactual) / N * 100 %


### Feature Engineering:

*Feature Engineering is the process of creating new features or transforming existing features to improve the performance of a machine-learning model*

- Feature engineering tasks: features for representing _categorical data_, features for representing _text_, and features for representing _images_.
- *Categorical feature* 
	- One Hot encoding
	- When your data comes as a list of dictionaries, Scikit-Learn's `DictVectorizer` it numeric .
- T*ext Feature* 
	- Most automatic mining of social media data relies on some form of encoding the text as numbers. One of the simplest methods of encoding data is by _word counts_.count the frequency of word in the text
	- `CountVectorizer`
	- _Term frequency-inverse document frequency_ (_TF–IDF_) which weights the word counts by a measure of how often they appear in the documents
- *Image Feature*


- Imputation of missing data : scikit provide a `imputer` class to handle missing data
- Feature pipelines -  which allow to perform the different steps at once such as removing imputation,transform feature ,model fit.

**Process involved in FE:**

- Feature creation
- Feature transformation 
	- Scaling ,Normalization,encoding and transformation
- Feature Extraction 
	- Dimensionality reduction,feature combination,feature aggregation
- Feature Selection 
	- Filter ,wrapper method and embedded method 
- Feature scaling
	- Min max scaling ,standard scaling and robust scaling 

### Naive Bayes classification:

- It is suitable for very high-dimensional datasets.
- It is aka _generative model_ because it specifies the hypothetical random process that generates the data.
- It is a probabilistic classifier, which means it predicts on the basis of the probability of an object.
- It is mainly used in _text classification_ that includes a high-dimensional training dataset
- **Naïve**: It is called Naïve because it assumes that the occurrence of a certain feature is independent of the occurrence of other features.
- **Bayes**: It is called Bayes because it depends on the principle of Bayes' Theorem.
- Bayes theorem:
	- $P(A|B)=P(B|A)*P(A)\div{p(B)}$

	- **P(A|B) is Posterior probability**: Probability of hypothesis A on the observed event B.
	
	- **P(B|A) is Likelihood probability**: Probability of the evidence given that the probability of a hypothesis is true.
	
	- **P(A) is Prior Probability**: Probability of hypothesis before observing the evidence.

	- **P(B) is Marginal Probability**: Probability of Evidence

### Types of Linear Regression 
- Linear regression models are a good starting point for regression tasks.
- Simple Linear regression and multiple linear regression
- The goal of the algorithm is to find the ****best Fit Line**** equation that can predict the values based on the independent variables.
- The slope of the line indicates how much the dependent variable changes for a unit change in the independent variable(s).
- *cost function* =$1\div{n}∑ni​(yi​^​−yi​)$
- *Gradient descent* 
	- A gradient is nothing but a derivative that defines the effects on outputs of the function with a little bit of variation in inputs.
	
- Assumption of linear regression
	- linearity
	- Independence ,Homoscedasticity,normality
	
- Assumption of multiple linear regression
	- No multicollinearity
	- Additivity
	- overfitting ,feature selection
- Regularization
	- Ridge regression or L2 regularization $\[P=α∑^N_(n=1)  θ^2_n\]$
	- This proceeds by penalizing the sum of squares (2-norms) of the model coefficients
	- Lasso regression or L1 regularization $\[P=α∑^N_n=1|θ_n|\]$
	- Another very common type of regularization is known as lasso, and involves penalizing the sum of absolute values (1-norms) of regression coefficients

```python

from sklearn.linear_model import LinearRegression
model = LinearRegression(fit_intercept=True)

model.fit(x[:, np.newaxis], y)

xfit = np.linspace(0, 10, 1000)
yfit = model.predict(xfit[:, np.newaxis])

plt.scatter(x, y)
plt.plot(xfit, yfit);

print("Model slope:    ", model.coef_[0])
print("Model intercept:", model.intercept_
	  
```

`Example` Bicycle traffic prediction

### [Support Vector Machine](https://www.geeksforgeeks.org/support-vector-machine-algorithm/)

- It is useful for both linear and nonlinear classification, as well as regression and outlier detection tasks.
- Its robust for binary and multi class classification.
- The primary objective of the **SVM algorithm** is to identify the **optimal hyperplane** in an N-dimensional space that can effectively separate data points into different classes in the feature space.
- Support vector machine terminology
	- Hyperplane,support vector,margin,kernel,hard margin,soft margin
- Types of svm
	- linear ,non-linear
- kernel svm
	- Linear,polynomial,Gaussian RBF and sigmoid

`Example` Face recognition

### [Decision Trees and Random Forests:](https://www.geeksforgeeks.org/decision-tree-introduction-example/)

- A decision tree is a type of supervised learning algorithm that is commonly used in machine learning to model and predict outcomes based on input data.
- Decision Tree works on the Sum of Product form which is also known as __Disjunctive Normal Form__.
- Attribute selection methods:
	1. Information Gain
		- Information gain is a measure of this change in entropy.
		- Gain(S,A)=Entropy(S)–∑vA​∣S∣∣Sv​∣​.Entropy(Sv​)
	2. Gini Index
		-  Gini Index is a metric to measure how often a randomly chosen element would be incorrectly identified.
		- It means an attribute with a lower Gini index should be preferred.
		- $Gini(s)=1-\sum^{c}_{i=1}p^2_i$
- Decision tree terminology


**Random forest**
- Bagging makes use of an ensemble (a grab bag, perhaps) of parallel estimators, each of which over-fits the data, and averages the results to find a better classification.
- `RandomForestClassifier`
- `RandomForestRegressor`

`Example`: classify the digits 

### [PCA:](https://www.geeksforgeeks.org/principal-component-analysis-pca/)

- **Principal Component Analysis (PCA)** is a statistical procedure that uses an orthogonal transformation that converts a set of correlated variables to a set of uncorrelated variables.
- Scikit-Learn contains a couple interesting variants on PCA, including `RandomizedPCA` and `SparsePCA`, both also in the `sklearn.decomposition` submodule.
- It is a Unsupervised learning
- STEPS 
	- Standardization
	- Covariance matrix Computation
	- Compute eigen values

### [Manifold learning](https://jakevdp.github.io/PythonDataScienceHandbook/05.10-manifold-learning.html)

- PCA not well on nonlinear relationship within the data.
- To address this deficiency, we can turn to a class of methods known as _manifold learning_—a class of unsupervised estimators that seeks to describe datasets as low-dimensional manifolds embedded in high-dimensional spaces.
- METHODS
	- t-SNE (t-distributed Stochastic Neighbor Embedding)
	- Isomap(Isometric mapping)
	- Locally Linear Embedding 
	- Multi-Dimensional Scaling 

### Kmean clustering 

- Unsupervised Machine Learning the process of teaching a computer to use unlabeled, unclassified data and enabling the algorithm to operate on that data without supervision.
- The goal of [clustering](https://www.geeksforgeeks.org/clustering-in-machine-learning/) is to divide the population or [set](https://www.geeksforgeeks.org/set-in-cpp-stl/) of data points into a number of groups so that the data points within each group are more [comparable](https://www.geeksforgeeks.org/comparable-vs-comparator-in-java/) to one another and different from the data points within the other groups.
### [Gaussian Mixture Models:](https://jakevdp.github.io/PythonDataScienceHandbook/05.12-gaussian-mixtures.html)

- The non-probabilistic nature of _k_-means and its use of simple distance-from-cluster-center to assign cluster membership leads to poor performance for many real-world situations.
- A Gaussian mixture model (GMM) attempts to find a mixture of multi-dimensional Gaussian probability distributions that best model any input dataset

- CHOOSE THE COVARIANCE TYPE 

	- This hyperparameter controls the degrees of freedom in the shape of each cluster
	- default : `covariance_type="diag"`
	- A slightly simpler and faster model is `covariance_type="spherical"`, which constrains the shape of the cluster such that all dimensions are equal
	- Though GMM is often categorized as a clustering algorithm, fundamentally it is an algorithm for _density estimation_
	
-  **Expectation-Maximization (EM) Algorithm*

	- The Expectation-Maximization (EM) algorithm is an iterative way to find maximum-likelihood estimates for model parameters when the data is incomplete or has some missing data points or has some hidden variables
	- EM chooses some random values for the missing data points and estimates a new set of data
	- In the Expectation-Maximization (EM) algorithm, the estimation step (E-step) and maximization step (M-step) are the two most important steps that are iteratively performed to update the model parameters until the model convergence.

```python
from sklearn.mixture import GMM
gmm = GMM(n_components=4).fit(X)
labels = gmm.predict(X)
plt.scatter(X[:, 0], X[:, 1], c=labels, s=40, cmap='viridis');

gmm = GMM(n_components=4, random_state=42)
plot_gmm(gmm, X)

```

### [Kernel density estimation:](https://jakevdp.github.io/PythonDataScienceHandbook/05.13-kernel-density-estimation.html)

- A density estimator is an algorithm which seeks to model the probability distribution that generated a dataset.
- 1D data use the simple estimator known as histogram.
- A non-parametric method for estimating the probability density function  of a continuous random variable using kernels as weights is known as kernel density estimation (or KDE).Unlike parametric methods, KDE does not assume a specific distribution for the data (e.g., Gaussian, Poisson).

- KDE work 
	- KDE uses a kernel function to assign weights to each data point and "spread" those weights over a region defined by the bandwidth parameter.
	- $f(x)=1\div{nh} \sum^{n}_{i=1}K ((x-x_i)\div h)$
	- Where:

		- f^(x)\hat{f}(x)f^​(x): Estimated density at point xxx.
		- n: Number of data points.
		- x_i​: Data points.
		- h: Bandwidth (smoothing parameter).
		- K: Kernel function.
	- Kernel 
		- Gaussian kernel 
		- Uniform kernel
- Bandwidth:
	- Small Bandwidth
	- Large Bandwidth
- Application 
	- EDA
	- Outlier detection
	- Data imputation
	- Anomaly detection