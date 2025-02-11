---
title: "Optic"
ring: trial
quadrant: "tools"
tags: [api, build, testing, integration]
---

[Optic](https://github.com/opticdev/optic)
Optic is an open-source tool that enhances API development by providing OpenAPI linting, diffing, and testing capabilities. It helps teams prevent breaking changes, publish accurate documentation, and improve API design by integrating seamlessly into continuous integration workflows

## Use cases

- **Preventing Breaking Changes**: Optic detects breaking changes between different versions of an OpenAPI specification, ensuring API stability and backward compatibility. 

- **Automated API Documentation**: By capturing traffic from tests, Optic verifies the accuracy of OpenAPI specifications, facilitating the maintenance of up-to-date and precise API documentation. 

- **API Design Improvement**: Optic's linting features assist in enhancing API design by enforcing consistent naming conventions and requiring comprehensive documentation within the OpenAPI spec. It utilizes Spectral, a flexible JSON/YAML linter, to apply custom rulesets for API design validation. 

## Reference of usage in our organization

- Selfcare Github Action (https://github.com/pagopa/selfcare-commons/tree/main/github-actions-template/swagger-detect-conflict-quarkus): Optic analyzes the proposed changes and compares the new specifications with existing ones to identify any breaking changes. In addition, GH fails if new changes doesn’t meet high-quality standards defined by Optic rules.
- Selfcare API Automation (https://github.com/pagopa/selfcare-external-api-backend): Optic enhances the description of exposed REST APIs by automatically generating up-to-date documentation that reflects the latest changes.
