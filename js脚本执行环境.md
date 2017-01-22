#JS脚本执行环境

微信小程序运行在三端：iOS、Android 和 用于调试的开发者工具。

三端的脚本执行环境聚以及用于渲染非原生组件的环境是各不相同的：

* 在 iOS 上，小程序的 javascript 代码是运行在 ```JavaScriptCore``` 中，是由 WKWebView 来渲染的，环境有 iOS8、iOS9、iOS10
* 在 Android 上，小程序的 javascript 代码是通过 ```X5 JSCore```来解析，是由 X5 基于 Mobile Chrome 37 内核来渲染的
* 在 开发工具上， 小程序的 javascript 代码是运行在 ```nwjs``` 中，是由 Chrome Webview 来渲染的
