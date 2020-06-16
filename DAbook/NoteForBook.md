#Getting Started with pandas

##Essential Functionality 
###Reindexing
Create a new index for dataframe or series
There are some tool for fill the data if there are new indexes. (ffil, bfill)

###Dropping entries from an axis

###Indexing, selection, and filtering
Use **iloc** instead of **ix** to select a particular position in dataframe

###Arithmetic and data alignment
Do numpy in pandas wont change type of pandas.

###Function application and mapping
Use **lambda** to make a operator would be great

###Sorting and ranking
Syntax: sort_index(axis=?), rank

In dataframe, it can be sort by a column or row.

###Axis indexes with duplicate values



##Summarizing and Computing Descriptive Statistics
###Correlation and Covariance
Need definition for 2 of these.

###Unique Values, Value Counts, and Membership
Note that only **Series** has *value_count*. In dataframe, we need to use *dataframe.apply(pd.value_count)*, it will return the frequency of every different object in each column of the dataframe.


##Handling Missing Data
Syntax: dropna, fillna, isnull, notnull
###Filtering Out Missing Data
how='all' will drop rows that are all NA
what is thresh?

###Filling in Missing Data
inplace=True is make a new one with changes


##Hierarchical Indexing
Hierarchical indexing is an important feature of pandas enabling you to have multiple index levels on an axis.
Example:
'''
data = Series(np.random.randn(10),
.....:		index=[['a', 'a', 'a', 'b', 'b', 'b', 'c', 'c', 'd', 'd'],
.....:			[1, 2, 3, 1, 2, 3, 1, 2, 2, 3]])

'''

*This data can be changed to be dataframe by unstack()*

There are many example of complex hierarchical index data.
Dataframe can be represented like this:
'''
frame = DataFrame(np.arange(12).reshape((4, 3)),
 			index=[['a', 'a', 'b', 'b'], [1, 2, 1, 2]],
 			columns=[['Ohio', 'Ohio', 'Colorado'],
 				['Green', 'Red', 'Green']])
'''


###Reordering and Sorting Levels
When **sort** data that has hierarchical indexes, we need to notice the level. Sort which level?

###Summary Statistics by Level
Do operation by levels

###Using a DataFrame’s Columns
You can use columns of dataframe to be index. Syntax: set_index() default is drop the columns that are used to be indexes

#Data Loading, Storage, and File Formats

##Reading and Writing Data in Text Format
There are many data follow up these:
1. *Indexing*: this data is not defined names. So the the names of columns can be in the columns of data
2. *Type inference and data conversion*: this data you dont have any information of columns' type 
3. *Datetime parsing*: includes combining capability, including combining date and time information spread over multiple columns into single column
4. *Iterating*:
5. *Unclean data issues*: skipping rows or a footer, comments, or other minor things like numeric data with thousands separated by commas


**Technique**
![image](pic/data_with_special_character.png)
