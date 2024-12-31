---
title: "Orca"
excerpt: "A Rust library for rewriting WebAssembly bytecode."
categories:
- projects
tags:
- instrumentation
- wasm
- WebAssembly
- research
- Rust
---

[Orca](https://github.com/thesuhas/orca) 🐋🌊 is an open-source project Rust library for rewriting WebAssembly bytecode.
It was originally created to replace [Walrus](https://github.com/rustwasm/walrus) as it was unmaintained and difficult to work with when attempting to use it in the [Whamm!](/projects/whamm) project.

This new library, I believe, is easier to reason about injected code since it uses its own IR to basically "hang" newly injected bytecode at specified locations in the original code through the use of "decorators" at the location of injection.
These decorators are associated with some "rule" that says where the code should be injected.
For example, new code to be injected _before_ some opcode would be done so by adding a `Before` decorator to that opcode location in the bytecode IR.
Then, during encoding, when this decorator is seen, it will inject the new instructions _before_ the original opcode.

This library also allows users to perform bytecode rewriting on Wasm components.
The usability could be better here, we are primarily improving each feature as it's being leveraged by Whamm!
As we add instrumentation support for components to Whamm!, the Orca library will be improved/expanded.

Contributions are welcome/encouraged/extremely helpful/all the good things.
