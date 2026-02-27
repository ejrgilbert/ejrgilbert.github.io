---
title: "Component Interposition"
excerpt: "Demonstration on bundling server+middleware into a single Wasm component."
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

The [component-interposition] repository demonstrates how to inject middleware into Wasm components using the
[`splicer`] tool. These components can be single services OR [service-chained] compositions. Through defining
some simple [YAML configurations], `splicer` does the hard work of planning the middleware interposition given
an arbitrary composition.

The services and middlewares used in this repository to demonstrate the interposition capability do the most basic
operation of printing to the console to not distract from the capability shown here. Next, we plan to use this technique,
to port production-ready middleware such as OpenTelemetry observability, encryption, and security policy enforcement
across service compositions.

[component-interposition]: https://github.com/ejrgilbert/component-interposition
[`splicer`]: https://ejrgilbert.github.io/projects/splicer/
[service-chained]: https://www.fermyon.com/blog/protect-rest-apis-with-service-chaining
[YAML configurations]: https://github.com/ejrgilbert/component-interposition/tree/main/splicer-rules
---

# Demos

<div class="link-list">

    <i class="far fa-file-alt"></i> <a href="https://www.youtube.com/live/F0adyCd2RMs?t=1039s" target="_blank">wasmCloud Community Meeting</a><br>
    <p style="margin-left: 33px; font-size: 19px; font-style: italic;">"We can do fascinating things with [component interposition]: observability, security policies, really whatever you want to! You have full control over the incoming and outgoing requests."</p>

</div>

