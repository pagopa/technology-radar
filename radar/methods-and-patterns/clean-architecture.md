---
title: "Hexagonal architecture"
ring: trial
quadrant: "methods-and-patterns"
tags: [all]
---

# [Hexagonal architecture](https://en.wikipedia.org/wiki/Hexagonal_architecture_(software))

Hexagonal architecture is a software design pattern that promotes a clear
separation of concerns and a strong dependency rule. It is based on the idea of
a "hexagon" with the core business logic at the center and the external
dependencies at the edges. The architecture is divided into three layers:

1. Core, which contains the **business logic** (*use cases*) and domain model
  (*entities*): methods belonging to the core layer must not depend on any
  external library or framework;
2. Ports, which **define the interfaces** that the core layer can use to
  interact with the external world;
3. Adapters, which **implement the interfaces** and interact with external
  dependencies.

Here are some advantages of using the "hexagonal architecture" approach:

- **Maintainability**: The architecture makes it easier to maintain and extend
  the codebase by isolating the core business logic from the external
  dependencies, for example when upgrading to a new version of a SDK or
  framework.
- **Testability**: The architecture makes it easier to test the core business
  logic in isolation from the external dependencies: you don't need to mock the
  database or the network to test the business logic.

## Comparison with Clean Architecture

As Hexagonal architecture, Clean architecture is a software design philosophy
that separates the concerns of the application into distinct layers. The
architecture is divided into four layers:

1. Entities
2. Use Cases
3. Interface Adapters
4. Frameworks & Drivers

Each layer has a specific responsibility and interacts with the other layers
through well-defined interfaces.

While **Clean Architecture** uses concentric circles with dependencies pointing
inward, emphasizing a *hierarchy* between layers, **Hexagonal Architecture**
employs a *symmetrical* model with ports and adapters to handle input/output
uniformly, without strict hierarchies.

## Example of application in a Typescript monorepo

Here is an example of how to structure a Typescript workspace to implement
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
  but do not import adapters.
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

The **Hexagonal Architecture** is currently being trialed in the development of
users SSO for the IO mobile app [FIMS](https://github.com/pagopa/io-fims)
and [Firma con IO](https://github.com/pagopa/io-sign).