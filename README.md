# kafka-real-time-data-anlysis


In this project, you will execute an End-To-End Data Engineering Project on Real-Time Stock Market Data using Kafka.

We are going to use different technologies such as Python, Amazon Web Services (AWS), Apache Kafka, Glue, Athena, and SQL.

This project is modified based on https://github.com/darshilparmar/stock-market-kafka-data-engineering-project.

## The data problem
- You need a way to send data to a central storage quickly
- Because machines frequently fail, you also need the ability to have your data replicated, so those inevitable failures don't cause downtime and data loss
That's where Apache Kafka comes in as an effective solution. Apache Kafka is a publish-subscribe based durable messaging system developed by Linkedin.

## Why use Kafka?
- Multiple producers and consumers at any given time without interfering with each other. This is in contrast to many queuing system where once a message is consumed by one client
- Disk-Based retention:
  - Consumers do not always need to work in real time. Messages are commited to disk and stay for some periods of time.
  - There is no danger of losing data.
- Fast: Kafka is a good solution for applications that require a high througput, low latency messaging solution. Kafka can write up to 2 million requests per second
- Scalable:
  - Expansions can be performed while the cluster is online, with no impact on the availability of the system as a whole.
- High Performance: Excellent performance under high load.
