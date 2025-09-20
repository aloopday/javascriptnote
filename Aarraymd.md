## Array md
[Array](https://www.runoob.com/js/js-obj-array.html)
数组对象的作用是：使用单独的变量名来存储一系列的值。
数组对象的作用是，使用单独的变量名来存储一系列的值。

创建一个数组
创建一个数组，有三种方法。

下面的代码定义了一个名为 myCars的数组对象：

1: 常规方式:

var myCars=new Array();
myCars[0]="Saab";      
myCars[1]="Volvo";
myCars[2]="BMW";
2: 简洁方式:

var myCars=new Array("Saab","Volvo","BMW");
3: 字面:

var myCars=["Saab","Volvo","BMW"];

在你的代码中，`join()` 是一个 **JavaScript 数组方法**，其作用是将数组中的所有元素连接成一个字符串，并返回该字符串。你可以通过指定分隔符（separator）来定义元素之间的连接方式。如果未提供分隔符，默认使用逗号（`,`）。

### 具体解释 `join()` 在代码中的作用
你的代码：
```javascript
function myFunction(){
    var fruits = ["Banana", "Orange", "Apple", "Mango"];
    var x = document.getElementById("demo");
    x.innerHTML = fruits.join();
}
```

1. **数组 `fruits`**：
   - `fruits` 是一个包含字符串的数组：`["Banana", "Orange", "Apple", "Mango"]`。

2. **调用 `fruits.join()`**：
   - `join()` 方法将 `fruits` 数组中的所有元素合并为一个字符串。
   - 默认情况下（没有指定分隔符），`join()` 使用逗号（`,`）作为分隔符。
   - 因此，`fruits.join()` 的结果是字符串：`"Banana,Orange,Apple,Mango"`。

3. **设置 `innerHTML`**：
   - `document.getElementById("demo")` 获取页面中 ID 为 `demo` 的 HTML 元素（例如 `<p id="demo"></p>`）。
   - `x.innerHTML = fruits.join()` 将 `join()` 生成的字符串（`"Banana,Orange,Apple,Mango"`）设置为该元素的 HTML 内容。
   - 最终，页面上的 `demo` 元素会显示：`Banana,Orange,Apple,Mango`。

### `join()` 方法的通用作用
- **语法**：`array.join(separator)`
  - `separator`（可选）：指定元素之间的分隔符（字符串）。如果省略，默认使用 `,`。
  - 返回值：由数组元素连接而成的字符串。
- **示例**：
  ```javascript
  var arr = ["a", "b", "c"];
  console.log(arr.join());      // 输出: "a,b,c"
  console.log(arr.join(""));    // 输出: "abc"
  console.log(arr.join("-"));   // 输出: "a-b-c"
  ```

### 代码中的 `join()` 细节
- 在你的代码中，`fruits.join()` 没有指定分隔符，因此使用默认的逗号分隔符。
- 如果你想用其他分隔符（例如空格或破折号），可以改写为：
  - `fruits.join(" ")` → 输出 `"Banana Orange Apple Mango"`
  - `fruits.join("-")` → 输出 `"Banana-Orange-Apple-Mango"`

### 运行代码的前提
- HTML 中需要有一个 ID 为 `demo` 的元素（例如 `<p id="demo"></p>`）。
- 需要触发 `myFunction`，例如通过按钮点击或页面加载：
  ```html
  <p id="demo"></p>
  <button onclick="myFunction()">Show Fruits</button>
  ```

### 总结
`join()` 的作用是将数组元素合并为一个字符串，方便在页面上显示或进一步处理。在你的代码中，`fruits.join()` 将 `["Banana", "Orange", "Apple", "Mango"]` 转换为 `"Banana,Orange,Apple,Mango"`，并显示在 ID 为 `demo` 的 HTML 元素中。

如果你有关于 `join()` 的其他问题或想修改代码（例如更改分隔符），请告诉我！