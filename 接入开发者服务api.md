#接入开发者服务API

####1.配置服务器

######(1)添加合法域名（必须是https）

![](/assets/wechat-config-server.png)

######(2)开发者工具- 项目- 配置信息 - 刷新

![](/assets/wechat-config-server-project.png)

######(3)开发者工具-清缓存、编译

![](/assets/wechat-config-server-clean.png)

####2.用wx.request()发起ajax请求

注意一下几点：

```
1. wx.request发起的是 HTTPS 请求;
2. url 中不能有端口;
3. method 的 value 必须为大写（例如：GET）
4. content-type 默认为 'application/json'
```
