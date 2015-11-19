---
layout: post
title: "Efficient Data Searching"
date: 2015-08-08 12:03:41 +0530
comments: true
categories: 
---

We use different technique to search data from our day to day life. Such as, while we are reading a book and we needed a particulr concept again and again, then we might search the concept either of the following list or some creativity searching criteria:-

+ If we know the concept present in particulr page, then access it directly. Here we index: concept-page number (page number is obiviously physical address!!). Here index is of type:- application level index.

+ To access page number we need 3-10 flip. To minimize the flip we can add a marker, so that we can access it in more faster. Here the index is page number-marker, and the index is of physical level index!!

+ We can make a xerox copy of the concept. Here The latency time to search the concept is comparatively smaller than the physical book(It depends where we keep the xerox copy) and same for access time. These concept are related to caching/buffering.

So to optimize for efficient access the data, we might need to understand physical representation of data, index used either in physical level or logical level, caching/buffering strategy, and most importatnly the context where we access data. So I will go through in following order:-

+ Phycsical Representation of Data
+ Index Structure
+ Buffering Strategy

## Phycsical Representation of Data

### Hard disk Structure

<img src="{{ root_url }}/images/harddisk_structure.png" />

From hardware arhitecture of hard disk perspective, it is made up of sector, cylinder, and track. The basic building block of hard disk is sector. To make interaction or communication with hard disk, we need a address mechanism from differnt perspective such as sector number. Some of the addressing mechanism are: [Cylinder-head-sector](https://en.wikipedia.org/wiki/Cylinder-head-sector), [Logical Block Addressing](https://en.wikipedia.org/wiki/Logical_block_addressing). It is the Disk Controller or Disk Driver which abstract way all the complexity and provide a nice intrface to inteact with hard disk wuch as [Serial ATA](https://en.wikipedia.org/wiki/Serial_ATA), and it address the memory with logical block. The interface looks like:-

+ read(address) :- retrun a block of data
+ write(address, data) : It write the data in given address from starting position


We know about file system which operating system provided to abstract way all the complexity of disk driver interfce. So it make a abstraction called file system(database) to manage your file from different perspective what we think a file at present moment. To read about file system from operating system perspective the following resoureces I used to refer:-

##### Emphasis on Storage
+ [Storage Sysetem NPTEL](http://nptel.ac.in/courses/106108058/)
+ [Practical File System Design](http://www.nobius.org/~dbg/)
+ [RAID](http://www.cs.uofs.edu/~mccloske/courses/cmps340/RAID_lec.html)
+ [CS4513 Distributed Computing Systems](http://web.cs.wpi.edu/~cs4513/b05/)

##### Project
+ [RedBase](https://web.stanford.edu/class/cs346/2015/)
+ [Ori A Secure Distributed File System](http://ori.scs.stanford.edu/)

##### Theory about Implementation:
+ [Operating Systems Lecture Notes](http://people.csail.mit.edu/rinard/osnotes/)
+ [6.828-MIT](http://pdos.csail.mit.edu/6.828/2012/reference.html)
+ [Operating Systems: Three Easy Pieces](http://pages.cs.wisc.edu/~remzi/OSTEP/)
+ [Readings in Database Systems](http://redbook.cs.berkeley.edu/redbook3/lecs.html)
+ [Database Reading List](https://github.com/rxin/db-readings)
+ [http://www.cs286.net/home/reading-list](http://www.cs286.net/home/reading-list)


### Index Structure


