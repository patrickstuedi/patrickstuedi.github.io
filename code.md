---
layout: page
permalink: /code/
title: Code
tags: [code]
modified: 3-10-2014
comments: false
---

A list of my recent projects:

### Apache Crail

Crail is a distributed data store designed from scratch for fast networking hardware (100Gb/s RoCE, IB) and byte addresssable storage (DRAM, NVMe Flash). Crail leverages user-level I/O (RDMA, NVMe-oF) to achieve ultra low data access latencies, high IOPS and line speed bandwidth. Crail can be used to accelerate data access in distributed data processing and machine learning frameworks like Spark, Tensorflow, PyTorch, etc. 
<br>
:octocat: https://github.com/apache/incubator-crail
<br>
Website: https://crail.apache.org

### DaRPC

DaRPC is an RDMA based RPC framework designed to provide ultra-low latencies. DaRPC efficiently distributes computation, network resources and RPC resources across cores and memory to achieve a high aggregate throughput (2-3M ops/sec) at a very low per-request latency (5μs with Infiniband). DaRPC is used by Crail to communicate between the Crail metadata server and Crail clients. 

### DiSNI

DiSNI is a Java library for direct storage and networking access from userspace. It provides an RDMA interface to access remote memory. DiSNI enables the development of Java applications for high performance RDMA networks, such as InfiniBand, iWARP, or RoCE. The RDMA API is implemented based on the Open Fabrics Enterprise Distribution (OFED) RDMA user libraries. It provides RDMA semantics including asynchronous operations, zero-copy transmission and direct data placement. 

### Spark-IO

Crail-Spark-IO contains various I/O accleration plugins for Spark tailored to high-performance network and storage hardware (RDMA, NVMef, etc.). Spark-IO is based on Crail, a fast multi-tiered distributed storage system. Spark-IO currently contains two IO plugins: a shuffle engine and a broadcast module. Both plugins inherit all the benefits of Crail such as very high performance (throughput and latency) and multi-tiering (e.g., DRAM and flash).


### NaRPC

NaRPC is a simple TCP based RPC library. 
