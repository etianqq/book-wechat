#带参数导航

API文档：[https://mp.weixin.qq.com/debug/wxadoc/dev/api/ui-navigate.html#wxnavigatetoobject](https://mp.weixin.qq.com/debug/wxadoc/dev/api/ui-navigate.html#wxnavigatetoobject)

保留当前页面，跳转到应用内的某个页面，使用wx.navigateBack可以返回到原页面。

![](/assets/wechat-navigateTo.png)

#####带参数
**参数与路径之间使用?分隔，参数键与参数值用=相连，不同参数用&分隔；如 ‘path?key=value&key2=value2’**

```
// 跳转页面
wx.navigateTo({
  // 需要跳转的应用内页面的路径 , 路径后可以带参数
  url: '../logs/logs?name=nicole&addr=hanghzou'
})
```

```
// 目标页面
Page({
  // option 为传入参数
  onLoad: function(option){
    console.log(option.name)
    console.log(option.addr)
  }
})
```