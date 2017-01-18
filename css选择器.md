# css选择器



| 选择器 | 样例 | 样例描述 |
| :--- | :--- | :--- |
| .class | .intro | 选择所有拥有 class="intro" 的组件 |
| #id | #firstname | 选择拥有 id="firstname" 的组件 |
| element | view | 选择所有 view 组件 |
| element element | view checkbox | 选择所有文档的 view 组件和所有的 checkbox 组件 |
| ::after | view::after | 在 view 组件后边插入内容 |
| ::before | view::before | 在 view 组件前边插入内容 |

```
定义在 app.wxss 中的样式为全局样式，作用于每一个页面。
在 page 的 wxss 文件中定义的样式为局部样式，只作用在对应的页面，并会覆盖 app.wxss 中相同的选择器。
```





