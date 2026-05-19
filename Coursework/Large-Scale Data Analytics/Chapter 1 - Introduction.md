# 1 - Introduction

---
## 1.1 - What Is Big Data

It's not uniformly defined, but it may be fair to say:

*Big data involves data whose volume, diversity, and complexity requires new techniques, algorithms, and analyses to extract useful data.*

A rough answer may be, if you can solve the problem on your laptop, it is not big data.

---
## 1.2 - Success (and Failure) of Big Data
Various examples of companies and organizations using big data to interpret trends at surprising speeds and with success. 

---
## 1.3 - Big Data Evolution and Definition

Big data is especially relevant in science, business, medicine, industry, energy, etc. CERN generates over 90 petabytes of data per year. 

Big data was organized around 3 'Vs': 
- Volume: How much data there is 
- Velocity: How fast new data arrives
- Variety: Types of data available

Some have added two more:
- Veracity: How trustworthy the data is for the problem
- Value: Is it actually useful data for your problem

### 1.3.1 - The Faces of Big Data

Some problems of big data. 
First, data needs to be *acquired*
Then the data needs to be *stored*
With big data we need a *sophisticated storage infrastructure*
Data needs to be *protected and secured* for *privacy*
The design of *databases* needs to accommodate all of this
Additionally, *data visualization* and *data analytics/mining* are two key areas in data science that contribute directly to the value of data. 

The book focuses on the data analytics things and how to efficiently extract knowledge from big datasets. 

---
## 1.4 - How to Deal with Big Data?
Let's assume we embark on exploring 100 terabytes of data. To begin with, a single machine wouldn't be able to store that data. 

For a trivial example, let's just think about the time to read the data. 

A standard mechanical hard drive disk that reads 160 MB/s would take 200 hours to just read the data. 

What do we do? Well, a divide-and-conquer approach, of course. 

Adding to current resources on a machine is considered *vertical scalability* or *build-up*.

Adding more machines is called *horizontal scalability* or *build-out*.

Horizontal scalability also has the advantage of *fault-tolerance*

The downsides are we need a network to connect these, more sophisticated algorithms, more physical space, higher energy costs for electricity and cooling, and network equipment. 

### 1.4.1 - High Performance Computing versus Big Data Computing
HPC is a cluster of independent computers that are connected using a communication network. It is important to note that an individual application that runs on a node can only access that node's RAM. 

This is called a *distributed memory* structure. 

In an HPC cluster, one node will usually act as the *master node* and be in charge of orchestrating all of the communication and synchronization across the nodes of the cluster. The remaining nodes, *the workers*, will perform actual calculations. 

One classical way of dealing with distributed computing is with MPI (Message Passing Interface). A protocol used in two main functions, scatter and gather. The former sends a message to the computing/worker nodes and the latter collects the results. 

One issue with MPI is you need to explicitly determine what each node is going to do. 

In general, HPC is set up for huge calculations with relatively small data (This is what I use it for, calculating atomic trajectories for example), and so big data problems simply do not scale up. In summary, HPC is not big data. 

**What do we have to do differently to tackle data intensive jobs?**