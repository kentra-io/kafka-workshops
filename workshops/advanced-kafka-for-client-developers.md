# Advanced Apache Kafka for Developers of client applications
### 2 day workshop

## About this workshop

This intensive course is for experienced developers of Kafka client applications who want to deepen their understanding of the platform. You will learn to build performant, resilient applications, avoid data loss, and confidently navigate the tradeoffs between latency, throughput, and consistency. We will also explore strategies for cost efficiency and introduce open-source tools that solve advanced use cases. 

### Coding exercises

This is a hands-on workshop, so many topics are accompanied by usually small coding exercises.

### What's in scope

We'll go in depth into Kafka Producer API and Consumer API - covering many advanced topics. We'll cover select advanced aspects of Kafka Architecture and recent developments including Tiered Storage and Kafka Queues. This workshop also includes concise modules on testing Kafka clients, Spring Boot integration and Data Integration with Kafka Connect.

### What isn't in scope
#### Kafka fundamentals
You should understand how a Kafka cluster works, what are partitions, consumers, producers. You should understand Consumer Groups, Consumers and Offsets.

Some experience in running Kafka client applications in production is strongly preferable.

#### Schema Management & serialization formats
While a very important topic, to keep this workshop focused - schema management is not in scope.

#### Cluster management
This workshop is for developers of client applications, it's not about operating an Apache Kafka cluster, which is usually done by a dedicated team.

#### Kafka Security
To maintain a sharp focus on application performance, resilience, and advanced design patterns, this workshop does not cover security configuration. It is assumed attendees are familiar with the basic security settings required to connect to their clusters.

#### Kafka Streams
Kafka Streams has been part of the Kafka API for years, but its use is diminishing in favour of dedicated Stream Processing platforms like Flink or RisingWave. Because of Kafka Streams complexity, often use cases that would be a good fit are instead implemented using standard Consumer API.

### Prerequisites
- Docker
- Java & basic Spring Boot
- Apache Kafka basics

## Local environment setup

### Docker Compose
#### Kafka
#### Kafka UI
#### Schema Registry
#### Kafka REST Proxy

### Integration testing with Spring Boot
#### Testcontainers
#### @MockitoSpyBean
#### Testing asynchronous code - timeouts

## Kafka Architecture - advanced concepts
### Replication and In-Sync Replicas
#### Unclean leader election
### Cross-AZ Networking
#### Rack awareness & fetch from follower
### Tiered Storage
### Kafka Queues
### Distributed tracing with OpenTelemetry

## Kafka Producer
### Acks & Idempotent producer
### Producer retries
### Message Key and partition assignment
#### Hot partitions
#### Sticky Partitioner
#### Custom Partitioner
### Batching
### Compression

## Kafka Consumer
### Poll timeout
### Poison Pill
### Exactly Once Processing
#### Kafka Transactions
#### Idempotent consumers
### Consumer Rebalancing & ConsumerRebalanceListener
### Non-Blocking Retries
### DLQ (DLT) and when to use it
### Beyond basic Kafka concurrency model
#### Parallel consumer
#### Reactor Kafka

## Data Integration with Kafka
### Single Message Transforms in Kafka Connect
### CDC & Transactional Outbox Pattern
