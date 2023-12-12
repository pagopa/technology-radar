---
title: "Atlas"
ring: trial
quadrant: "tools"
tags: [database, migration, devops]
---

[Atlas](https://atlasgo.io) is a language-independent tool for managing and migrating database schemas using modern DevOps principles

It offers two workflows:

* **Declarative**: Similar to Terraform, Atlas compares the current state of the database to the desired state, as defined in an HCL, SQL, or ORM schema. Based on this comparison, it generates and executes a migration plan to transition the database to its desired state.

* **Versioned**: Unlike other tools, Atlas automatically plans schema migrations for you. Users can describe their desired database schema in HCL, SQL, or their chosen ORM, and by utilizing Atlas, they can plan, lint, and apply the necessary migrations to the database.
