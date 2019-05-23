# docsify 生成 pdf

## 1. 安装 docsify-pdf-converter

```bash
npm install -g docsify-pdf-converter
```

如果报错无法连接网络，可以尝试使用 tnpm

```bash
tnpm install -g docsify-pdf-converter
```

## 2. 文档根目录下新建配置文件`.docsifytopdfrc.js`

```js
module.exports = {
  contents: ["en/_pdf_dir.md"], // array of "table of contents" files path
  pathToPublic: "component_codec.pdf", // path where pdf will stored
  pdfOptions: "{width: 100}", // reference: https://github.com/GoogleChrome/puppeteer/blob/master/docs/api.md#pagepdfoptions
  removeTemp: true, // remove generated .md and .html or not
  emulateMedia: "screen" // mediaType, emulating by puppeteer for rendering pdf, 'print' by default (reference: https://github.com/GoogleChrome/puppeteer/blob/master/docs/api.md#pageemulatemediamediatype)
};
```

注意此处配置的`en/_pdf_dir.md`为 md 文件目录，类似于`docsify`中的`_sidebar.md`，区别在于：

- 路径需要使用\_pdf_dir.md 所在的相对路径
- 每一个配置都需要指定到 md 文件，而不能是目录

![](https://image-host-wyao.oss-cn-shanghai.aliyuncs.com/img/15583336654197.jpg)

## 3. 文档根目录下新建配置文件`package.json`

```json
{
  "scripts": {
    "convert": "node_modules/.bin/docsify-pdf-converter"
  }
}
```

## 4. 执行命令生成 pdf

```bash
npm run convert
```

## 5. 附录·概览

![](https://image-host-wyao.oss-cn-shanghai.aliyuncs.com/img/15583331817316.jpg)

> 详细使用见：<https://github.com/meff34/docsify-to-pdf-converter>
