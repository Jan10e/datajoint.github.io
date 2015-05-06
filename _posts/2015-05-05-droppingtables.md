---
layout: post
title: 'Dropping tables'
summary: 'How to completely remove tables from the database'
tags: ['tutorial','matlab','python','help']
---

To _drop a table_ means to remove the table from the database and all its dependent tables recursively with all their contents without removing its MATLAB class definition files. If there are any data in the tables to be dropped, DataJoint will report the total number of tuples and will prompt for an additional confirmation before dropping. 

Dropping tables is often necessary when the table definition needs to be significantly modified or when the table is no longer necessary. Remember that the table will be created again automatically upon the next instantiation of its base relvar class, so if you want to ensure that the table never comes back, delete its class definition file as well.

## Matlab

All [base relvars]({% post_url 2015-05-05-baserelvars %}) have the constant property **table** of type **dj.Table**, which provides access to the table definition. 


For example, to drop the table of the class `tp.Segmentation`

```
>> tp.Segmentation.table.drop
```

See also

```
>> help dj.Table/drop
```

## Python 

TODO