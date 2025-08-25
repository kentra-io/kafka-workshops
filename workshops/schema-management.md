# Schema Management in Kafka for Java Application Developers
### 1 day workshop

## About This Workshop

Schema Management is a critical aspect of building complex Data Streaming ecosystems. It provides efficiency, predictability and enables 
sophisticated integrations built on top of your data streams. But it's often overlooked - because without practice and knowledge it's often perceived as significant development overhead. 

This workshop is designed for developers that are using Kafka already but either haven't used Schemas, or have some experience and want to deepen their understanding of the topic. It covers the basics as well as advanced topics that will help you set up an efficient Schema Management setup that results in smooth development flow and explicit, predictable structure of messages in your Kafka Topics. 

This is a hands-on workshop, and comes with two coding exercises that will be very helpful if you want to build or improve the way you manage schemas in your projects. Due to the intensity of this workshop, we won't be building things from scratch - you'll be learning how the workflow looks like in a mature production setup. You'll get a feel for how efficient it can be and get production-ready code that you can use as a reference.

### What you'll learn
- How Confluent Schema Registry works
- How Spring Boot Kafka Clients serialize and deserialize messages and use Schema Registry
- Basics of the Avro serialization format
- How to map Schemas to Topics and when to use which strategy
- How to use Schemas in Kafka Connect and Kafka REST Proxy
- How to evolve your schemas without breaking compatibility and how to choose Compatibility Type for your topics
- How to build a dedicated Schema repository and how to integrate it with your clients and your Schema Registry environments 

### What's not in scope
- Deploying and operating Schema Registry
- Securing Schema Registry

### Technologies used in the workshop
#### Confluent Schema Registry
There are many open source schema registries available for Kafka - but Confluent Schema Registry is the most popular one, and a reference point - most alternative solutions implement Confluent Schema Registry's API.
#### Spring Boot
Spring Boot is the most popular Java framework with great integration with both Kafka and Schema Registry.
#### Avro
Avro is the most popular serialization format, so that's what we'll be using on the open workshop. Dedicated workshops can be customized to use Protobuf or JsonSchema in the exercises.

## Structure of the workshop

### Why use Schemas in Kafka?
#### Message Retention in Data Streaming
#### Schema Evolution
#### Predictability & Downstream systems
#### Space efficiency

### Serialization formats
#### Avro
#### Protobuf
#### JSON & JSON Schema

### How Confluent Schema Registry works
#### Schemas, Subjects and Topics
##### SubjectNameStrategy
##### Schema Evolution & Compatibility Type
#### Deploying Schemas
##### Using REST API
##### Using Terraform
##### How are Schemas stored in Kafka?
#### Confluent Wire Format

### Using schemas in Spring Boot client applications
#### Configuring producers & consumers
#### Avro basics
##### Avro-reflect
#### Serialization / Deserialization issues
##### Poison Pill & ExceptionHandlingDeserializer

### Coding exercise - Avro
#### Generating Java classes from Avro schemas
#### Generating Avro from Java classes
#### Serializing & Deserializing a Java POJO with Avro

### Using schemas with Kafka tooling
#### Kafka Connect
#### Kafka REST Proxy

### Coding exercise - Dedicated Schema Repository
#### Workflow design
#### Integration with Maven repository
#### Integration with Schema Registry
