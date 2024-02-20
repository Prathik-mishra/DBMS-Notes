# DBMS

## Keys

Keys are one of the basic requirements of a relational database model. It is widely used to identify the tuples(rows) uniquely in the table. We also use keys to set up relations amongst various columns and tables of a relational database.

### Different Types of Database Keys:
* Candidate Key
* Primary Key
* Super Key
* Alternate Key
* Foreign Key
* Composite Key

## Candidate Key
The minimal set of attributes that can uniquely identify a tuple is known as a candidate key. For Example, STUD_NO in STUDENT relation. 

* It is a minimal super key.
* It is a super key with no repeated data is called a candidate key.
* The minimal set of attributes that can uniquely identify a record.
* It must contain unique values.
* It can contain NULL values.
* Every table must have at least a single candidate key.
* A table can have multiple candidate keys but only one primary key.
* The value of the Candidate Key is unique and may be null for a tuple.
* There can be more than one candidate key in a relationship. 

## Primary Key
There can be more than one candidate key in relation out of which one can be chosen as the primary key. For Example, STUD_NO, as well as STUD_PHONE, are candidate keys for relation STUDENT but STUD_NO can be chosen as the primary key (only one out of many candidate keys). 

* It is a unique key.
* It can identify only one tuple (a record) at a time.
* It has no duplicate values, it has unique values.
* It cannot be NULL.
* Primary keys are not necessarily to be a single column, more than one column can also be a primary key for a table.

## Super Key
The set of attributes that can uniquely identify a tuple is known as Super Key. For Example, STUD_NO, (STUD_NO, STUD_NAME), etc. A super key is a group of single or multiple keys that identifies rows in a table. It supports NULL values. 

* Adding zero or more attributes to the candidate key generates the super key.
* A candidate key is a super key but vice versa is not true.
* Super Key values may also be NULL.

## Alternate Key
The candidate key other than the primary key is called an alternate key.

* All the keys which are not primary keys are called alternate keys.
* It is a secondary key.
* It contains two or more fields to identify two or more records.
These values are repeated.

## Foreign Key
If an attribute can only take the values which are present as values of some other attribute, it will be a foreign key to the attribute to which it refers. The relation which is being referenced is called referenced relation and the corresponding attribute is called referenced attribute the relation which refers to the referenced relation is called referencing relation and the corresponding attribute is called referencing attribute. The referenced attribute of the referenced relation should be the primary key to it.

* It is a key it acts as a primary key in one table and it acts as 
secondary key in another table.
* It combines two or more relations (tables) at a time.
* They act as a cross-reference between the tables.

## Composite Key
Sometimes, a table might not have a single column/attribute that uniquely identifies all the records of a table. To uniquely identify rows of a table, a combination of two or more columns/attributes can be used.  It still can give duplicate values in rare cases. So, we need to find the optimal set of attributes that can uniquely identify rows in a table.

* It acts as a primary key if there is no primary key in a table
* Two or more attributes are used together to make a composite key.
* Different combinations of attributes may give different accuracy in terms of identifying the rows uniquely.


# Database Normalization

## Overview

Database Normalization is a crucial concept in Database Management Systems (DBMS) that aims to organize data efficiently, reduce redundancy, and enhance data integrity. It is a process of structuring a relational database to eliminate data anomalies and improve overall database performance. This README provides a brief overview of normalization and its various forms.

## Table of Contents

1. [Introduction](#introduction)
2. [Benefits of Normalization](#benefits-of-normalization)
3. [Normalization Forms](#normalization-forms)
   - [First Normal Form (1NF)](#first-normal-form-1nf)
   - [Second Normal Form (2NF)](#second-normal-form-2nf)
   - [Third Normal Form (3NF)](#third-normal-form-3nf)
   - [Boyce-Codd Normal Form (BCNF)](#boyce-codd-normal-form-bcnf)
   - [Fourth Normal Form (4NF)](#fourth-normal-form-4nf)
   - [Fifth Normal Form (5NF)](#fifth-normal-form-5nf)
4. [How to Normalize a Database](#how-to-normalize-a-database)
5. [Conclusion](#conclusion)

## Introduction

Normalization is the process of organizing and structuring data in a relational database to minimize redundancy and dependency. The goal is to achieve a database design that ensures data integrity, reduces data duplication, and facilitates efficient data retrieval.

## Benefits of Normalization

- **Data Integrity:** Normalization reduces the risk of data anomalies such as insertion, update, and deletion anomalies, ensuring that data remains accurate and consistent.

- **Efficient Storage:** By eliminating redundant data, normalization optimizes storage space, leading to more efficient use of resources.

- **Improved Query Performance:** Well-normalized databases generally perform better in terms of query speed and efficiency.

- **Simplified Maintenance:** Normalized databases are easier to maintain and modify, as changes can be made to a smaller, well-defined set of tables.

## Normalization Forms

### First Normal Form (1NF)

- Ensures that each column in a table contains atomic (indivisible) values, and there are no repeating groups or arrays.

### Second Normal Form (2NF)

- Builds on 1NF and eliminates partial dependencies by ensuring that non-prime attributes are fully functionally dependent on the primary key.

### Third Normal Form (3NF)

- Extends the normalization process by removing transitive dependencies, ensuring that no non-prime attribute depends on another non-prime attribute.

### Boyce-Codd Normal Form (BCNF)

- A stricter form of 3NF, where every non-trivial functional dependency is a superkey.

### Fourth Normal Form (4NF)

- Addresses multi-valued dependencies, ensuring that a table is free from certain types of redundancy related to multi-valued attributes.

### Fifth Normal Form (5NF)

- Deals with cases where a table contains join dependencies, aiming to further reduce redundancy in complex database structures.

## How to Normalize a Database

1. Identify the functional dependencies within the data.
2. Define primary keys for each table.
3. Apply normalization forms iteratively, starting from 1NF and progressing to higher normal forms.

## Conclusion

Database normalization is a fundamental concept in database design that plays a crucial role in maintaining data integrity and optimizing database performance. Understanding the various normalization forms and applying them appropriately can lead to a well-structured and efficient relational database.
