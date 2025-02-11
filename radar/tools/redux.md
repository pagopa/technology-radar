---
title: "Redux"
ring: adopt
quadrant: "languages-and-frameworks"
tags: [web, mobile, react, react-native]
---

[Redux](https://redux.js.org/)

Redux is a predictable state container for JavaScript applications. The
centralization aspect helps manage the data flow within an application, making
it more predictable and consistent. It can seamlessly work with different UI
layers by providing bindings also for React and React Native. Redux works with a
unidirectional data flow, ensuring a clear and predictable pattern for updating
and managing application state. Actions, which represent events or user are
dispatched to the store and reducers process these actions, producing a new
state for the application. The state is immutable and changes are made only by
dispatching actions. Immutability guarantees predictability and facilitates
debugging and testing. It's easy to trace back which action caused a change in
the state, which reducer processed it and which result was yielded.

An ecosystem of extentions is available to add additional functionalities such
as handling asynchronous operations, logging actions, persisting the store etc.
Middlewares in particular can be used to extend Redux functionality by adding
custom logic between dispatching an action and the moment it reaches the
reducer. Thus, allowing side effects like asynchronous API calls.

## Use cases

- Manage application state for web and mobile applications.
- Manage the state of a single component or a group of components in a screen
  based on user interactions.
- Manage the state of a single component or a group of components in a screen
  based on asynchronous operations such as API calls via middlewares like
  [redux-saga](https://redux-saga.js.org/).
- Persist the state of the application between sessions via extentions like
  [redux-persist](https://github.com/rt2zz/redux-persist).

## Reference of usage in our organization

[io-app](https://github.com/pagopa/io-app)
[io-web-profile](https://github.com/pagopa/io-web-profile)
