---
title: "Spring Boot"
ring: adopt
quadrant: "languages-and-frameworks"
tags: [java, backend]
---

Spring Boot is an open source Java-based framework used to create a microservices. It is developed by Pivotal Team and is used to build stand-alone and production ready spring applications.

The Spring Cloud ecosystem also gives you a lot of extension points for developing, deploying and running cloud applications.

It's based on the rock-solid Spring framework and provides excellent documentation.

[Spring Boot](https://spring.io/projects/spring-boot)

### Key Features

- **Great community support**: the large community behind spring boot and Pivotal itself allow for ready-to-use integrations for most commonly used technologies.

- **Spring Cloud**: provides tools for developers to quickly build some of the common patterns in distributed systems. Coordination of distributed systems leads to boiler plate patterns, and using Spring Cloud developers can quickly stand up services and applications that implement those patterns.
[Spring Cloud](https://spring.io/projects/spring-cloud)

- **Spring Data**: the mission is to provide a familiar and consistent, Spring-based programming model for data access while still retaining the special traits of the underlying data store. It makes it easy to use data access technologies, relational and non-relational databases, map-reduce frameworks, and cloud-based data services. 
[Spring Data](https://spring.io/projects/spring-data)

### Our use cases
- [File Reporter](https://github.com/pagopa/rtd-ms-file-reporter): microservice responsible to provide an aggregated view of files sent and processed by TAE system. Spring Cloud and Spring Data are respectively used to integrate a Kafka consumer and to provide access to a mongo database. By using spring framework the business logic which use these two integration are unaware of underlying technology and can be easily changed while the interfaces provided by spring keep stable.
- [Decrypter](https://github.com/pagopa/rtd-ms-decrypter): microservice responsible to decrypt incoming TAE's files. The serivce has no REST/HTTP interface and communicates only through Kafka queues. The integration with kafka is provided by Spring Cloud.