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

const定义常量与使用let 定义的变量相似：

二者都是块级作用域
都不能和它所在作用域内的其他变量或函数拥有相同的名称
两者还有以下两点区别：

const声明的常量必须初始化，而let声明的变量不用
const 定义常量的值不能通过再赋值修改，也不能再次声明。而 let 定义的变量值可以修改。
```var x = 10;
// 这里输出 x 为 10
{ 
    const x = 2;
    // 这里输出 x 为 2
}
// 这里输出 x 为 10
const 声明的常量必须初始化：

// 错误写法
const PI;
PI = 3.14159265359;

// 正确写法
const PI = 3.14159265359;
```

并非真正的常量
const 的本质: const 定义的变量并非常量，并非不可变，它定义了一个常量引用一个值。使用 const 定义的对象或者数组，其实是可变的。下面的代码并不会报错：


const define a value of variable.When we use const define object and array ,the value can changed. 

##  const 
const 关键字定义的变量则不可以在使用后声明，也就是变量需要先声明再使用。

[const](https://www.runoob.com/js/js-let-const.html)

## JavaScript JSON
[JavaScript JSON](https://www.runoob.com/js/js-json.html)


什么是 JSON?
JSON 英文全称 JavaScript Object Notation
JSON 是一种轻量级的数据交换格式。
JSON是独立的语言 *
JSON 易于理解。
```
{
  "name": "Tom",
  "age": 18,
  "isStudent": true,
  "scores": [90, 85, 88]
  用途：

```
在 Web 应用中传递数据
与服务器通信（如 AJAX、REST API）
注意：

JSON 的键必须用双引号包裹
JSON 只能表示数据，不能包含函数或特殊对象（如 Date）

}
	* JSON 使用 JavaScript 语法，但是 JSON 格式仅仅是一个文本。
文本可以被任何编程语言读取及作为数据格式传递。


Json is a text and can be read by any program language.

JSON 语法规则
数据为 键/值 对。
数据由逗号分隔。
大括号保存对象
方括号保存数组

JSON Object store  bracket

can store multiple key/value
{"name":"Google","url":"www.google.com"}

square bracket []
In javaScript ,array can include object:

"sites":[
    {"name":"google" ,"url":"www.google.com"},
    {"name":"Google","url":"www.google.com"},
    {"name":"Tao bao","url":"www.baidu.com"}
]

```
let text = '{ "sites" : [' +
    '{ "name":"Runoob" , "url":"www.runoob.com" },' +
    '{ "name":"Google" , "url":"www.google.com" },' +
    '{ "name":"Taobao" , "url":"www.taobao.com" } ]}';
 ```


##  JavaScript 
javascript:void(0) 含义
[javaScript void](https://www.runoob.com/js/js-void.html)

##  javaFunction
[javafunction](https://www.runoob.com/js/js-function-definition.html)

Due to the function is not a execution sentence .so don't ues  as the end semicolon

函数存储在变量中，不需要函数名称，通常通过变量名来调用。

Note	上述函数以分号结尾，因为它是一个执行语句。

## 函数提升（Hoisting）

在之前的教程中我们已经了解了 "hoisting(提升)"。

提升（Hoisting）是 JavaScript 默认将当前作用域提升到前面去的行为。

提升（Hoisting）应用在变量的声明与函数的声明。

因此，函数可以在声明之前调用：

myFunction(5);

function myFunction(y) {
    return y * y;
}
使用表达式定义函数时无法提升。

自调用函数
函数表达式可以 "自调用"。

自调用表达式会自动调用。

如果表达式后面紧跟 () ，则会自动调用。

不能自调用声明的函数。

通过添加括号，来说明它是一个函数表达式：

函数的参数用于向函数传递数据，让函数可以根据不同的输入执行不同的操作。
参数让函数更灵活、可复用。

举例：
```
function add(a, b) {
  return a + b;
}
add(2, 3); // 参数 2 和 3 传递给函数，结果是 5

```

总结：
参数就是函数运行时需要用到的变量或数据。

## arrow function()
[arrow function()](https://www.runoob.com/js/js-function-definition.html)

箭头函数
ES6 新增了箭头函数。

箭头函数表达式的语法比普通函数表达式更简洁。
```
(参数1, 参数2, …, 参数N) => { 函数声明 }

(参数1, 参数2, …, 参数N) => 表达式(单一)
// 相当于：(参数1, 参数2, …, 参数N) =>{ return 表达式; }

```
当只有一个参数时，圆括号是可选的：
```
(单一参数) => {函数声明}
单一参数 => {函数声明}
没有参数的函数应该写成一对圆括号:

() => {函数声明}
```


## JavaScript Explicit Parameters   and implicit parameters

函数显式参数(Parameters)与隐式参数(Arguments)
```
functionName(parameter1, parameter2, parameter3) {
    // 要执行的代码……
}

```
函数显式参数在函数定义时列出。

函数隐式参数在函数调用时传递给函数真正的值。
## ES6 函数可以自带参数
ES6 支持函数带有默认参数，就判断 undefined 和 || 的操作：

## arguments 对象
JavaScript 函数有个内置的对象 arguments 对象。

arguments 对象包含了函数调用的参数数组。

通过这种方式你可以很方便的找到最大的一个参数的值

## Global Object
[Global Object](https://www.runoob.com/js/js-function-invocation.html)

## 
***函数作为全局对象调用，会使 this 的值成为全局对象。***
使用 window 对象作为一个变量容易造成程序崩溃。

### JavaScript 中对象的方法（Method）和函数（Function）的区别

在 JavaScript 中，**函数（Function）** 和 **对象的方法（Method）** 都是可调用的代码块，但它们在定义、访问和行为上存在关键区别。简单来说：
- **函数** 是独立的、可重用的代码单元，可以单独定义和调用。
- **方法** 是函数的“特殊形式”，它被绑定到对象上，作为对象的属性存在，主要用于描述对象的行为。

#### 主要区别
以下是它们的核心差异，我用表格总结以便比较：

| 方面          | 函数 (Function)                          | 方法 (Method)                              |
|---------------|------------------------------------------|--------------------------------------------|
| **定义方式** | 独立定义，使用 `function` 关键字或箭头函数（如 `function add(a, b) { return a + b; }`）。 | 函数作为对象的属性定义（如 `obj.method = function() { ... };`）。 |
| **访问方式** | 直接调用（如 `add(1, 2)`），或通过变量（如 `const fn = add; fn(1, 2)`）。 | 通过对象调用（如 `obj.method()`），类似于 `obj.method.call(obj)`。 |
| **this 关键字** | `this` 的值取决于调用上下文（全局调用时通常为 `window` 或 `undefined`，箭头函数继承外层 `this`）。 | `this` 默认指向调用该方法的对象（除非使用箭头函数或显式绑定）。 |
| **作用域**    | 全局或模块作用域，可在任何地方调用。     | 绑定到对象，访问对象内部的属性（如 `this.property`）。 |
| **示例场景** | 通用工具函数，如计算或验证。             | 对象行为，如数组的 `push()` 方法操作自身。 |

#### 详细解释
1. **函数的独立性**：
   - 函数可以脱离任何对象存在。它是一个一等公民（first-class citizen），可以像变量一样赋值、传递或返回。
   - 示例：
     ```javascript
     function greet(name) {
       return `Hello, ${name}!`;
     }
     console.log(greet('World'));  // 输出: Hello, World!
     ```

2. **方法的绑定性**：
   - 方法必须是对象的一个属性。当你调用它时，JavaScript 会自动将 `this` 绑定到该对象。这使得方法能轻松访问对象的其他属性或方法。
   - 示例：
     ```javascript
     const person = {
       name: 'Alice',
       greet: function() {  // 这是一个方法
         return `Hello, ${this.name}!`;  // this 指向 person 对象
       }
     };
     console.log(person.greet());  // 输出: Hello, Alice!
     ```
   - 如果你将方法提取出来作为普通函数调用，`this` 就会丢失：
     ```javascript
     const extracted = person.greet;
     console.log(extracted());  // 输出: Hello, undefined!（严格模式下为错误）
     ```

3. **箭头函数的特殊情况**：
   - 如果方法使用箭头函数定义（如 `greet: () => { ... }`），则 `this` 不会绑定到对象，而是继承外层作用域。这在某些场景（如事件处理）有用，但会改变方法的“绑定”行为。

#### 实际应用建议
- 用**函数** 处理不依赖对象的逻辑（如数学计算）。
- 用**方法** 封装对象的操作（如 DOM 元素的 `addEventListener` 方法）。
- 记住：所有方法本质上都是函数，但不是所有函数都是方法。

如果需要更多代码示例或特定场景的演示，请提供细节！

## 作为函数方法调用函数
在 JavaScript 中, 函数是对象。JavaScript 函数有它的属性和方法。

call() 和 apply() 是预定义的函数方法。 两个方法可用于调用函数，两个方法的第一个参数必须是对象本身。

## JavaScript 闭包

[JavaScript 闭包](https://www.runoob.com/js/js-function-closures.html)

后面一个实例中， a 是一个 全局 变量。

在web页面中全局变量属于 window 对象。

全局变量可应用于页面上的所有脚本。

在第一个实例中， a 是一个 局部 变量。

局部变量只能用于定义它函数内部。对于其他的函数或脚本代码是不可用的。

全局和局部变量即便名称相同，它们也是两个不同的变量。修改其中一个，不会影响另一个的值。

Note	变量声明时如果不使用 var 关键字，那么它就是一个全局变量，即便它在函数内定义。

