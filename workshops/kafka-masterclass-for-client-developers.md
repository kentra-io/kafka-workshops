# Kafka Masterclass for Developers of client applications
### 4 day workshop

## Why take this workshop
It's easy to start using Kafka clients in your applications - but without in-depth understanding it's easy to overlook critical aspects that might cause data loss or data corruption. You might also waste a lot of time solving well-known problems in a suboptimal way, or miss out on important features that can significantly reduce your cloud costs.


## Scope of the workshop 
This workshop will give you a comprehensive overview of everything you need to know when building applications that produce or consume Kafka messages. It goes in depth into Kafka architecture, Producer API, Consumer API and provides and introduction into Kafka Connect and Debezium.

You'll learn about native Java client, but after that we'll be working in Spring Boot - as the most popular framework that Java applications are created in. You'll learn how to configure the application, understand its behaviour, get familiar with different delivery semantics, and how to set up error handling in a bulletproof, efficient way.

You'll learn how to write clean and comprehensive integration tests, how to use and manage schemas, how Kafka security works, and how you can leverage Kafka Connect and Debezium.

Since we'll be focusing on how to build production-ready applications, we'll also cover distributed tracing and relevant monitoring metrics - both for Kafka clients (producer and consumer metrics) as well as Kafka topics.

## What won't be covered:

### Managing and operating a Kafka cluster
This workshop is for developers of client applications, it's not about operating an Apache Kafka cluster, which is usually done by a dedicated team.

### Kafka Streams
Kafka Streams has been part of the Kafka API for years, but its use is diminishing in favour of dedicated Stream Processing platforms like Flink or RisingWave. Because of Kafka Streams complexity, often use cases that would be a good fit are instead implemented using standard Consumer API.

## Required foundations
Previous experience with Kafka is not necessary - we'll start from the foundations, but it's important to have good Software Engineering foundations - Kafka clients are communicating asynchronously with a distributed system, so to get the most out of this workshop - it's best to have a few years of experience. You'll also need to know how to work with Docker, and have basic understanding of Java and Spring.

# Structure of the workshop

## Kafka Architecture
### Introduction to Apache Kafka
### Main use cases
### Data model 
### Cluster architecture
### Advanced Kafka Architecture
#### KRaft - metadata consensus protocol
#### Replication & In-Sync replicas

## Local environment setup

### Docker Compose - local Kafka setup
#### Kafka
#### Kafka UI
#### Schema Registry
#### Kafka REST Proxy

### Java client
#### Java producer
#### Java consumer

### Spring boot client
#### Producing messages
#### Consuming messages

### Integration tests with Testcontainers
##### Testcontainers configuration
##### @MockitoSpyBean
##### Testing asynchronous code - timeouts

## Kafka Producers
### Message Key and partition assignment
#### Partition assignment
##### Message Key & Sticky Partitioner
##### Custom Partitioner
#### Impact of partitioning, Hot Partitions
### Producer delivery semantics
#### Acks
#### Idempotent producer
### Serialization
### Batching
### Compression
### Retries

## Kafka Consumers
### How consumers work
#### Consumer Group, Consumer and Partition assignment
#### Offsets and Commits
#### Fetch, Poll and Commit
#### Auto offset reset
### Processing semantics
#### At least once, at most once
#### Exactly once - Kafka Transactions
#### Exactly once - Consumer idempotency
### Consumer error handling strategies
#### What's a Poison Pill
#### Non-Blocking Retries
#### DLQ (DLT) and when to use it
### Kafka Queues (introduced in Kafka 4.0)
### Advanced Consumer topics
#### Consumer Rebalancing & ConsumerRebalanceListener
#### Poll timeout

## Schema Management
### How Schema Registry works with Kafka clients
### Serialization formats
### SubjectNameStrategy and when to use which
### Schema evolution

## Kafka Security
### Encryption in motion (TLS)
### Encryption at rest & client-side encryption
### Authentication (mTLS, SASL)
### Authorization - Access Control Lists

## Data integration with Kafka
### Kafka Connect
#### Single Message Transforms
### CDC & Debezium
#### Transactional Outbox pattern
### Can I query my Kafka topic?

## Advanced Kafka Concepts
### Cross-AZ traffic
#### Rack-awareness
#### Fetch From Follower
### Distributed tracing with Open Telemetry
### Monitoring
#### Consumer Lag
#### Overview of producer and consumer monitoring
### Advanced Storage
#### Tiered Storage
#### Log Compaction
