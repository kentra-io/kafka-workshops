# Kafka Schema Management with GitOps

#### Duration: 1 day

#### Format: Hands-on training workshop

#### Target audience: Kafka Developers, Platform Engineers, Architects

---

## About This Workshop

Schema Management is a critical aspect of building complex Data Streaming ecosystems. It provides efficiency,
predictability and enables sophisticated integrations built on top of your data streams.

But Schema Management is often overlooked. Sometimes after initial approach teams that don't develop an efficient setup
or introduce Schemas too early in a project reject Schemas because of the perception that they add overhead.

This can be the case if you don't have a good, deep understanding of this topic. However, with a proper setup the
development workflow is smooth and very intuitive to grasp.

I've introduced it in a few organizations and seen how quickly new engineers just grasp it and start using it without
friction.

### Target audience

This workshop is designed for Engineers and Architects that are using Kafka already but either haven't used Schemas, or
have some experience and want to get a full understanding of this topic.

Organizations that would benefit the most are either using Kafka without Schemas, or have started to introduce Schemas,
but didn't build a process they're happy with and want to understand the capabilities and best practices.

---

### Scope

This is a hands-on workshop. We go in depth into how Schema Management works in Kafka, what architectural choices you'll
need to understand and make, and what's available in the broader tech environment - not just the tech stack we'll be
working with.

This training touches many technologies, but the only one we'll explore a bit deeper is the Schema Registry API. The
purpose
of this workshop is to understand how different technologies integrate together, what concepts you need to understand
when working with Schemas and what are the best practices in this problem space.

Tech stack is designed to use the most mainstream technologies, however dedicated workshops can be tailored to the tech
stack of the customer. The critical parts are supplemented with hands-on exercises, that can serve as a
foundation when
building Schema Management setup in your organization.

#### What you'll learn

- Basics of message serialization with Avro
- How Confluent Schema Registry works
- How Spring Boot Kafka Clients serialize and deserialize messages and use Schema Registry
- Schema Evolution:
    - How to evolve your schemas without breaking compatibility
    - How to choose Compatibility Type for your topics
    - When does it make sense to break compatibility
- How to map Schemas to Topics, how to assign multiple Schemas to a Topic and when to do that
- How to build a Dedicated Schema Repository with GitOps approach
- How to integrate it with kafka consumers / producers and your Schema Registry environments

#### What's not in scope

- Deploying and operating Schema Registry
- Securing Schema Registry

#### Coding exercises

Due to the intensity of this workshop, we won't be building things from scratch - you'll be working with simple ready-made
apps and tests and slightly changing them in order to understand how different elements integrate together.

Exercises cover:

- Serializing and Deserializing your Kafka Messages using Schemas
- Integrating the application with your Kafka environment
- Schema evolution
- Schema Management in Kafka with GitOps

You'll get a feel of how an efficient Schema Management workflow looks like and get code examples that can serve as
reference when building Schema Management setup in your organization.

---

### Technologies used in the workshop

#### Confluent Schema Registry

There are many open source schema registries available for Kafka - but Confluent Schema Registry is the most popular
one, and reference point - most alternative solutions implement Confluent Schema Registry's API.

#### Spring Boot

Spring Boot is the most popular Java framework with great integration with both Kafka and Schema Registry.

#### Avro

Avro is the most popular serialization format, so that's what we'll be using in the open workshop. Dedicated workshops
can be customized to use Protobuf or JsonSchema in the exercises.

---

# Structure of the workshop

## Module 1: Introduction to Schema Management

### Why use Schemas in Kafka?

- Message Retention in Data Streaming
- Schema Evolution
- Predictability & Downstream systems
- Space efficiency

### How Confluent Schema Registry works

- Schemas, Subjects and Topics
- Schema Evolution & Compatibility Type
- SubjectNameStrategy and Union Schema pattern
- Confluent Wire Format
- How are Schemas stored in Kafka?

### Deploying Schemas

- Using REST API
- Using Terraform / GitOps

--- 

## Module 2: Serialization

### Serialization formats

- JSON & JSON Schema
- Avro
- Protobuf

### Coding exercise - Avro generation & serialization

In this exercise you'll:

- Generate a Java class from an Avro schema in Gradle
- Create an object, serialize it to Avro format and deserialize it
- Deserialize an object using a different Schema than the one it was serialized with (simulating Schema Evolution)

---

## Module 3: Using Schemas in a Kafka Client

### Using Schemas in Spring Boot client applications

- Configuring producers & consumers
- Poison Pill & ExceptionHandlingDeserializer
- Integration testing with Testcontainers

### Coding exercise - using Schemas

In this exercise you'll run Kafka, Schema Registry and a UI (Kafbat-UI) in Docker.

Then you'll run a Spring Boot application that integrates with this environment. You'll practice evolving Schemas you've
deployed and see what happens when you consume messages serialized using older Schemas.

---

## Module 4: Schema Management with GitOps - integrated workflow

### Designing a GitOps Schema Management setup

- Dedicated Schema Repository
- Integration with Schema Registry environments
- Integration with client applications
- Possible architectural choices
    - GitOps support in commercial & OSS tooling
    - Centralized vs Decentralized
    - YAML vs AsyncAPI
- Workflow design

### Coding exercises - Dedicated Schema Repository & GitOps

In these exercises you'll use Jikkou to provision your Docker environment with Topics and Schemas in a declarative
way using YAML.

Then you'll learn how to work with a setup where your Dedicated Schema Repository is separate from repositories of your
Kafka producers and consumers - how to evolve your Schemas and upgrade Schema versions in client applications by just
bumping the library version. 