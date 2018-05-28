# Create-and-manage-relationships-in-Power-BI-Desktop

#### Objective:-

When you import multiple tables, chances are you’re going to do some analysis using data from all those tables. Relationships between those tables are necessary in order to accurately calculate results and display the correct information in your reports. Power BI Desktop makes creating those relationships easy. In-fact, in most cases you won’t have to do anything, the Autodetect feature can do it for you. However, in some cases you might have to create relationships yourself, or you might need to make some changes to a relationship. Either way, it’s important to understand relationships in Power BI Desktop and how to create and edit them.

## Create a relationship manually :-
#### 1) On the Home tab, click Manage Relationships 

![alt text](https://drive.google.com/uc?id=1E2jl4ycD-M2CfRpJ2azcIDiu9wim-nHa)

#### 2) Click on the New Tab.

![alt text](https://drive.google.com/uc?id=1CGpcPyCmNgjDUAvi6Q2x4YMKR0MWeU5a)



![alt text](https://drive.google.com/uc?id=1IdKmACESzs3kzhzbn2uM9KfNWr3BSxEe)


In the Create Relationship dialog, in the first table drop-down list, select a table, and then select the column you want to use in the relationship.
In the to second table drop-down list, select the other table you want in the relationship, then select the other column you want to use, and then click OK.

![alt text](https://drive.google.com/uc?id=1ijg75eSKi2MO0xxMrBtqOG7THdSAuwVx)


By default, Power BI Desktop will automatically configure the Cardinality (direction), Cross filter direction, and Active properties for your new relationship; however, you can change these if necessary. 

Edit a relationship
1. On the Home tab, click Manage Relationships.
2. In the Manage Relationships dialog, select the relationship, then click Edit.
Configure additional options
When you create or edit a relationship, you can configure additional options. By default, additional options are automatically configured based on a best guess. This can be different for each relationship based on the data in the columns.


### Cardinality
Many to One (*:1) - This is the most common, default type. This means the column in one table can have more than one instance of a value, and the other related table, often know as the Lookup table, has only one instance of a value.
One to One (1:1) - This means the column in one table has only one instance of a particular value, and the other related table has only one instance of a particular value.
#### Cross filter direction
###### Both :- 
This is the most common, default direction. This means for filtering purposes, both tables are treated as if they're a single table. This works well with a single table that has a number of lookup tables that surround it. An example is a Sales actuals table with a lookup table for department. This is often called a Star schema configuration (a central table with several lookup tables.) However, if you have two or more tables that also have lookup tables (with some in common) then you wouldn't want to use the Both setting. To continue the previous example, in this case, you also have a budget sales table that records target budget for each department. And, the department table is connected to both the sales and the budget table. Avoid the Both setting for this kind of configuration.

###### Single:- 
This means that filtering choices in connected tables work on the table where values are being aggregated. If you import a Power Pivot in Excel 2013 or earlier data model, all relationships will have a single direction.

#### Make this relationship active

When checked, this means the relationship serves as the active, default relationship. In cases where there is more than one relationship between two tables, the active relationship provides a way for Power BI Desktop to automatically create visualizations that include both tables.
