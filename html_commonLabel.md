# HTML 常用标签

### a 标签


`<a>`元素 (或HTML锚元素, Anchor Element)通常用来表示一个锚点/链接。但严格来说，`<a>`元素不是一个链接，而是超文本锚点，可以链接到一个新文件、用id属性指向任何元素。如果`<a>`元素没有href属性的话，可以作为原本链接位置的占位符，常用于home链接

　[注意]任何文档流内容都可以被嵌套，只要不是交互内容类别(如按钮、链接等)

#### 属性

【href】

href属性表示地址，共包括以下几种：

1、链接地址
```
<a href="http://www.baidu.com">百度</a>
```
2、下载地址
```
<a href="test.zip">下载测试</a>
```
3、id 值
```
<a href="http://baike.baidu.com/view/2202.htm#2">足球比赛规则</a>
```
```
<a href="#test">目录</a>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div id="test" style="height: 200px;width: 200px; border: 1px solid black;margin-bottom: 300px;">内容</div>
```
4、伪协议
```
javascript: 代码;
mailto: 邮箱;
tel: 手机号;
```
【target】

target属性表示链接打开方式

```
1、_self    当前窗口（默认）
2、_blank    新窗口
3、_parent 父框架集
4、_top 整个窗口
5、_framename 指定框架
```

【download】

download属性用来设置下载文件的名称
```
<a href="test.zip" download="gogo">test</a>
```


### img 标签

`<img>` 表示image图像，从技术上讲，`<img>` 标签并不会在网页中插入图像，而是从网页上链接图像。`<img> `标签创建的是被引用图像的占位空间。`<img>` 的作用是发出 get 请求，展示一张图片

#### 属性


1、src:地址

2、alt:图像替代文本，供探索引擎抓取使用

3、height:图像高度

4、width:图像宽度

记住，永远不要让图片变形，只写高度，宽度会自适应，只写宽度，高度会自适应

#### 事件

onload：在图片加载成功的时候执行的函数

onerror：在图片加载失败的时候执行的函数
```
<img id=xxx />

xxx.onload = function () {alert("加载成功")}

xxx.onerror = function() {
    alert("加载失败")
    xxx.src = '404.png' //加载失败，重新加载一个404的图片  
}
```

#### 最大宽度

如下面设置，图片的宽度不会超过页面的宽度

```
img {
    max-width: 100%
}
```


### table 标签

HTML的 table 元素表示表格数据 — 即通过二维数据表表示的信息

table 元素中允许的内容如下：
```
一个可选的 <caption> 元素
零个或多个的 <colgroup> 元素
一个可选的 <thead> 元素
零个或多个 <tbody>
一个可选的 <tfoot> 元素
```

table 中不包括 tbody 时, 浏览器会自动添加 tbody

tfooter thead tbody 和顺序无关，浏览器会默认按照 thead - tbody -tfooter 将他们排好顺序




下面是一个简单表格的示例
```
<table>
    <thead> <!-- 表头 -->
    <tr> <!-- table里的row -->
        <th> <!-- table里的表头内容 -->
            英语
        </th>
        <th>
            翻译
        </th>
    </tr>
    </thead>
    <tbody>   <!-- 表格内容 -->
    <tr>
        <td> <!-- table里的data 也是一列的内容 -->
            hyper
        </td>
        <td>
            超级
        </td>
    </tr>
    </tbody>
    <tfoot> <!-- 表格脚部内容 -->
    <tr>
        <td>空</td>
        <td>空</td>
    </tr>
    </tfoot>
</table>


#### 感想


1、学习要多练习

2、知识更新换代的速度很快，以前的推荐用法可能过段时间就不推荐了，所以要及时回头看

3、学习 HTML 要选择合适的材料：包括 [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML) 和 [网道](http://wangdoc.com/html/)

