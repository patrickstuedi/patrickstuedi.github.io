---
layout: page
permalink: /code/
title: Code
tags: [code]
modified: 3-10-2014
comments: false
---

I like building hardware-aware software and distributed systems. Here is a list of my current and recent projects with code I have written over the years:

### Apache Crail

Crail is a distributed data store for ephemeral data designed from scratch for fast networking hardware (100Gb/s RoCE, IB) and byte addresssable storage (DRAM, NVMe Flash). Crail leverages user-level I/O (RDMA, NVMe-oF) to achieve ultra low data access latencies, high IOPS and line speed bandwidth. Crail can be used to accelerate data access in distributed data processing like Spark, Presto, Hive, etc. 
<br><br>
[https://github.com/apache/incubator-crail](https://github.com/apache/incubator-crail)
<br>
[https://crail.apache.org](https://crail.apache.org)

### Crail Native

Crail Native is a C++/Python implementation of Crail geared towards fast distributed temporary storage in machine learning worklflows. Crail native is compatible with Apache Crail and can be used as temporary storage space in job pipelines consisting of different frameworks. For instance, in a image recognition model training worklflow a Spark job may be used to pre-process raw image data and store it on Apache Crail, followed by a distributed Tensorflow job running the actual training using Crail Native to access the pre-processed data set.  

### DiSNI

DiSNI is a Java library for direct storage and networking access from userspace. It provides an RDMA interface to access remote memory. DiSNI enables the development of Java applications for high performance RDMA networks, such as InfiniBand, iWARP, or RoCE. The RDMA API is implemented based on the Open Fabrics Enterprise Distribution (OFED) RDMA user libraries. It provides RDMA semantics including asynchronous operations, zero-copy transmission and direct data placement. 
<br><br>
[https://github.com/zrlio/disni](https://github.com/zrlio/disni)

### DaRPC

DaRPC is an RDMA based RPC framework designed to provide ultra-low latencies. DaRPC efficiently distributes computation, network resources and RPC resources across cores and memory to achieve a high aggregate throughput (2-3M ops/sec) at a very low per-request latency (5μs with Infiniband). DaRPC is used by Crail to communicate between the Crail metadata server and Crail clients. 
<br><br>
[https://github.com/zrlio/darpc](https://github.com/zrlio/darpc)

### Spark-IO

Crail-Spark-IO contains various I/O accleration plugins for Spark tailored to high-performance network and storage hardware (RDMA, NVMef, etc.). Spark-IO is based on Crail, a fast multi-tiered distributed storage system. Spark-IO currently contains two IO plugins: a shuffle engine and a broadcast module. Both plugins inherit all the benefits of Crail such as very high performance (throughput and latency) and multi-tiering (e.g., DRAM and flash).
<br><br>
[https://github.com/zrlio/crail-spark-io](https://github.com/zrlio/crail-spark-io)


### NaRPC

NaRPC is a simple TCP based RPC library. NaRPC follows the same design as DaRPC where client requests are served by per-core handlers in-place, that is, without additional thread-pool. Therefore, similar to DaRPC, NaRPC is useful for small size RPC requests that require little computation on the server side and where high total throughput and low latency are the desired performance targets. 
<br><br>
[https://github.com/zrlio/narpc](https://github.com/zrlio/narpc)

### Crail YCSB Benchmark

Crail YCSB is a module in the official YCSB benchmark suite. It can be used to benchmark the key-value interface in Crail.
<br><br>
[Crail-YCSB-module](https://github.com/brianfrankcooper/YCSB/tree/master/crail)

