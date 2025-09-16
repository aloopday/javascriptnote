## javascript advance
[Javascript](https://www.w3schools.com/js/js_classes.asp)

[JavasCript](https://www.runoob.com/js/js-class-inheritance.html)

extend is the key word
super to invoke the parent class

![alt text](image-4.png)
JavaScript 类继承使用 extends 关键字。

"super" 方法用于调用父类的构造函数。
super() 方法引用父类的构造方法。

通过在构造方法中调用 super() 方法，我们调用了父类的构造方法，这样就可以访问父类的属性和方法。

继承对于代码可复用性很有用。

JavaScript 并没有像其他编程语言一样具有传统的类，而是基于原型的继承模型。

ES6 引入了类和 class 关键字，但底层机制仍然基于原型继承。

## 使用原型链继承 
[使用原型链继承](https://www.runoob.com/js/js-class-inheritance.html)
```
function Animal(name) {
  this.name = name;
}
 
Animal.prototype.eat = function() {
  console.log(this.name + " is eating.");
};
 
function Dog(name, breed) {
  Animal.call(this, name);
  this.breed = breed;
}
 
// 建立原型链，让 Dog 继承 Animal
Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;
 
Dog.prototype.bark = function() {
  console.log(this.name + " is barking.");
};
 
var dog = new Dog("Buddy", "Labrador");
dog.eat();  // 调用从 Animal 继承的方法
dog.bark(); // 调用 Dog 的方法
```

## 使用 ES6 类继承

ES6 引入了 class 关键字，使得定义类和继承更加清晰，extends 关键字用于建立继承关系，super 关键字用于在子类构造函数中调用父类的构造函数。

## JavaScript Inheritance
[JavaScript Inheritance](https://www.w3schools.com/js/js_class_inheritance.asp)
