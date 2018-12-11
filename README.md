# Database Prototype System

## A database prototype system follow UCI CS222P

https://grape.ics.uci.edu/wiki/public/wiki/cs222p-2017-fall

Written in C++. Implemented with seperate test cases.


## Record-Based File Manager (/rbf) by Bicheng Wang:

Builds up the basic file system required for relation manager, index manager, and query engine.

  Including:
  
    (1) Paged file system: which provides functionalities for higher-level control of paged file I/O;
    
    (2) Record-based file system: handles CRUD in paged file system for records, support data of variable length


## Relation Manager (/rm) by Xingyu Wu

Relation management is implemented based on the record-based file system.

  Including:

    (1) Meta info table
  
    (2) Two main tables: tables' table and columns' table.

    (3) Other user tables.


## Index Manager (/ix) by Bicheng Wang & Xingyu Wu

Unclustered B+ tree is implemented to support range queries.
  
support data insert, update, delete, and bulk-load.


## Query Engine (/qe) by Xingyu Wu & Bicheng Wang

Based on all above components, this query engine includes:
  
    (1) Relation Manager index scan iterator.
 
    (2) Filter Interface: filter the tuple by selection condition. 
 
    (3) Projection Interface: project the value of attributes.
 
    (4) Block Nested-Loop Join Interface: takes two iterators, leftIn as outer, rightIn as inner relation.
 
    (5) Index Nested-Loop Join Interface: based on nested loop to join.
 
    (6) Grace-Hash Join Interface: support "equal" join.
 
    (7) Aggregation Interface: support max, min, sum, average, count.
