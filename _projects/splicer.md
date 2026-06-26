---
title: "`splicer`"
excerpt: "A Rust CLI tool to perform interposition on components with chained services."
categories:
- projects
tags:
- instrumentation
- wasm
- WebAssembly
- research
- components
- Rust
---

Component [`splicer`](https://github.com/ejrgilbert/component-interposition) 🔍✂️ is an open-source project Rust CLI tool for splicing middleware(s) into components with chained services.

Given a component composition graph (JSON) and a declarative splice configuration (YAML), it computes how middleware should
be inserted, reordered, or constrained within the component topology without having to manually reason about every edge
and instance. It’s built for engineers working with the WebAssembly Component Model who want deterministic, reviewable
composition plans instead of ad-hoc wiring.

Designed as a CLI-first utility, `splicer` separates *what* you want (expressed in a clean YAML spec) from *how* it must be
integrated (derived from the graph). The result is a clear, automatable workflow for enforcing ordering rules, "before/between"
constraints, and middleware chains in complex component systems.

Contributions are welcome/encouraged/extremely helpful/all the good things.

---

# Published Articles

<div class="link-list">

    <i class="far fa-play-circle"></i> <a href="https://www.youtube.com/watch?v=S8HgLNeLD-k&list=PLyqga7AXMtPNV1zr2aTWEegep0FQU6Qvj&index=1" target="_blank">Composable instrumentation in the component model</a><br>
    <p style="margin-left: 33px; font-size: 19px; font-style: italic;">"...folks have had dreams of having...this type of debuggability for WebAssembly components...you're actually bringing it to life!"</p>

    <i class="far fa-file-alt"></i> <a href="https://bytecodealliance.org/articles/how-wasm-components-enable-pluggable-middleware" target="_blank">How Wasm components enable pluggable tooling through interposition</a><br>
    <p style="margin-left: 33px; font-size: 19px; font-style: italic;">"...the splicer framework makes [component interposition] tractable at any interface edge."</p>


</div>
