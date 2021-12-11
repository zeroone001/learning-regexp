# learning-regexp

学习正则表达式

## 学习资料收集

* [JS正则表达式完整教程（略长）](https://juejin.cn/post/6844903487155732494)
* [freeCodeCamp 正则表达式](https://chinese.freecodecamp.org/learn/javascript-algorithms-and-data-structures/#regular-expressions)

## 用惰性匹配来查找字符

```js
let text = "<h1>Winter is coming</h1>";
let myRegex = /<.*?>/; // 修改这一行 加上? 就会匹配最少的情况
let result = text.match(myRegex); // 匹配 <h1>

```

## 检查全部或无

```js
let favWord = "favorite";
let favRegex = /favou?rite/; // 修改这一行
let result = favRegex.test(favWord);
```

## 正向先行断言和负向先行断言

```js
let sampleWord = "astronaut";
let pwRegex = /(?=\w{6})(?=\w*\d{2})/; // 修改这一行
let result = pwRegex.test(sampleWord);
```

## 使用捕获组搜索和替换

```js
let str = "one two three";
let fixRegex = /(\w+)\s(\w+)\s(\w+)/; // 修改这一行
let replaceText = "$3 $2 $1"; // 修改这一行
let result = str.replace(fixRegex, replaceText);
```

## 删除开头和结尾的空白

```js
let hello = "   Hello, World!  ";
let wsRegex = /^(\s*)|(\s*)$/g; // 修改这一行
let result = hello.replace(wsRegex, ''); // 修改这一行
```