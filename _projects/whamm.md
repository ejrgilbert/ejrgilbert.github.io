---
title: "Whamm!"
excerpt: "A bytecode instrumentation DSL for WebAssembly."
categories:
- projects
tags:
- instrumentation
- wasm
- WebAssembly
- research
- DSL
---

<figure style="width: 100px" class="align-right mfp-align-top">
  <img src="/assets/images/whamm!_logo.png" alt="">
</figure>
I may be biased, but [Whamm!](https://github.com/ejrgilbert/whamm) is really cool.
It's a bytecode instrumentation DSL for WebAssembly inspired by the Dtrace [D language](https://docs.oracle.com/en/operating-systems/oracle-linux/dtrace-guide/dtrace-ref-TheDProgrammingLanguage.html#dt_pred_dlang).

Traditionally, bytecode instrumentation frameworks are written using one injection technique, specifically selected based on its chosen domain, limiting the scope of tool use to that domain's breadth.
Expressing instrumentation in Whamm! abstracts above the injection technique and can target multiple domains, based on what makes sense to the user.

You can write instrumentation once, and support wide domain of apps.
Use **engine instrumentation capabilities** as available (currently only the [Wizard VM](https://github.com/titzer/wizard-engine)).
Use **bytecode rewriting**, done with [Orca](/projects/orca), to support everything else.
