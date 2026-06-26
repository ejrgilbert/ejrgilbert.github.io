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

:link: [Read the paper on ACM!](https://doi.org/10.1145/3763124)

I may be biased, but [Whamm!](https://github.com/ejrgilbert/whamm) is really cool.
It's a bytecode instrumentation DSL for WebAssembly inspired by the Dtrace [D language](https://docs.oracle.com/en/operating-systems/oracle-linux/dtrace-guide/dtrace-ref-TheDProgrammingLanguage.html#dt_pred_dlang).

Traditionally, bytecode instrumentation frameworks are written using one injection technique, specifically selected based on its chosen domain, limiting the scope of tool use to that domain's breadth.
Expressing instrumentation in Whamm! abstracts above the injection technique and can target multiple domains, based on what makes sense to the user.

You can write instrumentation once, and support wide domain of apps.
Use **engine instrumentation capabilities** as available (currently only the [Wizard VM](https://github.com/titzer/wizard-engine)).
Use **bytecode rewriting**, done with [Wirm](/projects/wirm), to support everything else.

---

# Published Articles

<div class="link-list">

    <i class="far fa-play-circle"></i> <a href="https://www.youtube.com/watch?v=S8HgLNeLD-k&list=PLyqga7AXMtPNV1zr2aTWEegep0FQU6Qvj&index=1" target="_blank">Composable instrumentation in the component model</a><br>
    <p style="margin-left: 33px; font-size: 19px; font-style: italic;">"Whamm asks a surprisingly simple question: What if building a debugger, profiler, tracer, coverage tool, and security monitor wasn't a giant engineering project every single time?"</p>

    <i class="far fa-file-alt"></i> <a href="https://thenewstack.io/meet-whamm-the-webassembly-instrumentation-framework/" target="_blank">Meet Whamm: The WebAssembly Instrumentation Framework</a><br>
    <p style="margin-left: 33px; font-size: 19px; font-style: italic;">"[Whamm] does not replace, ameliorate or improve existing tools and processes but can actually do things that have not properly existed before."</p>

    <i class="fas fa-code"></i> <a href="https://thenewstack.io/open-source-whamm-use-webassembly-to-monitor-and-fix-running-apps/" target="_blank">Use WebAssembly To Monitor and Fix Running Apps</a><br>
    <p style="margin-left: 33px; font-size: 19px; font-style: italic;">"[Whamm is] definitely another win for the WebAssembly community, as well as for observability, debugging and the ability to update applications dynamically with Wasm."</p>

</div>
