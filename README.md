## Usage

```bash
https://unpkg.com/lowcode-demo-preview/build/js/preview.js

# OR
https://cdn.jsdelivr.net/npm/lowcode-demo-preview/build/js/preview.js
```

Edit and save in the [editor](https://lowcode-engine.cn/demo/index.html), and then copy the corresponding content from LocalStorage:

- `${scenarioName}:projectSchema`
- `${scenarioName}:packages`

Store it in the corresponding key in `window.g_config`:

```js
window.g_config = {
    //...
    ___packages: [],
    ___schema: {}
};
```

It can then be used in a custom `preview.html`:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta
      name="viewport"
      content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no"
    />
    <title>阿里低代码引擎 Demo - 预览页</title>
    <link href="https://g.alicdn.com/code/lib/alifd__next/1.23.24/next.min.css" rel="stylesheet" />
    <link href="./css/preview.css" rel="stylesheet" />
  </head>
  <body>
    <div id="ice-container"></div>
    <script>
      window.g_config = {
        locale: 'zh_CN',
        ___packages: [],
        ___schema: {},
      };
    </script>
    <script src="https://g.alicdn.com/code/lib/react/16.13.1/umd/react.production.min.js"></script>
    <script src="https://g.alicdn.com/code/lib/react-dom/16.13.1/umd/react-dom.production.min.js"></script>
    <script src="https://g.alicdn.com/code/lib/prop-types/15.7.2/prop-types.js"></script>
    <script src="https://g.alicdn.com/platform/c/??react15-polyfill/0.0.1/dist/index.js,lodash/4.6.1/lodash.min.js"></script>
    <script src="https://g.alicdn.com/mylib/moment/2.24.0/min/moment.min.js"></script>
    <script src="https://g.alicdn.com/code/lib/alifd__next/1.23.24/next.min.js"></script>
    <script src="https://unpkg.com/lowcode-demo-preview/build/js/preview.js"></script>
  </body>
</html>
```

---

## Low-Code Engine Demo

本 demo 是一个组合内核、setter、插件、物料的示范工程，因为未经长期生产环境打磨，可能还会有一些各个模块间结合的 bug，希望大家理解~

场景列表：

- [index](https://lowcode-engine.cn/demo/index.html)
- [basic-fusion](https://lowcode-engine.cn/demo/basic-fusion.html)（此 fusion 的元数据描述是很老的版本，只为了示意描述结构，请勿用于生产环境）
- [basic-antd](https://lowcode-engine.cn/demo/basic-antd.html)
- [basic-fusion-with-single-component](https://lowcode-engine.cn/demo/basic-fusion-with-single-component.html)
- [custom-initialization](https://lowcode-engine.cn/demo/custom-initialization.html)
- [node-extended-actions](https://lowcode-engine.cn/demo/node-extended-actions.html)
- [next-pro](https://lowcode-engine.cn/demo/next-pro.html)
- [antd-pro-with-formily](https://lowcode-engine.cn/demo/antd-pro-with-formily.html)

更多参考资料：

- [马上玩一下](https://lowcode-engine.cn/demo/index.html)
- [低代码引擎官网](http://lowcode-engine.cn)
- [引擎主包](https://github.com/alibaba/lowcode-engine)
