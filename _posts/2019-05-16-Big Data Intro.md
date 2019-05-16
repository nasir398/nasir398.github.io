---
layout: post
title:  "Big Data Introduction"
date:   2019-05-16
desc: "Getting started with Big Data "
keywords: "Artificial Intelligence, AI, ML, Python, Big Data"
categories: [Python]
tags: [AI, ML, Python, Big Data]
icon: icon-html
---

Big data :

```
Big data is not about large volume of dataset rather it is a solution provided in situation where normal traditional methodologies fail. Big data is defined by three components of dataset 
Volume >> The amount of data generated. 
Velocity >> Frequency at which data is generated, captured and shared. 
Variety >> Actual contents of the dataset. Can be structured or unstructured (  Images, Writings, Videos) 



```


Architecture:
At the core of Big data when traditional architectures fail, Big data distributes the load, resulting in data being saved over hundreds or thousands of servers, faster computation time. 

```

Hadoop:
It is big data solution but is not a database. It is a scalable data storage and batch processing framework. Hadoop ingests, processes, aggregates large amount of external data unstructured or structured. The result can be then passed on to any software system which is independent of Hadoop systems. It consists of several services:
Hadoop common :  These are the basic functions that Hadoop provides and used by most other modules. 
HDFS (Hadoop Distributed File System) : The distributed file system used to store the data. 
Hadoop YARN : Module for scheduling and execution of data processing. 
Hadoop MapReduce : It is a YARN based systems for processing large datasets on the clusters.
Overview of Hadoop cluster 
Start with a large number of virtual or commodity servers and configure them as data nodes where actual big data will be stored. A small number of name nodes will also be configured which contain the information where data resides. 
When a client requests a write query it is being sent to one name node which writes it in one of its shelves. The data is copied within the same rack if configured to do so but copy is mandatory done in Hadoop 2.0 to separate rack, providing additional resiliency.  This copying of data is managed internally over all of the data nodes and its information is being stored at Name Node. 
Parallel data processing:
YARN stands for Yet Another Resource Negotiator and uses a global resource manager and for each application master. This application master handles job distribution among the nodes. 
Jobs by client are sent to resource manager which reside on name node, which then decides which data node should handle the job. This is done by communicating with Node manager demon running on all data nodes. Node managers monitor containers on the node to see memory usage and report back to resource manager. Resource manager then decides on which node the application master will run based on report from containers.  Application master on each node is responsible for running the application on each node.  


```
Big Data Jobs Types :
Ways to process data in this architecture all supported by YARN:
MapReduce: It is a programming model for distrusted processing of large datasets either structured or unstructured.  Each user defined job has two phase:
Map: Parallel share network process of input, which delegates tasks to distributed clusters. 
Reduce: User defined phase for the output of Map phase aggregated. This solves the problem and results in single value output. 
Hive: 
Hive is a data warehouse infrastructure for analyzing of large data sets by using HQL ( Hive query language) , which is very similar to SQL. It allows user query unstructured data using query and provides easy data summarization, analysis of large volumes of data, Adhoc query
Pig:
High level programming language that reduces complexity of data analysis tasks via Pig Latin language. This is a simple language that combines SQL with procedures qualities of MapReduce.  


```



---
