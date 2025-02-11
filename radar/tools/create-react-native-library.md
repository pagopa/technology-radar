---
title: "create-react-native-library"
ring: adopt
quadrant: "tools"
tags: [mobile, react-native, swift, kotlin, java]
---

[create-react-native-library](https://callstack.github.io/react-native-builder-bob/)
is a CLI for scaffolding React Native libraries for iOS and Android. It
simplifies the process of creating, building, testing, and publishing React
Native libraries by providing a CLI that leverages `react-native-builder-bob`.

#### Key features:

1. **Simplicity**: Provides a CLI which guides you in the creation of different
   types of React Native libraries.
2. **Toolchain**: Supports TypeScript, ESLint, Prettier, Lefthook and Release It
   out of the box.
3. **Javascript library**: Supports for plain Javascript libraries supported by
   [Expo](https://expo.dev/).
4. **Native view and native module**: Supports the creation of components with
   native view, allowing the leverage of native UI counterparts on specific
   platforms. Supports native module to expose functionality implemented in
   native code, offering a means to access device-specific features (camera,
   keystore, accelerometer, ecc.) or implement performance-critical tasks more
   efficiently through native code integration.
5. **Turbo module and Fabric view**: Experimental support for Turbo module and
   Fabric view which allows for more efficient communication between native and
   JavaScript code by using JSI instead of a bridge which uses serialization via
   JSON like native modules.
6. **Multi-language support**: Supports the creation of libraries written in
   Swift, Kotlin, Java, Objective-C and C++.

## Use cases

- Creation of React Native libraries for iOS and Android which use
  device-specific features like interacting with the keystore on Android or the
  keychain on iOS.
- Creation of React Native libraries for iOS and Android which implement
  performance-critical tasks more efficiently through native code integration,
  like cryptography operations.
- Creation of React Native libraries for iOS and Android which leverage native
  UI counterparts on specific platforms, like a native map view or a native
  video player.

## Reference of usage in our organization

- [IO React Native Crypto](https://github.com/pagopa/io-react-native-crypto)
- [IO React Native Login Utils](https://github.com/pagopa/io-react-native-login-utils)
- [IO React Native JWT](https://github.com/pagopa/io-react-native-jwt)
- [IO App Design System](https://github.com/pagopa/io-app-design-system)
