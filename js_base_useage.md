# JS 对象基本用法

### 创建对象

有以下三种方式来创建对象，包括new构造函数、对象直接量和Object.create()函数

【1】new构造函数

　　使用new操作符后跟Object构造函数用以初始化一个新创建的对象

```
var person = new Object();
//如果不给构造函数传递参数可以不加括号 var person = new Object;
person.name = 'bai';
person.age = 29;
```


【2】对象字面量

javascript提供了叫做字面量的快捷方式，用于创建大多数原生对象值。使用字面量只是隐藏了与使用new操作符相同的基本过程，于是也可以叫做语法糖

　　对象字面量是由若干名值对组成的映射表，名值对中间用冒号分隔，整个映射表用花括号括起来

　　不同属性之间用逗号分隔，属性名可以是任意字符串，属性值可以是任意类型表达式，表达式的值是属性值

```
var person = {
    name : 'bai',
    age : 29,
    5 : true
};
```

【3】Object.create()

ES5定义了一个名为Object.create()的方法，它创建一个新对象，第一个参数就是这个对象的原型，第二个可选参数用以对对象的属性进行进一步描述
```
var o1 = Object.create({x:1,y:1}); //o1继承了属性x和y
console.log(o1.x);//1
```

### 属性查询

属性查询一般有两种方法，包括点运算符和方括号运算符

```
var o = {
  p: 'Hello World'
};
o.p // "Hello World"
o['p'] // "Hello World"
```

如果要在对象字面量内部对属性名使用表达式，则需要使用ES6的可计算属性名

```
var a = 1;
var person = {
    [a + 3]: 'abc'
};
person[4];//'abc'
```

### 属性设置或增加


属性设置又称为属性赋值，与属性查询相同，具有点运算符和方括号运算符这两种方法

```
o.p = 'abc';
o['p'] = 'abc';
```
增加对象的属性与属性设置相同

### 属性删除

使用delete运算符可以删除对象属性

```
var o = {
    a : 1
};
console.log(o.a);//1
console.log('a' in o);//true
console.log(delete o.a);//true
console.log(o.a);//undefined
console.log('a' in o);//false
```

### 属性继承

每一个javascript对象都和另一个对象相关联。“另一个对象”就是我们熟知的原型，每一个对象都从原型继承属性。所有通过对象直接量创建的对象都具有同一个原型对象，并可以通过Object.prototype获得对原型对象的引用

```
var obj = {};
console.log(obj.__proto__ === Object.prototype);//true
```
对象本身具有的属性叫自有属性(own property)，从原型对象继承而来的属性叫继承属性

```
var o = {a:1};
var obj = Object.create(o);
obj.b = 2;
//继承自原型对象o的属性a
console.log(obj.a);//1
//自有属性b
console.log(obj.b);//2
```
【in】
in操作符可以判断属性在不在该对象上，但无法区别自有还是继承属性

```
var o = {a:1};
var obj = Object.create(o);
obj.b = 2;
console.log('a' in obj);//true
console.log('b' in obj);//true
console.log('b' in o);//false
```
【hasOwnProperty()】

通过hasOwnProperty()方法可以确定该属性是自有属性还是继承属性

```
var o = {a:1};
var obj = Object.create(o);
obj.b = 2;
console.log(obj.hasOwnProperty('a'));//false
console.log(obj.hasOwnProperty('b'));//true
```