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
