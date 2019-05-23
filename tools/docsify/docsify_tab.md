# docsify 使用 tab 插件

`index.html`加载插件

```html
<script src="https://cdn.jsdelivr.net/npm/docsify-tabs@1"></script>
```

配置参数

```js
window.$docsify = {
  // ...
  tabs: {
    persist: true, // default
    sync: true, // default
    theme: "classic", // default
    tabComments: true, // default
    tabHeadings: true // default
  }
};
```

用法：

```markdown
<!-- tabs:start -->

#### ** English **

Hello!

#### ** French **

Bonjour!

#### ** Italian **

Ciao!

<!-- tabs:end -->
```

样例：
![](https://image-host-wyao.oss-cn-shanghai.aliyuncs.com/img/20190523223452.png)
