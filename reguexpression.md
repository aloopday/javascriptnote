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