# Vue 入门
## 课程大纲
### vue2.5入门教程(vueshili (vue实例) )
>[vue2.5入门教程](https://www.imooc.com/video/16987)

> ?代表存疑问


## 总结
### vue2.5
> 用过的记一下

```vue
指令：

v-on:简写 @
v-bind: 简写:
v-for 循环
v-text 纯文本
v-html 字符串转换为代码
v-model 双向数据绑定
对象,实例  ?

el: 貌似是挂载点  ?
data: 数据
methods: 方法
components: 模板
事件：

@click 点击事件
@delete 自定义事件 ?
应该是创建一个'delete'事件 ?
this.$emit('delete',this.index)
```
>安装vue-cli

```
npm install -g vue-cli
vue init webpack {{项目名}}
```