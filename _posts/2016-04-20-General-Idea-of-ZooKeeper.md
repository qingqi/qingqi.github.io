---
layout: post
title: General Idea of ZooKeeper
excerpt: "quick start for ZooKeeper"
modified: 2016-04-20
tags: [intro, beginner, basics, ZooKeeper, tutorial]
comments: true
---

At Apache ZooKeeper official website[^1], it says:

**ZooKeeper is an open-source, highly reliable, distributed coordination server.** 

What does coordination server mean? Generally, it means that distributed processes can coordinate their behavior through the ZooKeeper servers. We can view ZooKeeper as a cluster of servers which maintain a tree structure of data nodes. The tree structure is analogous with standard file system. However, unlike directories, intermediate ZooKeeper nodes can also contain data. Distributed processes can get and set data on the data nodes to coordinate their behavior. Each ZooKeeper server will contain its own copy of the hierarchical data nodes. ZooKeeper clients establish connetions to one of the ZooKeeper servers. Data updates on one node will propogate to other ZooKeeper servers.

ZooKeeper is a distributed lock manager[^2], and provides similar services as Google Chubby[^3].

Some usage of ZooKeeper can be found at [Some usage of ZooKeeper](https://zookeeper.apache.org/doc/r3.5.0-alpha/recipes.html).

[^1]: [ZooKeeper Overview](http://zookeeper.apache.org/doc/trunk/zookeeperOver.html)
[^2]: [Distributed Lock Manager](https://en.wikipedia.org/wiki/Distributed_lock_manager)
[^3]: [Google Chubby](http://research.google.com/archive/chubby.html)