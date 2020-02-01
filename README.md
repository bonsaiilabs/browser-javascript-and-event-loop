# Browser JavaScript and Event Loop
## Master how browser runs JavaScript under the hood using asynchronous execution and event loop
This is the code repository for the course [Browser JavaScript and Event Loop](https://bonsaiilabs.com/event-loop-javascript)

**Note**  

---  
Every browser may differ in their implementation which *may* result in different behaviours when code execution happens.  

This course takes [Google Chrome](https://www.google.com/chrome/) as browser of choice. It is a great idea to have it installed on your machine, if haven't already. This will help you replicate the results as explained in the course.

## How to run the code
- Clone the repository  
```sh
git clone git@github.com:bonsaiilabs/browser-javascript-and-event-loop.git   
```

- Get inside the project root  
```sh
cd browser-javascript-event-loop
```

- Open the folder in your favorite editor
- Open Google Chrome. Open the [Developer Tools](https://developers.google.com/web/tools/chrome-devtools/open).  
- Open the [**Console** panel](https://developers.google.com/web/tools/chrome-devtools/open#console)  
- Copy the code from an existing file. Paste in the Chrome Developer Tools Console. Press **Enter** `↩`.  
- You should see the output in the console now.  

## References  
- [Apple's JavaScript Engine is called JavaScript Core](https://en.wikipedia.org/wiki/WebKit#JavaScriptCore)  
- [Microsoft JScript Engine is known as Chakra](https://en.wikipedia.org/wiki/Chakra_(JScript_engine))  
- [List of JavaScript Engines](https://en.wikipedia.org/wiki/List_of_ECMAScript_engines)  
- [ECMAScript is a scripting-language specification to standardize JavaScript](https://en.wikipedia.org/wiki/ECMAScript)  
- `setTimeout` is a method on [Window](https://developer.mozilla.org/en-US/docs/Web/API/Window) which is an interface available on [DOM API](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)  
- Relationship between [Chrome and Chromium](https://chromium.googlesource.com/chromium/src/+/master/docs/chromium_browser_vs_google_chrome.md)  


### About Chrome JavaScript Engine - [V8](https://v8.dev/docs)  
1. [V8](https://source.chromium.org/chromium/chromium/src/+/master:v8/) is Google's open source JavaScript engine.
2. [V8](https://source.chromium.org/chromium/chromium/src/+/master:v8/) implements ECMAScript as specified in ECMA-262.

### Web APIs
1. Use [caniuse.com](https://caniuse.com/) to search for feature support in browsers  
2. List of the Web APIs specifications by [WHATWG](https://spec.whatwg.org/) 
3. List of Web APIs specifications by [W3C](https://www.w3.org/TR/?tag=webapi)  
4. [DOM](https://www.w3.org/TR/?tag=dom) is standardized by W3C  
5. A browser engine is also known as [rendering engine](https://en.wikipedia.org/wiki/Browser_engine)   
### Rendering Engine    
1. [Gecko](https://en.wikipedia.org/wiki/Gecko_(software)) is the rendering engine for Mozilla Firefox browser.   
2. [Webkit](https://webkit.org/) is the rendering engine for Apple Safari browser  
3. [Blink](https://www.chromium.org/blink) is the rendering engine for Google Chrome browser  
4. [EdgeHTML](https://en.wikipedia.org/wiki/EdgeHTML) is the rendering engine for Microsoft Edge Browser. 
5. Example of [`fetch`](https://fetch.spec.whatwg.org/) API implementation by browser engines  
    a. [Gecko (Mozilla)](https://platform-status.mozilla.org/#fetch)  
    b. [Webkit (Safari)](https://webkit.org/status/#specification-fetch)  
    c. [Blink (Chrome)](https://chromestatus.com/feature/6730533392351232)  
    c. [EdgeHTML (Edge)](https://developer.microsoft.com/en-us/microsoft-edge/status/fetchapi/?q=fetch%20api)  

### Timers implementation (`setTimeout`, `setInterval`)  
1. Gecko (Mozilla) - [setTimeout](https://github.com/mozilla/gecko-dev/blob/master/toolkit/modules/Timer.jsm#L81), [setInterval](https://github.com/mozilla/gecko-dev/blob/master/toolkit/modules/Timer.jsm#L95)  
2. Webkit (Safari) - [setTimeout](https://github.com/WebKit/webkit/blob/9029c43e695bf886fffb15eec951f0605e34509b/Source/WebCore/page/DOMWindow.cpp#L1688), [setInterval](https://github.com/WebKit/webkit/blob/9029c43e695bf886fffb15eec951f0605e34509b/Source/WebCore/page/DOMWindow.cpp#L1729)  
3. Blink (Chrome) - [setTimeout](https://github.com/chromium/chromium/blob/888beef69f57f6c8810d22af036e961208cda05f/third_party/blink/renderer/core/frame/window_or_worker_global_scope.cc#L132), [setInterval](https://github.com/chromium/chromium/blob/888beef69f57f6c8810d22af036e961208cda05f/third_party/blink/renderer/core/frame/window_or_worker_global_scope.cc#L195)  

### Processes in Chrome  
1. [Chrome Process Models](https://www.chromium.org/developers/design-documents/process-models)  
2. [Utility Process](https://source.chromium.org/chromium/chromium/src/+/master:content/browser/utility_process_host.h;l=6?q=utility_process&ss=chromium%2Fchromium%2Fsrc&originalUrl=https:%2F%2Fcs.chromium.org%2F). The [Utility Process is a type of Process](https://www.chromium.org/developers/design-documents/extensions/proposed-changes/apis-under-development/processes-api)  
3. [Plugin Process architecture](https://www.chromium.org/developers/design-documents/plugin-architecture). The Pepper Plugin implementation is available [here](https://www.chromium.org/developers/design-documents/pepper-plugin-implementation)  
4. [GPU Process](https://www.chromium.org/developers/design-documents/gpu-accelerated-compositing-in-chrome). The documentation of 3D APIs in Mac is available [here](https://support.apple.com/en-us/HT202823)  

### Other References about Chrome Browser  
1. [Inter Process Communication (IPC)](https://www.chromium.org/developers/design-documents/inter-process-communication#IPC_in_the_browser)  
2. [Network Service in Chrome](https://docs.google.com/document/d/1wAHLw9h7gGuqJNCgG1mP1BmLtCGfZ2pys-PdZQ1vg7M/edit)  
3. [Moving Chrome Audio to separate process](https://docs.google.com/document/d/1fVHVJjd5zTqc6O7b0lprILyuFPC9qVQUudzjEgOq1HY/edit#heading=h.x730v6kpv1zk)  
4. [Mojofication of Chrome Audio IPC](https://docs.google.com/document/d/1awQoajq_DLmz2AIU9iweC0zEYlVuHCvEIRQepeYyxh8/edit#)  
5. [Sandbox architecture](https://chromium.googlesource.com/chromium/src/+/master/docs/design/sandbox.md).     
6. [Sandboxed Chrome Processes](https://developers.google.com/web/updates/2019/08/chromium-chronicle-5)  
7. [Sandbox FAQs](https://chromium.googlesource.com/chromium/src/+/master/docs/design/sandbox_faq.md)  
8. [How Blink works](https://docs.google.com/document/d/1aitSOucL0VHZa9Z2vbRJSyAIsAz24kX8LFByQ5xQnUg/edit#heading=h.v5plba74lfde)  
9. [What Blink does](https://docs.google.com/document/d/1aitSOucL0VHZa9Z2vbRJSyAIsAz24kX8LFByQ5xQnUg/edit#heading=h.mndgzxvp6evc)  
10. [Chrome Multi-process architecture](https://www.chromium.org/developers/design-documents/multi-process-architecture)  

### Reference to [Chromium Codebase](https://source.chromium.org/)  
1. [Blink directory structure](https://source.chromium.org/chromium/chromium/src/+/master:third_party/blink/renderer/README.md)  
2. [Off-main thread runs the task in worker pool](https://chromium.googlesource.com/chromium/src/+/master/third_party/blink/renderer/platform/scheduler/TaskSchedulingInBlink.md#off_main-thread-scheduling)  
3. [Task Scheduling in Blink](https://chromium.googlesource.com/chromium/src/+/master/third_party/blink/renderer/platform/scheduler/TaskSchedulingInBlink.md#overview)  
4. [Blink Scheduler](https://docs.google.com/document/d/11N2WTV3M0IkZ-kQlKWlBcwkOkKTCuLXGVNylK5E2zvc/edit#)  
5. [Task Queues and Ordering in Blink Scheduler](https://docs.google.com/document/d/1Apz-SD-pOagGeyWxIpgOi0ARNkrCrELhPdm18eeu9tw/edit#heading=h.ca7ypstpqk29)  
6. [List of Task Sources known to Blink](https://source.chromium.org/chromium/chromium/src/+/master:third_party/blink/public/platform/task_type.h;l=6?q=task_type&ss=chromium%2Fchromium%2Fsrc&originalUrl=https:%2F%2Fcs.chromium.org%2F)  
7. [Event Loop](https://source.chromium.org/chromium/chromium/src/+/master:third_party/blink/renderer/platform/scheduler/public/event_loop.h;l=6?q=event_loop&ss=chromium%2Fchromium%2Fsrc&originalUrl=https:%2F%2Fcs.chromium.org%2F) in Chromium manages the microtask queue  
8. [Promise reactions are queued as microtask](https://source.chromium.org/chromium/chromium/src/+/master:v8/src/objects/promise.h;l=84)  
9. [message_loop](https://source.chromium.org/chromium/chromium/src/+/master:base/message_loop/message_loop.h) is the Chromium's abstraction for event loops. See *Part 3: Message loops* in [codelabs](https://www.chromium.org/developers/cpp-in-chromium-101-codelab). The event loop implementation is different for every platform. View the [message_loop](https://source.chromium.org/chromium/chromium/src/+/master:base/message_loop/message_loop.h) directory structure to locate header files for `android`, `ios`, `mac`, and many more. 
10. [Every thread has its own event loop](https://source.chromium.org/chromium/chromium/src/+/master:base/message_loop/message_loop.h;l=36-37)  
11. Blink uses [V8 APIs](https://github.com/chromium/chromium/tree/c09af941e6675068427d56bf7c540659e2578a17/third_party/blink/renderer#bindings)   
12. The source for [main thread scheduler](https://source.chromium.org/chromium/chromium/src/+/master:third_party/blink/renderer/platform/scheduler/main_thread/main_thread_scheduler_impl.cc)  

### References from ECMASCript specification
1. [ExecutionContext Stack](https://tc39.es/ecma262/#execution-context-stack)  
2. [Jobs and Job Queues](https://tc39.es/ecma262/#sec-jobs-and-job-queues)
3. [Promise Objects](https://tc39.es/ecma262/#sec-promise-objects)  
4. Section on [Promise.then](https://tc39.es/ecma262/#sec-performpromisethen)  

### References from HTML specification  
1. `setTimeout` callback is queued as a Task. See *step 18* of [timer initialization steps](https://html.spec.whatwg.org/multipage/timers-and-user-prompts.html#timer-initialisation-steps)  
2. [Event Loop Processing Model](https://html.spec.whatwg.org/multipage/webappapis.html#event-loop-processing-model)  
3. User agents must use [event loops](https://html.spec.whatwg.org/multipage/webappapis.html#event-loop) to coordinate events, user interaction, scripts, rendering, and networking.  
4. User interaction (e.g. click events) are queued as Tasks as defined in [user interaction task source](https://html.spec.whatwg.org/#user-interaction-task-source)  
5. [Rendering Opportunity](https://html.spec.whatwg.org/multipage/webappapis.html#rendering-opportunity) under the event loop processing model.  
    
### References from `fetch` specification  
1. `fetch` queues a Task. See *step 18* of [Main fetch](https://fetch.spec.whatwg.org/#main-fetch)  