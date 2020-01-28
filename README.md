# Browser JavaScript and Event Loop
## Master how browser runs JavaScript under the hood using asynchronous execution and event loop
This is the code repository for the course [Browser JavaScript and Event Loop](https://bonsaiilabs.com/event-loop-javascript)

**Note**  

---  
Every browser has different implementation which *may* result in different behaviours when code execution happens.  

This course takes [Google Chrome](https://www.google.com/chrome/) as browser of choice. It is a great idea to have it installed on your machine, if haven't already.

This will help you replicate the results as explained in the course.

## How to run the code
- Clone the repository  

- [ ] TODO: Add Github Link  

```sh
git clone ...
```

- Get inside the project root  
```sh
cd browser-javascript-event-loop
```

- Open the folder in your favorite editor
- Open Google Chrome. Open the Developer Tools by pressing `⌥⌘I`. Select the `Console` Tab where you can write JavaScript Code.   
- Copy the code from an existing file. Paste in the Chrome Developer Tools Console. Press Enter `↩`.  
- You should see the output in the console now.  

## References  
- [Apple's JavaScript Engine is called JavaScript Core](https://en.wikipedia.org/wiki/WebKit#JavaScriptCore)  
- [Microsoft JScript Engine is known as Chakra](https://en.wikipedia.org/wiki/Chakra_(JScript_engine))  
- [List of JavaScript Engines](https://en.wikipedia.org/wiki/List_of_ECMAScript_engines)  
- [ECMAScript is a scripting-language specification to standardize JavaScript](https://en.wikipedia.org/wiki/ECMAScript)  
- Web APIs
    1. Use [caniuse.com](https://caniuse.com/) to search for feature support in browsers  
    2. List of the Web APIs specifications by [WHATWG](https://spec.whatwg.org/) 
    3. List of Web APIs specifications by [W3C](https://www.w3.org/TR/?tag=webapi)  
    4. [DOM](https://www.w3.org/TR/?tag=dom) is standardized by W3C  
    5. A browser engine is also known as [rendering engine](https://en.wikipedia.org/wiki/Browser_engine)   
- Rendering Engine    
    1. [Gecko](https://en.wikipedia.org/wiki/Gecko_(software)) is the rendering engine for Mozilla Firefox browser.   
    2. [Webkit](https://webkit.org/) is the rendering engine for Apple Safari browser  
    3. [Blink](https://www.chromium.org/blink) is the rendering engine for Google Chrome browser  
    4. [EdgeHTML](https://en.wikipedia.org/wiki/EdgeHTML) is the rendering engine for Microsoft Edge Browser. 
    5. Example of [`fetch`](https://fetch.spec.whatwg.org/) API implementation by browser engines  
        a. [Gecko (Mozilla)](https://platform-status.mozilla.org/#fetch)  
        b. [Webkit (Safari)](https://webkit.org/status/#specification-fetch)  
        c. [Blink (Chrome)](https://chromestatus.com/feature/6730533392351232)  
        c. [EdgeHTML (Edge)](https://developer.microsoft.com/en-us/microsoft-edge/status/fetchapi/?q=fetch%20api)  
- Timers implementation (`setTimeout`, `setInterval`) in different browser engines
    1. Gecko (Mozilla) - [`setTimeout`](https://github.com/mozilla/gecko-dev/blob/master/toolkit/modules/Timer.jsm#L81), [`setInterval`](https://github.com/mozilla/gecko-dev/blob/master/toolkit/modules/Timer.jsm#L95)  
    2. Webkit (Safari) - [`setTimeout`](https://github.com/WebKit/webkit/blob/9029c43e695bf886fffb15eec951f0605e34509b/Source/WebCore/page/DOMWindow.cpp#L1688), [`setInterval`](https://github.com/WebKit/webkit/blob/9029c43e695bf886fffb15eec951f0605e34509b/Source/WebCore/page/DOMWindow.cpp#L1729)  
    3. Blink (Chrome) - [`setTimeout`](https://github.com/chromium/chromium/blob/888beef69f57f6c8810d22af036e961208cda05f/third_party/blink/renderer/core/frame/window_or_worker_global_scope.cc#L132), [`setInterval`](https://github.com/chromium/chromium/blob/888beef69f57f6c8810d22af036e961208cda05f/third_party/blink/renderer/core/frame/window_or_worker_global_scope.cc#L195)  


TBD
- Chromium Codebase links



