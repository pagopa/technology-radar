---
title: "Clean Architecture"
ring: trial
quadrant: "methods-and-patterns"
tags: [all]
---

# [Clean architecture](https://betterprogramming.pub/the-clean-architecture-beginners-guide-e4b7058c1165)

Clean Architecture is a software design philosophy that separates the concerns
of the application into distinct layers. It is based on the idea of a "onion"
with the core business logic at the center and the external dependencies at the
edges. The architecture is divided into four concentric layers.

From the center to the edges, the layers are:

1. Entities, which contain **domain models** with their own methods:
   methods belonging to the entities must not depend on any external library or
   framework;
2. Use Cases, which contain the **application-specific business rules**:
   methods belonging to the use cases uses the entities and must not depend on any external library or framework;
3. Interface Adapters, which **implement the interfaces** defined in the use
   cases and interact with external dependencies;
4. Frameworks & Drivers, which contain the **external dependencies** (e.g.,
   database, network, UI).

Here are some advantages of using the Clean Architecture approach:

- **Maintainability**: The architecture makes it easier to maintain and extend
  the codebase by isolating the core business logic from the external
  dependencies, for example when upgrading to a new version of a SDK or
  framework.
- **Testability**: The architecture makes it easier to test the core business
  logic in isolation from the external dependencies: you don't need to mock the
  database or the network to test the business logic.

## Comparison with Hexagonal Architecture

As Clean architecture, Heaxagonal architecture is a software design philosophy
that separates the concerns of the application into distinct layers. 

It is based on the idea of a "hexagon" with the core business logic at the
center and the external dependencies at the edges. The architecture is divided
into three layers:

1. Core, which contains the **business logic** (*use cases*) and domain model
  (*entities*): methods belonging to the core layer must not depend on any
  external library or framework;
1. Ports, which **define the interfaces** that the core layer can use to
  interact with the external world;
1. Adapters, which **implement the interfaces** and interact with external
  dependencies.

While **Clean Architecture** uses concentric circles with dependencies pointing
inward, emphasizing a *hierarchy* between layers, **Hexagonal Architecture**
employs a *symmetrical* model with ports and adapters to handle input/output
uniformly, without strict hierarchies.

In both architectures, the core business logic is isolated from the external
dependencies. Each layer has a specific responsibility and interacts with the
other layers through well-defined interfaces.

## Use cases

Clean Architecture is well-suited for **microservices** because it allows
you to isolate the business logic of each service from the external
dependencies.

## Example of application in a Typescript monorepo

Below is an example of how to structure a TypeScript workspace to achieve
separation of concerns:

```
/src
  /domain
    - [Entities and Interfaces (ports)]
  /use-cases
    - [Use Cases]
  /adapters
    - [HTTP Controllers, Event Handlers,
     Database, External Services (SDK), Logging]
    - config.ts
    - [Configuration, e.g., from environment]
  api.ts
    - [Entry point for the API]
  cli.ts
    - [Entry point for the CLI]
   ...
```

- **Entities** are autonomous and do not import from either adapters or
  use-cases.
- **Domain Interfaces (ports)** contain the interfaces to manipulate entities
  (e.g., repositories, services, etc.) which are agnostic with respect to
  frameworks and external services.
- **Use-cases** utilize entities and ports (e.g., repositories, services, etc.),
  but *never* import adapters.
- **Adapters** implement the interfaces defined in the domain and are only
  imported in the entry point modules and in config.
- **Entry points** act as the "Composition Root" and connect adapters to
  use-cases.

Shared domain parts between workspaces and/or utility functions should go into a
package with the same name of the applicative in the `packages/<monorepo-name>`
directory of the repository.

### Configuration

- The service must fail immediately in case of a configuration error.
- Each adapter exposes a configuration.
- `config.ts` aggregates these configurations and parses the environment (or
  other input, e.g., database) to populate the values for all adapters.

### Reference of usage in our organization

The **Clean Architecture** is currently being trialed in the development of
users SSO for the IO mobile app [FIMS](https://github.com/pagopa/io-fims) and
[Firma con IO](https://github.com/pagopa/io-sign).
