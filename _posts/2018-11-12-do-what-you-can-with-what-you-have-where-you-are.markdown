---
layout: post
title:  What is Amazon dynamodb and how to use it?
date:   2018-11-12 15:01:35 +0300
image:  '/images/post1.png'
tags:   [AWS, Nosql_dababase, key_value_db, documnet_db]
---
Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. DynamoDB lets you offload the administrative burdens of operating and scaling a distributed database so that you don't have to worry about hardware provisioning, setup and configuration, replication, software patching, or cluster scaling. DynamoDB also offers encryption at rest, which eliminates the operational burden and complexity involved in protecting sensitive data. 

> What is dynamodb? Here is a short introduction from my youtube channel :)

<p><iframe src="https://www.youtube.com/embed/1jEljwiSvfU" frameborder="0" allowfullscreen></iframe></p>

> If you want to know how to run dynamodb in docker and play around with it on AWS, here is an instruction that you can use.

<p><iframe src="https://www.youtube.com/embed/oTUo7HHW45s" frameborder="0" allowfullscreen></iframe></p>

> Benefits of DynamoDB:

Scalability and Performance: Using Amazon DynamoDB, Developers can combine incremental scalability and high performance with the ease of cloud administration, reliability and table data model and thus can meet the customer demand. It can scale the table assets to a large number of servers on various Availability Zones for addressing storage need. In addition, there is no specific limit to the quantity of data that a table can store. As a result, any amount of data can be stored and retrieved and Dynamo DB shared data across more servers with the increase of data stored in a table.

Cross-region Replication: It enables you to maintain identical copies as replicas of a DynamoDB master table in one or more AWS regions. Once you enable cross-region replication for a table, identical copies of the table are created in other AWS areas. Any mode of changes in the table will be consequently propagated to all replicas.

TTL (Time to Live): TTL is a process that gives you an opportunity to set a specific timestamp to delete expired data from your tables. Once the timestamp expires, the relating item is marked as expired and is subsequently deleted from the table. By using this functionality, you don’t need to track expired data and delete it manually. TTL can help you reduce storage usage and reduce the cost of storing data that is no longer important.

Fine-grained Access Control: Fine-Grained Access Control gives a DynamoDB table owner a high level of control over data in the table. In particular, the table owner can specify who can access which data or attributes of the table and perform what actions such as read-write or update. Fine-Grained Access Control is used in combination with AWS Identity and Access Management, which manages the security credentials and the related permissions.

Stream: Using the DynamoDB Streams, developers can update and receive the item-level data before and after data are changed. DynamoDB Streams provides a time-ordered sequence of data changes made in a table in the last 24 hours. You can access a stream with a simple API call and use it to keep other data stores updated with the latest changes and take actions based on it.

> Tables, Items, and Attributes

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/post2.gif" alt="Project">
  </div>
</div>

The following are the basic DynamoDB components:

Tables — Similar to other database systems, DynamoDB stores data in tables. A table is a collection of data. For example, see the example table called People that you could use to store personal contact information about friends, family, or anyone else of interest. You could also have a Cars table to store information about vehicles that people drive.

Items — Each table contains zero or more items. An item is a group of attributes that is uniquely identifiable among all of the other items. In a People table, each item represents a person. For a Cars table, each item represents one vehicle. Items in DynamoDB are similar in many ways to rows, records, or tuples in other database systems. In DynamoDB, there is no limit to the number of items you can store in a table.

Attributes — Each item is composed of one or more attributes. An attribute is a fundamental data element, something that does not need to be broken down any further. For example, an item in a People table contains attributes called PersonID, LastName, FirstName, and so on. For a Department table, an item might have attributes such as DepartmentID, Name, Manager, and so on. Attributes in DynamoDB are similar in many ways to fields or columns in other database systems.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/post3.png" alt="Project">
  </div>
</div>

Note the following about the People table:
Each item in the table has a unique identifier, or primary key, that distinguishes the item from all of the others in the table. In the People table, the primary key consists of one attribute (PersonID).
Other than the primary key, the People table is schema-less, which means that neither the attributes nor their data types need to be defined beforehand. Each item can have its own distinct attributes.
Most of the attributes are scalar, which means that they can have only one value. Strings and numbers are common examples of scalars.
Some of the items have a nested attribute (Address). DynamoDB supports nested attributes up to 32 levels deep.


When you create a table, in addition to the table name, you must specify the primary key of the table. The primary key uniquely identifies each item in the table, so that no two items can have the same key.

> DynamoDB supports two different kinds of primary keys:

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/post4.jfif" alt="Project">
  </div>
</div>

Partition key — A simple primary key, composed of one attribute known as the partition key.

DynamoDB uses the partition key’s value as input to an internal hash function. The output from the hash function determines the partition (physical storage internal to DynamoDB) in which the item will be stored.

In a table that has only a partition key, no two items can have the same partition key value.

The People table described in Tables, Items, and Attributes is an example of a table with a simple primary key (PersonID). You can access any item in the People table directly by providing the PersonId value for that item.

Partition key and sort key — Referred to as a composite primary key, this type of key is composed of two attributes. The first attribute is the partition key, and the second attribute is the sort key.

DynamoDB uses the partition key value as input to an internal hash function. The output from the hash function determines the partition (physical storage internal to DynamoDB) in which the item will be stored. All items with the same partition key are stored together, in sorted order by sort key value.

In a table that has a partition key and a sort key, it’s possible for two items to have the same partition key value. However, those two items must have different sort of key values.

> DynamoDB can have three data types

Scalar，
，Set
Document

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/post5.jfif" alt="Project">
  </div>
</div>