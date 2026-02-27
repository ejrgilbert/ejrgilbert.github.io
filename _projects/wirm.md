---
title: "Wirm"
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

[Wirm](https://github.com/thesuhas/orca) 🐉 is an open-source project Rust library for rewriting WebAssembly bytecode.
It was originally created to replace [Walrus](https://github.com/rustwasm/walrus) as it was unmaintained and difficult to work with when attempting to use it in the [Whamm!](/projects/whamm) project.

This new library, I believe, is easier to reason about injected code since it uses its own IR to basically "hang" newly injected bytecode at specified locations in the original code through the use of "decorators" at the location of injection.
These decorators are associated with some "rule" that says where the code should be injected.
For example, new code to be injected _before_ some opcode would be done so by adding a `Before` decorator to that opcode location in the bytecode IR.
Then, during encoding, when this decorator is seen, it will inject the new instructions _before_ the original opcode.

This library also allows users to work with Wasm components.
Instrumentation of Wasm components is no longer limited to their internal core modules!
Now, users can inject new component-level IR nodes, then the library does the hard work of [encoding the instrumented component](https://docs.rs/wirm/3.0.0/wirm/ir/component/struct.Component.html#method.encode) in topological order (changes any forward references introduced by the instrumentation to backward references).
Further, `wirm` provides [a visitor API](https://docs.rs/wirm/3.0.0/wirm/ir/component/visitor/index.html) for walking components either in:
1. [structural order](https://docs.rs/wirm/3.0.0/wirm/ir/component/visitor/fn.walk_structural.html) (follows the order of the parsed binary)
2. or [topological order](https://docs.rs/wirm/3.0.0/wirm/ir/component/visitor/fn.walk_topological.html) (visits dependencies first).

This API also provides built-in support for [reference resolution](https://docs.rs/wirm/3.0.0/wirm/ir/component/visitor/struct.VisitCtx.html#method.resolve).

Contributions are welcome/encouraged/extremely helpful/all the good things.
