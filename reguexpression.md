## JavaScript RegExp 对象

[JavaScript RegExp 对象](https://www.runoob.com/js/js-obj-regexp.html)

什么是 RegExp？
正则表达式描述了字符的模式对象。

当您检索某个文本时，可以使用一种模式来描述要检索的内容。RegExp 就是这种模式。

简单的模式可以是一个单独的字符。

更复杂的模式包括了更多的字符，并可用于解析、格式检查、替换等等。

您可以规定字符串中的检索位置，以及要检索的字符类型，等等。\

1. What is a Regex in JavaScript?In JavaScript, a regex is an object that describes a pattern of characters. You can use it to:Match: Check if a string contains a pattern.
Search: Find the position of a pattern in a string.
Replace: Replace parts of a string that match a pattern.
Split: Split a string based on a pattern.

Regex patterns can be simple (e.g., matching a specific word) or complex (e.g., validating an email address).


A **Regular Expression (regex)** in JavaScript is a powerful tool for pattern matching and manipulating text strings. It’s a sequence of characters that defines a search pattern, often used for tasks like validation, searching, and replacing parts of strings. Below, I’ll explain the key concepts of JavaScript regex, how it works, and provide examples to make it clear.

---

### **1. What is a Regex in JavaScript?**
In JavaScript, a regex is an object that describes a pattern of characters. You can use it to:
- **Match**: Check if a string contains a pattern.
- **Search**: Find the position of a pattern in a string.
- **Replace**: Replace parts of a string that match a pattern.
- **Split**: Split a string based on a pattern.

Regex patterns can be simple (e.g., matching a specific word) or complex (e.g., validating an email address).

---

### **2. Creating a Regex in JavaScript**
There are two ways to create a regex in JavaScript:

1. **Literal Notation** (using `/pattern/flags`):
   ```javascript
   const regex = /cat/;
   ```
   - The pattern is enclosed in forward slashes (`/`).
   - Flags (optional) come after the second slash to modify behavior.

2. **RegExp Constructor** (useful for dynamic patterns):
   ```javascript
   const regex = new RegExp('cat');
   ```

**Common Flags**:
- `g`: Global (matches all occurrences, not just the first).
- `i`: Case-insensitive (e.g., `Cat` and `cat` are treated the same).
- `m`: Multiline (affects `^` and `$` to match the start/end of each line).
- `s`: Dot-all (allows `.` to match newline characters).
- `u`: Unicode (enables full Unicode matching).
- `y`: Sticky (matches only from the last index).

Example:
```javascript
const regex = /cat/gi; // Matches "cat", "Cat", "CAT", etc., globally.
```

---

### **3. Key Regex Syntax**
Here’s a breakdown of common regex components:

| **Symbol** | **Meaning** | **Example** | **Matches** |
|------------|-------------|-------------|-------------|
| `.` | Any character (except newline, unless `s` flag is used) | `c.t` | `cat`, `cot`, `c#t` |
| `^` | Start of string (or line with `m` flag) | `^cat` | `cat` at string start |
| `$` | End of string (or line with `m` flag) | `cat$` | `cat` at string end |
| `*` | 0 or more occurrences | `ca*t` | `ct`, `cat`, `caat` |
| `+` | 1 or more occurrences | `ca+t` | `cat`, `caat` |
| `?` | 0 or 1 occurrence | `ca?t` | `ct`, `cat` |
| `{n}` | Exactly `n` occurrences | `a{2}` | `aa` |
| `{n,m}` | Between `n` and `m` occurrences | `a{1,3}` | `a`, `aa`, `aaa` |
| `[]` | Any character in the set | `[abc]` | `a`, `b`, or `c` |
| `[^]` | Any character not in the set | `[^abc]` | Any character except `a`, `b`, `c` |
| `\d` | Digit (0-9) | `\d` | `0`, `1`, etc. |
| `\w` | Word character (a-z, A-Z, 0-9, _) | `\w` | `a`, `Z`, `5`, `_` |
| `\s` | Whitespace (space, tab, newline) | `\s` | ` `, `\t`, `\n` |
| `|` | OR operator | `cat|dog` | `cat` or `dog` |
| `()` | Group characters | `(ab)+` | `ab`, `abab`, etc. |
| `\` | Escape special characters | `\.` | Literal `.` |

---

### **4. Using Regex in JavaScript**
JavaScript provides several methods to work with regex:

1. **Testing for a Match (`test`)**:
   - Returns `true` if the pattern is found, `false` otherwise.
   ```javascript
   const regex = /cat/;
   console.log(regex.test('I have a cat')); // true
   console.log(regex.test('I have a dog')); // false
   ```

2. **Finding Matches (`match`)**:
   - Returns an array of matches or `null` if no match is found.
   ```javascript
   const str = 'The cat and the Cat';
   const regex = /cat/gi;
   console.log(str.match(regex)); // ['cat', 'Cat']
   ```

3. **Searching (`search`)**:
   - Returns the index of the first match or `-1` if not found.
   ```javascript
   const str = 'The cat is here';
   console.log(str.search(/cat/)); // 4
   ```

4. **Replacing (`replace` or `replaceAll`)**:
   - Replaces matched patterns with a new string.
   ```javascript
   const str = 'The cat is here';
   console.log(str.replace(/cat/, 'dog')); // 'The dog is here'
   console.log(str.replaceAll(/cat/gi, 'dog')); // Replaces all case-insensitive 'cat'
   ```

5. **Splitting (`split`)**:
   - Splits a string based on a pattern.
   ```javascript
   const str = 'cat,dog,mouse';
   console.log(str.split(/,/)); // ['cat', 'dog', 'mouse']
   ```

6. **Exec (`exec`)**:
   - Returns an array with details of the first match (or `null`) and updates the `lastIndex` property for global searches.
   ```javascript
   const regex = /cat/g;
   const str = 'cat and Cat';
   console.log(regex.exec(str)); // ['cat', index: 0, input: 'cat and Cat', groups: undefined]
   console.log(regex.exec(str)); // ['Cat', index: 8, input: 'cat and Cat', groups: undefined]
   ```

---

### **5. Practical Examples**
Here are some common use cases with JavaScript regex:

#### **Example 1: Validate an Email**
```javascript
const regex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
const email = 'user@example.com';
console.log(regex.test(email)); // true
console.log(regex.test('invalid.email@com')); // false
```

- Breakdown:
  - `^`: Start of string.
  - `[a-zA-Z0-9._%+-]+`: One or more letters, digits, or allowed symbols.
  - `@`: Literal `@`.
  - `[a-zA-Z0-9.-]+`: Domain name (letters, digits, dots, hyphens).
  - `\.`: Literal dot.
  - `[a-zA-Z]{2,}`: Top-level domain (e.g., `com`, `org`).
  - `$`: End of string.

#### **Example 2: Extract All Numbers**
```javascript
const str = 'My numbers are 123 and 456!';
const regex = /\d+/g;
console.log(str.match(regex)); // ['123', '456']
```

#### **Example 3: Replace Case-Insensitive Words**
```javascript
const str = 'The Cat and the CAT';
const regex = /cat/gi;
console.log(str.replace(regex, 'dog')); // 'The dog and the dog'
```

#### **Example 4: Capture Groups**
Use parentheses `()` to capture parts of a match for reuse.
```javascript
const str = 'Date: 2025-09-20';
const regex = /(\d{4})-(\d{2})-(\d{2})/;
const match = str.match(regex);
console.log(match); // ['2025-09-20', '2025', '09', '20']
console.log(`Year: ${match[1]}, Month: ${match[2]}, Day: ${match[3]}`);
```

---

### **6. Tips for Using Regex**
- **Test Your Regex**: Use tools like regex101.com to debug and test patterns.
- **Escape Special Characters**: Use `\` before special characters like `.`, `*`, `+`, etc., if you want to match them literally.
- **Performance**: Complex regexes on large strings can be slow, so optimize patterns when possible.
- **Readability**: Break complex regexes into smaller parts or use comments with the `x` flag (in RegExp constructor) for clarity.

---

### **7. Common Pitfalls**
- **Greedy vs. Lazy Matching**: By default, quantifiers like `*` and `+` are greedy (match as much as possible). Use `?` for lazy matching.
  ```javascript
  const str = '<p>text</p><p>more</p>';
  console.log(str.match(/<p>.*<\/p>/)); // Greedy: ['<p>text</p><p>more</p>']
  console.log(str.match(/<p>.*?<\/p>/g)); // Lazy: ['<p>text</p>', '<p>more</p>']
  ```
- **Unicode Issues**: Use the `u` flag for proper Unicode support if matching special characters.
- **Case Sensitivity**: Forgetting the `i` flag can cause missed matches.

---

### **8. Resources**
- **MDN Web Docs**: Detailed JavaScript regex documentation (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions).
- **Regex101**: Online regex tester with JavaScript support (https://regex101.com).
- **RegExr**: Another great tool for learning and testing regex (https://regexr.com).

---

If you have a specific regex problem or want an example for a particular use case (e.g., validating a phone number, extracting URLs, etc.), let me know, and I’ll provide a tailored solution!


正则表达式（regex）的**元字符**是具有特殊含义的字符，用于定义匹配模式。在 JavaScript 中，元字符在正则表达式中起着关键作用，用于匹配特定的字符、位置或模式。如果需要匹配元字符的字面值，必须使用反斜杠 `\` 进行转义。以下是对 JavaScript 正则表达式中元字符的详细解释，包括其功能和示例。

---

### **1. 什么是元字符？**
元字符是正则表达式中的特殊字符，它们不表示字面字符，而是表示某种匹配规则或模式。例如，`.` 表示匹配任意字符，`*` 表示匹配前面的字符 0 次或多次。

JavaScript 中的常见元字符包括：
- `.`, `*`, `+`, `?`, `|`, `()`, `[]`, `{}`, `^`, `$`, `\`

---

### **2. 元字符列表及其功能**
以下是 JavaScript 正则表达式中常见的元字符及其作用：

| **元字符** | **功能** | **示例** | **匹配** |
|------------|----------|----------|----------|
| `.` | 匹配任意单个字符（除换行符 `\n`、`\r` 等外，除非使用 `s` 标志） | `c.t` | `cat`, `cot`, `c#t` |
| `*` | 匹配前面的字符或子表达式 0 次或多次 | `ca*t` | `ct`, `cat`, `caat` |
| `+` | 匹配前面的字符或子表达式 1 次或多次 | `ca+t` | `cat`, `caat` |
| `?` | 匹配前面的字符或子表达式 0 次或 1 次 | `ca?t` | `ct`, `cat` |
| `|` | 表示“或”，匹配左右任一模式 | `cat|dog` | `cat` 或 `dog` |
| `()` | 定义子表达式（分组），用于捕获或限定范围 | `(ab)+` | `ab`, `abab` |
| `[]` | 定义字符集，匹配集合中的任意单个字符 | `[abc]` | `a`, `b`, 或 `c` |
| `[^]` | 否定字符集，匹配不在集合中的任意单个字符 | `[^abc]` | 除 `a`, `b`, `c` 外的字符 |
| `{n}` | 匹配前面的字符或子表达式正好 n 次 | `a{2}` | `aa` |
| `{n,}` | 匹配前面的字符或子表达式至少 n 次 | `a{2,}` | `aa`, `aaa`, ... |
| `{n,m}` | 匹配前面的字符或子表达式 n 到 m 次 | `a{1,3}` | `a`, `aa`, `aaa` |
| `^` | 匹配字符串或行的开头（若有 `m` 标志则为每行开头） | `^cat` | `cat`（在字符串开头） |
| `$` | 匹配字符串或行的结尾（若有 `m` 标志则为每行结尾） | `cat$` | `cat`（在字符串结尾） |
| `\` | 转义字符，用于匹配元字符的字面值或定义特殊序列 | `\.` | 字面 `.` |

---

### **3. 元字符的详细说明与示例**

#### **(1) `.`（点号）**
- **功能**：匹配任意单个字符（除换行符 `\n`, `\r`, `\u2028`, `\u2029` 外，除非使用 `s` 标志）。
- **示例**：
  ```javascript
  const str = "cat cot c#t";
  const regex = /c.t/g;
  console.log(str.match(regex)); // ['cat', 'cot', 'c#t']
  ```
- **注意**：使用 `s` 标志（dotAll）时，`.` 也可以匹配换行符：
  ```javascript
  const str = "cat\ncot";
  const regex = /.+/s;
  console.log(str.match(regex)); // ['cat\ncot']
  ```

#### **(2) `*`（星号）**
- **功能**：匹配前面的字符或子表达式 0 次或多次（贪婪匹配）。
- **示例**：
  ```javascript
  const str = "ct cat caat";
  const regex = /ca*t/g;
  console.log(str.match(regex)); // ['ct', 'cat', 'caat']
  ```
- **注意**：`*` 是贪婪的，会尽可能多地匹配。可以用 `?` 改为非贪婪：
  ```javascript
  const str = "<p>text</p><p>more</p>";
  const regex = /<p>.*?</p>/g; // 非贪婪
  console.log(str.match(regex)); // ['<p>text</p>', '<p>more</p>']
  ```

#### **(3) `+`（加号）**
- **功能**：匹配前面的字符或子表达式 1 次或多次。
- **示例**：
  ```javascript
  const str = "ct cat caat";
  const regex = /ca+t/g;
  console.log(str.match(regex)); // ['cat', 'caat']
  ```
- **注意**：与 `*` 不同，`+` 要求至少匹配 1 次，因此 `ct` 不匹配。

#### **(4) `?`（问号）**
- **功能**：
  - 匹配前面的字符或子表达式 0 次或 1 次。
  - 放在量词（如 `*`, `+`, `{n,m}`）后，表示非贪婪匹配。
- **示例**：
  ```javascript
  const str = "ct cat";
  const regex = /ca?t/g;
  console.log(str.match(regex)); // ['ct', 'cat']
  ```

#### **(5) `|`（或）**
- **功能**：匹配 `|` 左侧或右侧的模式。
- **示例**：
  ```javascript
  const str = "cat dog mouse";
  const regex = /cat|dog/g;
  console.log(str.match(regex)); // ['cat', 'dog']
  ```

#### **(6) `()`（括号）**
- **功能**：
  - 定义子表达式（分组），用于捕获匹配的内容。
  - 限定量词的作用范围。
- **示例**：
  ```javascript
  const str = "ababab";
  const regex = /(ab)+/g;
  console.log(str.match(regex)); // ['ababab']
  console.log(str.match(/(ab)/g)); // ['ab', 'ab', 'ab']（捕获组）
  ```

#### **(7) `[]`（方括号）**
- **功能**：定义字符集，匹配集合中的任意单个字符。
- **特殊用法**：
  - `[a-z]`: 匹配小写字母。
  - `[0-9]`: 匹配数字（等价于 `\d`）。
  - `[a-zA-Z0-9]`: 匹配字母或数字。
- **示例**：
  ```javascript
  const str = "cat dog";
  const regex = /[a-c]/g;
  console.log(str.match(regex)); // ['c', 'a', 'b']
  ```

#### **(8) `[^]`（否定字符集）**
- **功能**：匹配不在集合中的任意单个字符。
- **示例**：
  ```javascript
  const str = "cat";
  const regex = /[^a]/g;
  console.log(str.match(regex)); // ['c', 't']
  ```

#### **(9) `{n}`, `{n,}`, `{n,m}`**
- **功能**：
  - `{n}`: 匹配正好 n 次。
  - `{n,}`: 匹配至少 n 次。
  - `{n,m}`: 匹配 n 到 m 次。
- **示例**：
  ```javascript
  const str = "aa aaa aaaa";
  const regex = /a{2,3}/g;
  console.log(str.match(regex)); // ['aa', 'aaa', 'aaa']
  ```

#### **(10) `^`（开头）**
- **功能**：匹配字符串（或行的）开头。
- **示例**：
  ```javascript
  const str = "cat in hat";
  const regex = /^cat/;
  console.log(str.match(regex)); // ['cat']
  ```

#### **(11) `$`（结尾）**
- **功能**：匹配字符串（或行的）结尾。
- **示例**：
  ```javascript
  const str = "hat cat";
  const regex = /cat$/;
  console.log(str.match(regex)); // ['cat']
  ```

#### **(12) `\`（转义）**
- **功能**：
  - 转义元字符，使其表示字面字符（如 `\.` 匹配 `.`）。
  - 定义特殊序列（如 `\d`, `\w`）。
- **示例**：
  ```javascript
  const str = "3.14";
  const regex = /3\.14/;
  console.log(str.match(regex)); // ['3.14']
  ```

#### **(13) 特殊转义序列（与元字符相关）**
这些序列虽然以 `\` 开头，但它们本身也常被视为元字符的一部分：
- `\d`: 数字 `[0-9]`。
- `\D`: 非数字 `[^0-9]`。
- `\w`: 单词字符 `[a-zA-Z0-9_]`。
- `\W`: 非单词字符 `[^a-zA-Z0-9_]`。
- `\s`: 空白字符（空格、制表符、换行等）。
- `\S`: 非空白字符。
- `\b`: 单词边界。
- `\B`: 非单词边界。

**示例**：
```javascript
const str = "runoob123";
const regex = /\w+/g;
console.log(str.match(regex)); // ['runoob123']
```

---

### **4. 使用元字符时的注意事项**
1. **转义元字符**：
   - 要匹配字面元字符，必须加 `\`。例如，匹配 `*` 需要写 `\*`。
   ```javascript
   const str = "5 * 3";
   const regex = /\*/;
   console.log(str.match(regex)); // ['*']
   ```

2. **RegExp 构造函数中的双重转义**：
   - 在 `new RegExp()` 中，字符串需要额外的转义。例如，匹配 `\w` 需要写 `\\w`。
   ```javascript
   const regex = new RegExp("\\w+");
   console.log("runoob".match(regex)); // ['runoob']
   ```

3. **贪婪与非贪婪匹配**：
   - 元字符 `*`, `+`, `{n,m}` 默认是贪婪的，匹配尽可能多的字符。加 `?` 后变为非贪婪。
   ```javascript
   const str = "<p>text</p><p>more</p>";
   const regex = /<p>.*?</p>/g;
   console.log(str.match(regex)); // ['<p>text</p>', '<p>more</p>']
   ```

4. **多行模式（`m` 标志）**：
   - `^` 和 `$` 在 `m` 标志下匹配每行的开头和结尾。
   ```javascript
   const str = "cat\ndog";
   const regex = /^.*/mg;
   console.log(str.match(regex)); // ['cat', 'dog']
   ```

5. **Unicode 支持（`u` 标志）**：
   - 处理 Unicode 字符（如 emoji）时，使用 `u` 标志。
   ```javascript
   const str = "😊";
   const regex = /\uD83D\uDE0A/u;
   console.log(str.match(regex)); // ['😊']
   ```

---

### **5. 结合你的代码背景**
你之前提供的代码展示了转义规则对元字符 `\w` 的影响：
```javascript
var str = 'runoob';
var patt1 = new RegExp('\\w', 'g'); // 正确转义，匹配单词字符
var patt2 = new RegExp('\w', 'g');  // 错误，无效转义，匹配字面 'w'
var patt3 = /\w+/g;                // 字面量，直接使用 \w
```
- `patt1` 和 `patt3` 都使用了元字符 `\w`，正确匹配单词字符。
- `patt2` 因未正确转义，导致匹配字面字符 `w`，无法匹配 `"runoob"`。

这说明元字符（如 `\w`）在正则表达式中的正确使用至关重要，尤其是在 `RegExp` 构造函数中需要注意双重转义。

---

### **6. 总结**
- **元字符**是正则表达式的核心，用于定义复杂的匹配模式。
- 常见元字符包括 `.`, `*`, `+`, `?`, `|`, `()`, `[]`, `{}`, `^`, `$`, `\` 以及特殊序列（如 `\d`, `\w`）。
- 使用元字符时，注意转义规则（尤其在 `RegExp` 构造函数中）、贪婪/非贪婪匹配、以及标志（如 `g`, `i`, `m`, `s`, `u`）的影响。

如果你有具体的元字符问题（例如，如何使用某个元字符匹配特定模式），请提供更多细节，我可以为你提供更精确的示例或解答！