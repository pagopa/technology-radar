---
title: "Gherkin"
ring: trial
quadrant: "languages-and-frameworks"
tags: [testing]
---

[Gherkin](https://cucumber.io/docs/gherkin/reference/) is a domain-specific language designed for describing software behavior without detailing how that behavior is implemented. It serves as a collaboration tool between technical and non-technical team members.

Gherkin is often used to write acceptance tests. In our case serves as the foundation for test automation. Tools (e.g. [behave](https://behave.readthedocs.io/en/latest/)) interpret Gherkin syntax to execute tests and verify that the software behaves as specified.

Gherkin files can be used as living documentation for software projects. They provide a clear and concise representation of the expected behavior, aiding in requirements understanding and maintenance.

### Key features:

- **Human-Readable Syntax**:
Gherkin uses a plain-text format that is easy to understand by both technical and non-technical stakeholders. This facilitates better collaboration and communication within cross-functional teams.


- **Behavior-Driven Development (BDD)**:
Gherkin is a central component of BDD methodologies, promoting collaboration between developers, testers, and business stakeholders. It allows the creation of executable specifications that ensure the development team delivers the expected functionality.

- **Structured Format**:
Gherkin scenarios are written in a structured format using keywords such as Given, When, Then. This structure provides a clear and consistent way to define the steps of a scenario, making it easy to follow and maintain.

- **Tool Agnostic**:
Gherkin is not tied to any specific programming language or testing tool. This agnosticism allows teams to use Gherkin with various BDD tools and frameworks, fostering flexibility and adaptability.

### Our use cases:

- [Test automation](https://github.com/pagopa/idpay-functional-testing): We use Gherkin as framework to automate funcional tests but its flexibility makes it suitable even for integration tests. At unit level the use of Gherkin can result in a proliferation of ad-hoc step definition, making the whole suite less maintainable. 

- [Requirement Documentation](https://pagopa.github.io/idpay-functional-testing/): Given Gherkin syntax, We parsed feature files and presented their content as documentation on the currently tested scenarios.