---
title: "Flipper"
ring: adopt
quadrant: "tools"
tags: [mobile, react-native, ios, android, debug]
---

[Flipper](https://fbflipper.com/) is a debugging tool for mobile apps that
provides a GUI to inspect the app's state. It supports React Native, native iOS,
and native Android apps and has been integrated into React Native as the default
debugger from version 0.62 to version 0.73.

Out of the box, Flipper provides a network inspector for monitoring application
network requests, a log viewer for inspecting and filtering logs, and a crash
reporter for investigating crashes and exceptions. Additionally, it provides a
layout inspector and various utilities for managing virtual devices, recording
videos, and taking screenshots. Flipper is built around a plugin system which
allows developers to create custom plugins for a variety of use cases. A list of
available plugins can be downloaded directly from Flipper.

## Use cases

- Inspect the network requests made by the app and their responses.
- Inspect the view hierarchy of the app.
- Inspect the state of the Redux store and the dispatched actions.
- Inspect and filter logs produced by the app.
- Inspect the asynchronous storage of the app to debug persisted state.

## Reference of usage in our organization

- [io-app](https://github.com/pagopa/io-app)
