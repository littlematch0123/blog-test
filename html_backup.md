hyper 超级

target 目标

reference 引用

frame 框架

error 错误

blank 空白

parent 父母之一

self 自己

load 加载

canvas 画布

a 标签

href = hyper reference 超链接
target
download 下载该网页，但浏览器不支持
rel=noopener

vscode 插件
1、使用 http-server
-c-1 表示不要缓存
http-server -c-1

2、使用 parcel
parcel t.html


伪协议

javascript: 代码
mailto: 邮箱
tel: 手机号
id: href= #xxx
一般地，使用javascript:; 来实现点击a标签什么也不做的效果

target="xxx"，如果没有就创建一个窗口，叫xxx；如果有，就在xxx打开

window.name 就叫做 xxx

iframe 可以设置 name

table 中 tbody是默认需要的，如果不加，浏览器也会加上

image
作用是发出 get 请求，展示一张图片
记住，永远不要让图片变形，只写宽，或者只写高
src 是 source 的缩写

max-width: 100%;

可替换元素包括： iframe| video | embed| img

form
作用是发送 get 或 post 请求，然后刷新页面

属性： action | autocomplete | method | target

事件： onsubmit

input submit 和 button sumit 有什么区别：button 不是自闭合的，里面还可以添加别的内容

form 里面必须要有一个 submit 的 button 或 input 才能提交

input

textarea

验证器 h5 自带

一般不监听 Input 的 click 事件
form 里面的 Input 要有 name
form 里要放一个 type=submit 才能触发 submit 事件

只用 HTML，也能做网页，俗称 CSS 裸奔

2015年之前，每年 4 月 9 日 是 CSS 裸奔节(CSS Naked Day)



去 维基百科 收集内容

emmet wrap
ol > li*

目录 TOC
table of content

注意：最下面一个锚点往往无法到达页面顶部，可以通过添加额外的空白解决

添加外部资源

添加图片
注意不要让图片变形
如果图片比例不对，需要使用工具裁剪一下
如果图片尺寸过大，无需特殊处理
如果图片体积过大，超过300kb，则需要压缩，如果压缩完还超过300kb，则需要缩小尺寸

不连同一个 wifi，也可以让手机访问电脑的网页

more tools -> remote devices -> port forwarding



