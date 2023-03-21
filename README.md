# kafka-real-time-data-analysis

In this project, you will execute an End-To-End Data Engineering Project on Real-Time Stock Market Data using Kafka.

We are going to use different technologies such as Python, Amazon Web Services (AWS), Apache Kafka, Zookeeper, Glue,
Athena, and
S3.

This project is modified based on https://github.com/darshilparmar/stock-market-kafka-data-engineering-project.

## Architecture

![Architecture](Architecture.jpg)

## What is Kafka?

Apache Kafka is a distributed event store and stream processing platform. It is used for building real-time data
pipelines and streaming apps. It is horizontally scalable, fault-tolerant, wicked fast, and runs in production in
thousands of companies.

## ZooKeeper Basics

- Open source Apache project
- Distributed key-value store
- Maintains configuration information, naming, providing distributed synchronization, and providing group services
- Stores ACLs(Access Control List) and Secrets
- Enables highly reliable distributed coordination
- Provides distributed synchronization

## Producer Basics

- Producer writes Data as Messages
- Can be written in any language
- Command Line Producer Tool

## Broker Basics

- Producer sends Messages to Broker
- Broker receives and store Messages
- A Kafka cluster can have many Brokers
- Each Broker manages multiple Partitions

## Consumer Basics

- Consumer pulls Messages from 1..n topics
- New inflowing Messages are automatically retrieved
- Consumer offset
    - keeps track of the last message read
    - is stored in specific topic
- CLI tools exist to read from cluster

## The data problem

- You need a way to send data to a central storage quickly
- Because machines frequently fail, you also need the ability to have your data replicated, so those inevitable failures
  don't cause downtime and data loss
  That's where Apache Kafka comes in as an effective solution. Apache Kafka is a publish-subscribe based durable
  messaging system developed by LinkedIn.

## Why use Kafka?

- Multiple producers and consumers at any given time without interfering with each other. This is in contrast to many
  queuing system where once a message is consumed by one client
- Disk-Based retention:
    - Consumers do not always need to work in real time. Messages are committed to disk and stay for some periods of
      time.
    - There is no danger of losing data.
- Fast: Kafka is a good solution for applications that require a high throughput, low latency messaging solution. Kafka
  can write up to 2 million requests per second
- Scalable:
    - Expansions can be performed while the cluster is online, with no impact on the availability of the system as a
      whole.
- High Performance: Excellent performance under high load.

## [S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data
availability, security, and performance.

## [Glue](https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html)

AWS Glue is a serverless data integration service that makes it easy for analytics users to discover, prepare, move, and
integrate data from multiple sources. You can use it for analytics, machine learning, and application development. It
also includes additional productivity and data ops tooling for authoring, running jobs, and implementing business
workflows.

## [Athena](https://docs.aws.amazon.com/athena/latest/ug/what-is.html)

Amazon Athena is an interactive query service that makes it easy to analyze data directly in Amazon Simple Storage
Service (Amazon S3) using standard SQL. With a few actions in the AWS Management Console, you can point Athena at your
data stored in Amazon S3 and begin using standard SQL to run ad-hoc queries and get results in seconds.

## Command

- `bin/zookeeper-server-start.sh config/zookeeper.properties` start zookeeper