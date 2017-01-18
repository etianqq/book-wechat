#setData

```setData``` 函数用于将数据从逻辑层发送到视图层，同时改变对应的 this.data 的值。

```
注意：

1. 直接修改 this.data 无效，无法改变页面的状态，还会造成数据不一致。
2. 单次设置的数据不能超过1024kB，请尽量避免一次设置过多的数据。
```

可以有如下设置方法：
```
Page({
  data: {
    text: 'init data',
    array: [{text: 'init data'}],
    object: {
      text: 'init data'
    }
  },
  changeText: function() {
    // this.data.text = 'changed data'  // bad, it can not work
    this.setData({
      text: 'changed data'
    })
  },
  changeItemInArray: function() {
    // you can use this way to modify a danamic data path
    this.setData({
      'array[0].text':'changed data'
    })
  },
  changeItemInObject: function(){
    this.setData({
      'object.text': 'changed data'
    });
  },
  addNewField: function() {
    this.setData({
      'newField.text': 'new data'
    })
  }
})
```

要注意，如果为数组里的某个对象设置值：
![](/assets/wechat-setdata.png)


