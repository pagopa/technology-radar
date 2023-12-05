---
title: "Monorepo"
ring: adopt
quadrant: "methods-and-patterns"
tags: [all]
---

In our continuous effort to optimize our software development processes, we
suggest to evaluate the transition from a poly-repo (multiple repositories)
approach to a [monorepo](https://monorepo.tools/) (single repository) structure.
This change is considered to promote better organization, easier maintenance,
and enhanced collaboration across our projects.

The current poly-repo setup presents several challenges:

1. **Repository Obsolescence and Neglect**: Multiple repositories often lead to some
   becoming obsolete or unused, and these are not always marked accordingly. This
   situation creates clutter and confusion in our codebase.
1. **Refactoring Complexity**: In a poly-repo environment, tasks like library
   updates or major refactoring become highly complex. Each repository must be
   individually updated, requiring significant coordination and increasing the
   risk of inconsistencies and integration issues. This complexity can lead to
   delays and higher costs in maintaining and evolving our software.
1. **Inconspicuous Common Package Modifications**: Changes made to common packages are
   less visible in a poly-repo structure. This necessitates the additional steps of
   publishing the packages and then updating each respository with a separate pull
   request (PR), making the process cumbersome.
1. **Risk of Service Misalignment**: Due to the above, there is a high risk of software
   components becoming misaligned, depending on the update status of common packages.
   This can lead to inconsistencies and integration challenges.
1. **Distributed PR Reviews**: Pull requests are spread across multiple repositories,
   making the review process more complex, hard to monitor and time-consuming.
1. **Replication of Settings Across Repositories**: Essential settings like security
   measures, GitHub identity, and pipeline boilerplates need to be replicated in
   each repository. Updates to any of these common elements require refactoring
   across multiple repositories, increasing the workload and potential for errors.
1. **Documentation Challenges**: When common documentation pertains to multiple
   components, it becomes unclear where to place it in a poly-repo setup, leading
   to potential accessibility and update issues.

Adopting a monorepo approach can address these challenges effectively: a
monorepo facilitates streamlined management of common elements, simplifies
refactorings, the PR process, and ensures consistency across the codebase. It
also makes the handling of shared documentation more straightforward and
accessible.

Implementation Considerations: To transition to a monorepo, we need to plan the
migration of existing repositories, ensuring minimal disruption to ongoing
projects. This includes consolidating documentation, unifying pipeline
configurations, and creating a comprehensive strategy for maintaining repository
health and organization.

## List of mono-repositories

https://github.com/pagopa/developer-portal
https://github.com/pagopa/io-services-cms
https://github.com/pagopa/io-sign
https://github.com/pagopa/pn-frontend
