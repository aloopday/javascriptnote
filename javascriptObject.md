## javascript Object 

[javascript object](https://www.runoob.com/js/js-objects.html)
JavaScript 对象
对象只是一种特殊的数据。对象拥有属性和方法。


JavaScript 对象就是一个 name:value 集合。

##  JavaScript 的对象是可变的
对象是可变的，它们是通过引用来传递的。

以下实例的 person 对象不会创建副本：
```
var x = person;  // 不会创建 person 的副本，是引用
```
如果修改 x ，person 的属性也会改变：