## JavaScript 
[JavaScript](https://www.runoob.com/js/js-errors.html)

JavaScript 错误 - throw、try 和 catch
JavaScript try 和 catch
try 语句允许我们定义在执行时进行错误测试的代码块。

catch 语句允许我们定义当 try 代码块发生错误时，所执行的代码块。

JavaScript 语句 try 和 catch 是成对出现的。

## JavaScript 调试j

[JavaScript 调试](https://www.runoob.com/js/js-debugging.html)

[vue](https://vuejs.org/)

JavaScript 调试工具
在程序代码中寻找错误叫做代码调试。

调试很难，但幸运的是，很多浏览器都内置了调试工具。

内置的调试工具可以开启或关闭，严重的错误信息会发送给用户。

有了调试工具，我们就可以设置断点 (代码停止执行的位置), 且可以在代码执行时检测变量。

浏览器启用调试工具一般是按下 F12 键，并在调试菜单中选择 "Console" 。

## JavaScript install vaiable can not hoist.

##  write your declare in the head of program.
在头部声明你的变量
对于大多数程序员来说并不知道 JavaScript 声明提升。

如果程序员不能很好的理解声明提升，他们写的程序就容易出现一些问题。

## JavaScript 严格模式(use strict)

[JavaScript 严格模式](https://www.runoob.com/js/js-strict.html)

## strict model 

[strict](https://www.runoob.com/js/js-strict.html)

## use javascript misunderstand

[misconception](https://www.runoob.com/js/js-mistakes.html)
## JavaScript 使用误区
[JavaScript 使用误区](https://www.runoob.com/js/js-mistakes.html)

在 JavaScript 程序中如果你在 if 条件语句中使用赋值运算符的等号 (=) 将会产生一个错误结果, 正确的方法是使用比较运算符的两个等号 (==)

在 JavaScript 程序中如果你在 if 条件语句中使用assignment |赋值运算符的等号（=）将会产生一个错误结果，正确的方法是使用比较运算符的两个等号（==）

## JavaScript end

The JavaScript will be end of the sentence.


为什么会有这样的结果呢？因为在 JavaScript 中，实例 4 的代码与下面的代码一致：
```
function myFunction(a) {
    var
    power = 10;  
    return;       // 分号结束，返回 undefined
    a * power;
}
```
解析
如果是一个不完整的语句，如下所示:
```
var
JavaScript 将尝试读取第二行的语句：

power = 10;
```
但是由于这样的语句是完整的:
```
return
```
JavaScript 将自动关闭语句:

return;
在 JavaScript 中，分号是可选的 。

由于 return 是一个完整的语句，所以 JavaScript 将关闭 return 语句。

Note	注意：不用对 return 语句进行断行。

## define array.
定义数组元素，最后不能添加逗号
数组最后一个值的后面添加逗号虽然语法没有问题，但是在不同的浏览器可能得到不同的结果。
```
var colors = [5, 6, 7,]; //这样数组的长度可能为3 也可能为4。
```
正确的定义方式：
```
points = [40, 100, 1, 5, 25, 10];
```
定义对象，最后不能添加逗号
错误的定义方式：
```
websites = {site:"菜鸟教程", url:"www.runoob.com", like:460,}
正确的定义方式：
```
```
websites = {site:"菜鸟教程", url:"www.runoob.com", like:460}
```

## Undefined 不是 Null
在 JavaScript 中, null 用于对象, undefined 用于变量，属性和方法。

对象只有被定义才有可能为 null，否则为 undefined。

如果我们想测试对象是否存在，在对象还没定义时将会抛出一个错误。

错误的使用方式：

## 程序块作用域
在每个代码块中 JavaScript 不会创建一个新的作用域，一般各个代码块的作用域都是全局的。

以下代码的的变量 i 返回 10，而不是 undefined：

## javaScript form.
[javaScript](https://www.runoob.com/js/js-validation.html);

## javascript form validate
[JavaScript 表单验证](https://www.runoob.com/js/js-form-validation.html)

为什么需要表单验证？
数据准确性：确保用户输入的数据符合预期格式，避免无效数据。
***安全性：防止恶意用户提交有害数据，如 SQL 注入、跨站脚本攻击（XSS）等。***
用户体验：及时反馈用户输入错误，帮助用户快速纠正问题。

## JavaScript API 验证：

[JavaScript 验证 API](https://www.runoob.com/js/js-validation-api.html)

## JavaScript keep the keyword

[keep the keyword](https://www.runoob.com/js/js-reserved.html)

JavaScript 保留关键字
In JavaScript, some identifier  keep key word.
This can not use as variable name and function name.


##  JavaScript reserved keyword
[reserved keyword](https://www.runoob.com/js/js-reserved.html)
## JavaScript  This key word
[JavaScript this 关键字](https://www.runoob.com/js/js-this.html)

显式函数绑定
在 JavaScript 中函数也是对象，对象则有方法，apply 和 call 就是函数对象的方法。这两个方法异常强大，他们允许切换函数执行的上下文环境（context），即 this 绑定的对象。

在下面实例中，当我们使用 person2 作为参数来调用 person1.fullName 方法时, this 将指向 person2, 即便它是 person1

## JavaScript let and const 

[javascript let & const](https://www.runoob.com/js/js-let-const.html)

ES2015(ES6) 新增加了两个重要的 JavaScript 关键字: let 和 const。

let 声明的变量只在 let 命令所在的代码块内有效。

const 声明一个只读的常量，一旦声明，常量的值就不能改变。

在 ES6 之前，JavaScript 只有两种作用域： 全局变量 与 函数内的局部变量。


let 声明的变量只在let 命令所在的代码块内有效。
const 声明一个只读的常量，一旦声明，常量的值就不能改变。
在ES6之前，JavaScript只有两种作用域：全局变量与函数内的局部变量。

JavaScript 块级作用域(Block Scope)
使用 var 关键字声明的变量不具备块级作用域的特性，它在 {} 外依然能被访问到。
```
{ 
    var x = 2; 
}
```
// 这里可以使用 x 变量
在 ES6 之前，是没有块级作用域的概念的。

ES6 可以使用 let 关键字来实现块级作用域。

let 声明的变量只在 let 命令所在的代码块 {} 内有效，在 {} 之外不能访问。
```
{ 
    let x = 2;
}
```
// 这里不能使用 x 变量

在第一个实例中，使用了 var 关键字，它声明的变量是全局的，包括循环体内与循环体外。

在第二个实例中，使用 let 关键字， 它声明的变量作用域只在循环体内，循环体外的变量不受影响。

全局变量
在函数体外或代码块外使用 var 和 let 关键字声明的变量也有点类似。

它们的作用域都是 全局的:
```
// 使用 var
var x = 2;       // 全局作用域

// 使用 let
let x = 2;       // 全局作用域

```