# PagoPA Technology Radar - Content

This is the location of [PagoPA technology radar](https://pagopa.github.io/engineering/technology-radar/index.html),
based on [AOE technology radar](https://github.com/AOEpeople/aoe_technology_radar).

## Content Guidelines

Place new Markdown content inside the `radar` directory (one Markdown file for each technology / pattern).

Start every `.md` file with a frontmatter header ie.

```md
---
title: "Turborepo"
ring: trial
quadrant: "tools"
tags: [build, frontend]
---
```

Tags: architecture, security, devops, frontend, agile,
coding, quality assurance, ci/cd, ux/ui, documentation

Rings: adopt, trial, assess, hold

Quadrants: tools, methods-and-patterns, languages-and-frameworks, platforms-and-aoe-services

## Development

### Host the application under a sub path

To host the application under a sub path, set the environment variable `PUBLIC_URL`,
The default is `/`.

> For local development use `/build` and use this for the following steps.

### Build the radar

```
npm i
PUBLIC_URL=/build npm run start
```

Then open here: http://localhost:8080/build

### Build the radar with static files

```
npm i
PUBLIC_URL=/build npm run start:static
```

Then open here: http://localhost:8080/build

### Regenerate the json file based on your changes on md files

```
npm run generateJson
```

You can do this while the server is running.
You can find the newly created rd.json in "/build/rd.json".
