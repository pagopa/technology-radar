---
title: "SmallRye Mutiny"
ring: trial
quadrant: "languages-and-frameworks"
tags: [java, backend]
---

["SmallRye Mutiny"](https://smallrye.io/smallrye-mutiny/latest/) is a reactive
Java library designed to handle asynchronous communications and reactive
programming, widely utilized within the Quarkus framework. It offers powerful
tools for managing data streams and events efficiently and scalably, allowing
developers to create robust and highly performant applications. With seamless
integration into Quarkus, it enables developers to build responsive and reliable
Java applications effortlessly, leveraging the full potential of reactive
programming paradigms.

## Use cases

- **Non-blocking I/O Support**: Mutiny serves as an ideal tool for managing the
  asynchronous nature of applications with non-blocking I/O. Developers can
  compose operations declaratively, transform data, handle failures, and ensure
  progress efficiently, enhancing the performance of reactive applications.

- **Reactive Converters Built-In**: it offers built-in converters to interact
  seamlessly with other popular reactive programming libraries. This feature
  enhances interoperability and facilitates the integration of Mutiny into
  existing codebases that might use different reactive frameworks or protocols.

- **Quarkus and Vert.x native Integration**: it is deeply integrated into
  Quarkus, where every reactive API leverages Mutiny's capabilities, ensuring
  optimal performance and scalability within Quarkus applications. Furthermore,
  Mutiny provides bindings for Eclipse Vert.x clients, allowing developers to
  harness the power of Mutiny in Vert.x applications seamlessly.

### Repositories using Mutiny

- Selfcare Onboarding domain (https://github.com/pagopa/selfcare-onboarding)
- Selfcare User domain (https://github.com/pagopa/selfcare-user)
