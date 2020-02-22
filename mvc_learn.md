# 浅析 MVC

### MVC

M module(数据模型) 负责操作数据
V view(视图) 负责 UI 界面
C controller(控制器) 负责业务逻辑等其他操作

```
const Model= {
    data:{},    //绑定数据
    init: function(){},     //增删改查
    add: function(){},
    delete: function(){},
    get: function(){}
}
const View={
    el:'',  //挂载元素
    init: function(){},    //初始化
    template:'',            //模板
    render: function(){}   //渲染函数
}
const controller = {
    init(): function{},         //初始化
    bindEvents: function(){},   //绑定事件
}
```


### EventBus

EventBus 也就是观察者模式，又被称为发布-订阅（Publish/Subscribe）模式，它定义了一种一对多的依赖关系，让多个观察者对象同时监听某一个主题对象。这个主题对象在状态变化时，会通知所有的观察者对象，使他们能够自动更新自己

1、绑定事件 eventBus.on()
```
eventBus.on("eventName",callback)
```

2、触发事件 eventBus.emit()
```
eventBus.emit("eventName",[...args])
```

3、解绑事件 eventBus.off()
```
eventBus.off("eventName",callback)
```


### 表驱动编程

表驱动法是一种编程模式(scheme)——从表里面查找信息而不使用逻辑语句(if和case)。事实上，凡是能通过逻辑语句来选择的事物，都可以通过查表来选择。对简单的情况而言，使用逻辑语句更为容易和直白。但随着逻辑链的越来越发杂，查表法也就愈发显得更具吸引力

```
var obj={
    1：add1,
    2: add2,
    3：add3,
    4：add4,
    5：add5,
}
obj[flg]()
```


### 模块化

模块化是指解决一个复杂问题时自顶向下逐层把系统划分成若干模块的过程，有多种属性，分别反映其内部特性

对于前端而言，模块化是指将一个复杂的程序依据一定的规则(规范)封装成几个块(文件), 并进行组合在一起，并且块的内部数据与实现是私有的, 只是向外部暴露一些接口(方法)与外部其它模块通信

模块化编程是非常重要的一种编程模式，优势如下

1、多人协作互不干扰，模块化避免了变量污染，并且可以使得分工更加容易

2、灵活架构，焦点分离，可以将独立的功能从主干中分离开来单独开发，增加效率

3、方便模块间组合、分解 、解耦，降低各个功能模块间的耦合度，方便维护和管理

4、方便单个模块功能调试、升级
