# JS 基本语法

### 表达式

表达式分为原始表达式和复杂表达式

#### 原始表达式

原始表达式是表达式的最小单位——它不再包含其他表达式

　　原始表达式分为字面量、关键字和变量；详细来说包括this关键字、标识符引用、字面量引用、数组初始化、对象初始化和分组表达式

```
PrimaryExpression : 
this 
Identifier 
Literal 
ArrayLiteral 
ObjectLiteral 
( Expression )

```

#### 复杂表达式

复杂表达式由原始表达式和操作符(operator)组合而成，包括属性访问表达式、对象创建表达式和函数表达式

```
MemberExpression : 
MemberExpression [ Expression ] 
MemberExpression . IdentifierName 
new MemberExpression Arguments
FunctionExpression 
```

### 语句

　如果表达式在javascript中是短语，那么语句(statement)就是javascript整句或命令。表达式计算出一个值，语句用来执行以使某件事发生。javascript程序无非就是一系列可执行语句的集合，javascript解释器依照语句的编写顺序依次执行

语句包括表达式语句、块语句、空语句、声明语句、条件语句、循环语句和跳转语句

### 标识符


标识符(Identifier)就是一个名字，用来对变量、函数、属性、参数进行命名，或者用做某些循环语句中的跳转位置的标记

```
//变量
var Identifier = 123;
//属性
(new Object).Identifier = 'test';
//函数及参数
function IdentifierName(Identifier1){};
//跳转标记
Identifier:
for(var i = 0; i < 5; i++){
    if(i == 3){
        break Identifier;
    }
}
```


javascript标识符名允许包含字母、数字、美元符号和下划线(但第一个字符不允许是数字)

```
//错误示范
  6num  //开头不能用数字
  %sum //开头不能用除(_ $)外特殊符号,如(%  + /等)
  sum+num //开头中间不能使用除(_ $)外特殊符号，如(%  + /等)
```

### if 语句

　最常见的条件语句是if语句。if语句的条件必须放在if后面的圆括号内，条件的求值结果永远是一个布尔值，即只能是true或false。花括号中的语句，不管它们有多少条，只有在给定条件的求值结果是true的情况下才会执行

当代码有多条分支时，需要使用else if语句。else if语句并不是真正的javascript语句，它是多条if/else语句连在一起时的一种惯用写法 

```
if(n == 1){
    //代码1
}else if(n == 2){
    //代码2
}else if(n == 3){
    //代码3
}else{
    //其他代码
}
```

### while 语句

while语句属于前测试循环语句，也就是说，在循环体内的代码被执行之前，就会对出口条件求值

```
while(expression){
　　statement
}
```

### for 语句

for语句提供了一种比while语句更加方便的循环控制结构，用for循环来重复执行一些代码的好处是循环控制结构更加清晰

　　大部分的循环都具有特定的计数器变量，计数器的三个关键操作是初始化、检测和更新。for语句将这三步明确声明为循环语法的一部分，各自使用一个表达式来表示


```
for(initialize;test;increment){
    statement;    
}
```
```
//等价于:
initialize;
while(test){
    statement
    increment;
}
```

### break 语句

单独使用break语句的作用是立即退出最内层的循环或switch语句

```
for(var i = 0; i < a.length; i++){
    if(a[i] == target) break;
}
```
### continute 语句

continue语句和break语句非常类似，但它不是退出循环，而是转而执行下一次循环

```
//1 3
for(i = 0; i < 5; i++){
    if(i % 2 === 0)continue;
    console.log(i);
}
```


### label 语句

label语句，叫标签语句，通过给语句定义标签，就可以在程序的任何地方通过标签名引用这条语句

标签语句通常与break语句和continue语句配合使用，跳出特定的循环

```
mainloop: while(token != null){
    //Todo
    continue mainloop;
}
```