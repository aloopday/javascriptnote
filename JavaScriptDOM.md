## JavaScript HTML DOM
[JavaScript HTML DOM](https://www.runoob.com/js/js-htmldom.html)

![alt text](image-5.png)
JavaScript 能够改变页面中的所有 HTML 元素
JavaScript 能够改变页面中的所有 HTML 属性
JavaScript 能够改变页面中的所有 CSS 样式
JavaScript 能够对页面中的所有事件做出反应

## Find element
id , element .class
HTML DOM 教程
在本教程接下来的篇幅中，您将学到：

如何改变 HTML 元素的内容 (innerHTML)
如何改变 HTML 元素的样式 (CSS)
如何对 HTML DOM 事件做出反应
如何添加或删除 HTML 元素

## HTML 

[HTML DOM](https://www.w3schools.com/js/js_htmldom.asp)


[HTML DOM](https://www.runoob.com/js/js-htmldom-html.html)

JavaScript HTML DOM - 改变 HTML

## HTML stype property

[Javascript to change style property](https://www.runoob.com/js/js-htmldom-css.html)

## Html event .

HTML DOM 允许我们通过触发事件来执行代码。

比如以下事件：

元素被点击。
页面加载完成。
输入框被修改。
……
在接下来的章节，你会学到更多关于事件的知识。

本例改变了 id="id1" 的 HTML 元素的样式，当用户点击按钮时：

## JavaScript HTML DOM 事件
[JavaScriptDOM](https://www.runoob.com/js/js-htmldom-events.html)

对事件做出反应
我们可以在事件发生时执行 JavaScript，比如当用户在 HTML 元素上点击时。

如需在用户点击某个元素时执行代码，请向一个 HTML 事件属性添加 JavaScript 代码：

onclick=JavaScript
HTML 事件的例子：

当用户点击鼠标时
当网页已加载时
当图像已加载时
当鼠标移动到元素上时
当输入字段被改变时
当提交 HTML 表单时
当用户触发按键时

## JavsScript envent listner
[envent listner](https://www.runoob.com/js/js-htmldom-eventlistener.html)

## JavaScript Node
[JavaScript Node](https://www.runoob.com/js/js-htmldom-elements.html)

如果能够在不引用父元素的情况下删除某个元素，就太好了。
不过很遗憾。DOM 需要清楚您需要删除的元素，以及它的父元素。
以下代码是已知要查找的子元素，然后查找其父元素，再删除这个子元素（删除节点必须知道父节点）：

var child = document.getElementById("p1");
child.parentNode.removeChild(child);

## JavScript HTML DOM (Collection)
[JavaScript HTML DOM](https://www.runoob.com/js/js-htmldom-collections.html)


HTMLCollection 与 NodeList 的区别
HTMLCollection 是 HTML 元素的集合。

NodeList 是一个文档节点的集合。

NodeList 与 HTMLCollection 有很多类似的地方。

NodeList 与 HTMLCollection 都与数组对象有点类似，可以使用索引 (0, 1, 2, 3, 4, ...) 来获取元素。

NodeList 与 HTMLCollection 都有 length 属性。

HTMLCollection 元素可以通过 name，id 或索引来获取。

NodeList 只能通过索引来获取。

只有 NodeList 对象有包含属性节点和文本节点。

节点列表不是一个数组！

节点列表看起来可能是一个数组，但其实不是。

你可以像数组一样，使用索引来获取元素。

节点列表无法使用数组的方法： valueOf(), pop(), push(), 或 join() 。

add mthod to object function

JavaScript 类
JavaScript 是面向对象的语言，但 JavaScript 不使用类。

在 JavaScript 中，不会创建类，也不会通过类来创建对象（就像在其他面向对象的语言中那样）。

JavaScript 基于 prototype，而不是基于类的。

## JavaScript for...in 循环
[Javascript for...in](https://www.runoob.com/js/js-objects.html)

```
for (variable in object)
{
    执行的代码……
}

```

## [proto](https://www.runoob.com/js/js-object-prototype.html)

## 原型链
在 JavaScript 中，对象通过原型链（prototype chain）来实现继承。当一个对象尝试访问一个属性或方法时，JavaScript 会首先检查该对象自身是否有这个属性或方法。如果没有，它会沿着原型链向上查找。
```
let obj = {};
console.log(obj.toString()); // 输出: [object Object]

```
// 这个 `toString` 方法实际上是从 `Object.prototype` 继承过来的
在上面的例子中，obj 对象没有定义 toString 方法，因此 JavaScript 沿着原型链查找，最终在 Object.prototype 中找到该方法。

## 修改原型
你可以动态地修改对象的原型，这样可以影响到所有基于该原型创建的对象：

实例
```
function Person(name) {
    this.name = name;
}

Person.prototype.sayHello = function() {
    console.log("Hello, my name is " + this.name);
};

let bob = new Person("Bob");
bob.sayHello(); // 输出: Hello, my name is Bob

// 修改原型
Person.prototype.sayGoodbye = function() {
    console.log("Goodbye from " + this.name);
};
```
bob.sayGoodbye(); // 输出: Goodbye from Bob
在这个例子中，我们在 Person.prototype 上添加了一个新的方法 sayGoodbye，bob 对象立即就可以访问到这个新方法。

Object.create 方法
Object.create 方法允许你创建一个新对象，并将其原型设置为指定的对象。
```
let personPrototype = {
    sayHello: function() {
        console.log("Hello, my name is " + this.name);
    }
};

let alice = Object.create(personPrototype);
alice.name = "Alice";
alice.sayHello(); // 输出: Hello, my name is Alice
```
在这个例子中，alice 的原型是 personPrototype，因此 alice 对象可以访问 sayHello 方法。

## prototype 继承
所有的 JavaScript 对象都会从一个 prototype（原型对象）中继承属性和方法：

Date 对象从 Date.prototype 继承。
Array 对象从 Array.prototype 继承。
Person 对象从 Person.prototype 继承。
所有 JavaScript 中的对象都是位于原型链顶端的 Object 的实例。

JavaScript 对象有一个指向一个原型对象的链。当试图访问一个对象的属性时，它不仅仅在该对象上搜寻，还会搜寻该对象的原型，以及该对象的原型的原型，依次层层向上搜索，直到找到一个名字匹配的属性或到达原型链的末尾。

Date 对象, Array 对象, 以及 Person 对象从 Object.prototype 继承。

添加属性和方法
有的时候我们想要在所有已经存在的对象添加新的属性或方法。

另外，有时候我们想要在对象的构造函数中添加属性或方法。

使用 prototype 属性就可以给对象的构造函数添加新的属性



