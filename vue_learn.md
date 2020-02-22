# vue 的 runtime

### 术语

完整版(vue.js)： 同时包含编译器和运行时的版本

运行时(vue.runtime.js)：用来创建 Vue 实例、渲染并处理虚拟 DOM 等的代码。基本上就是除去编译器的其它一切

### 渲染

如果需要在客户端编译模板 (比如传入一个字符串给 template 选项，或挂载到一个元素上并以其 DOM 内部的 HTML 作为模板)，就将需要加上编译器，即完整版：

```
// 需要编译器
new Vue({
  template: '<div>{{ hi }}</div>'
})

// 不需要编译器
new Vue({
  render (h) {
    return h('div', this.hi)
  }
})
```

当使用 vue-loader 或 vueify 的时候，*.vue 文件内部的模板会在构建时预编译成 JavaScript。在最终打好的包里实际上是不需要编译器的，所以只用运行时版本即可。

因为运行时版本相比完整版体积要小大约 30%，所以应该尽可能使用这个版本。如果仍然希望使用完整版，则需要在打包工具里配置一个别名：

```
module.exports = {
  // ...
  resolve: {
    alias: {
      'vue$': 'vue/dist/vue.esm.js'
    }
  }
}
```

### codesandbox.io

codeSandbox 是一个浏览器端的沙盒运行环境，支持多种流行的构建模板，例如 create-react-app、 vue-cli、parcel等等。 可以用于快速原型开发、DEMO 展示、Bug 还原等等

只要按照如下步骤：

codesandbox.io –> 不用登录 –> create sandbox –> Vue

一个Vue项目就创建好了
