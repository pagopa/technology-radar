---
title: "AWS SQS"
ring: adopt
quadrant: "platforms-and-aoe-services"
tags: [cloud, aws, queue]
---

[AWS SQS](https://aws.amazon.com/sqs/) is a fully managed message queuing
service that enables decoupling and scaling of distributed systems components.
SQS supports both standard and FIFO (First-In-First-Out) queues, ensuring
reliable and ordered message delivery. As a serverless service, SQS eliminates
the need for managing infrastructure, providing on-demand scalability and high
availability. It integrates seamlessly with other AWS services, making it a
reliable choice for building distributed and resilient applications.

### Use cases

Buffer requests until they can be consumed, whether ordered or not? <br/> if the
answer is yes, use SQS.

- Increase application reliability and scale
- Decouple microservices and process event-driven applications
- Maintain message ordering with deduplication

### Reference of usage in our organization

- [Personal data vault Tokenizer](https://github.com/pagopa/pdv-tokenizer-infra)
- [PDND Interoperabilita'](https://github.com/pagopa/interop-infra)
