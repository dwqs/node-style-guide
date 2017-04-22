## Nodejs Style Guide(by [felixge](https://github.com/felixge/node-style-guide))

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


[格式](#%E6%A0%BC%E5%BC%8F)
  - [2个空格缩进](#2%E4%B8%AA%E7%A9%BA%E6%A0%BC%E7%BC%A9%E8%BF%9B)
  - [换行](#%E6%8D%A2%E8%A1%8C)
  - [清除尾随空格](#%E6%B8%85%E9%99%A4%E5%B0%BE%E9%9A%8F%E7%A9%BA%E6%A0%BC)
  - [使用分号](#%E4%BD%BF%E7%94%A8%E5%88%86%E5%8F%B7)
  - [每行限制 80 个字符](#%E6%AF%8F%E8%A1%8C%E9%99%90%E5%88%B6-80-%E4%B8%AA%E5%AD%97%E7%AC%A6)
  - [使用单引号](#%E4%BD%BF%E7%94%A8%E5%8D%95%E5%BC%95%E5%8F%B7)
  - [在同一行书写左大括号](#%E5%9C%A8%E5%90%8C%E4%B8%80%E8%A1%8C%E4%B9%A6%E5%86%99%E5%B7%A6%E5%A4%A7%E6%8B%AC%E5%8F%B7)
  - [每个 var 语句只声明一个变量](#%E6%AF%8F%E4%B8%AA-var-%E8%AF%AD%E5%8F%A5%E5%8F%AA%E5%A3%B0%E6%98%8E%E4%B8%80%E4%B8%AA%E5%8F%98%E9%87%8F)

[命名约定](#%E5%91%BD%E5%90%8D%E7%BA%A6%E5%AE%9A)
  - [使用小驼峰式命名法对变量、属性和函数名命名](#%E4%BD%BF%E7%94%A8%E5%B0%8F%E9%A9%BC%E5%B3%B0%E5%BC%8F%E5%91%BD%E5%90%8D%E6%B3%95%E5%AF%B9%E5%8F%98%E9%87%8F%E5%B1%9E%E6%80%A7%E5%92%8C%E5%87%BD%E6%95%B0%E5%90%8D%E5%91%BD%E5%90%8D)
  - [使用大驼峰式命名法对类名命名](#%E4%BD%BF%E7%94%A8%E5%A4%A7%E9%A9%BC%E5%B3%B0%E5%BC%8F%E5%91%BD%E5%90%8D%E6%B3%95%E5%AF%B9%E7%B1%BB%E5%90%8D%E5%91%BD%E5%90%8D)
  - [使用大写字母对常量命名](#%E4%BD%BF%E7%94%A8%E5%A4%A7%E5%86%99%E5%AD%97%E6%AF%8D%E5%AF%B9%E5%B8%B8%E9%87%8F%E5%91%BD%E5%90%8D)

[变量](#%E5%8F%98%E9%87%8F)
  - [创建对象/数组变量](#%E5%88%9B%E5%BB%BA%E5%AF%B9%E8%B1%A1%E6%95%B0%E7%BB%84%E5%8F%98%E9%87%8F)

[条件](#%E6%9D%A1%E4%BB%B6)
  - [使用 === 操作符](#%E4%BD%BF%E7%94%A8--%E6%93%8D%E4%BD%9C%E7%AC%A6)
  - [三目运算符使用多行形式](#%E4%B8%89%E7%9B%AE%E8%BF%90%E7%AE%97%E7%AC%A6%E4%BD%BF%E7%94%A8%E5%A4%9A%E8%A1%8C%E5%BD%A2%E5%BC%8F)
  - [使用描写性的的条件](#%E4%BD%BF%E7%94%A8%E6%8F%8F%E5%86%99%E6%80%A7%E7%9A%84%E7%9A%84%E6%9D%A1%E4%BB%B6)

[函数](#%E5%87%BD%E6%95%B0)
  - [编写简短函数](#%E7%BC%96%E5%86%99%E7%AE%80%E7%9F%AD%E5%87%BD%E6%95%B0)
  - [提前从函数返回](#%E6%8F%90%E5%89%8D%E4%BB%8E%E5%87%BD%E6%95%B0%E8%BF%94%E5%9B%9E)
  - [对闭包命名](#%E5%AF%B9%E9%97%AD%E5%8C%85%E5%91%BD%E5%90%8D)
  - [避免闭包嵌套](#%E9%81%BF%E5%85%8D%E9%97%AD%E5%8C%85%E5%B5%8C%E5%A5%97)
  - [方法的链式调用](#%E6%96%B9%E6%B3%95%E7%9A%84%E9%93%BE%E5%BC%8F%E8%B0%83%E7%94%A8)

[注释](#%E6%B3%A8%E9%87%8A)
  - [注释使用斜杠语法](#%E6%B3%A8%E9%87%8A%E4%BD%BF%E7%94%A8%E6%96%9C%E6%9D%A0%E8%AF%AD%E6%B3%95)

[其它杂项](#%E5%85%B6%E5%AE%83%E6%9D%82%E9%A1%B9)
  - [Object.freeze, Object.preventExtensions, Object.seal, with, eval](#objectfreeze-objectpreventextensions-objectseal-with-eval)
  - [将 Requires 语句放在上面](#%E5%B0%86-requires-%E8%AF%AD%E5%8F%A5%E6%94%BE%E5%9C%A8%E4%B8%8A%E9%9D%A2)
  - [Getters 和 setters](#getters-%E5%92%8C-setters)
  - [不去扩展内置对象的原型](#%E4%B8%8D%E5%8E%BB%E6%89%A9%E5%B1%95%E5%86%85%E7%BD%AE%E5%AF%B9%E8%B1%A1%E7%9A%84%E5%8E%9F%E5%9E%8B)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## 格式

可以使用 [.editorconfig](http://editorconfig.org/) 配置文件来强制编辑器的格式配置. 推荐使用 Node.js Style Guide 提供的 [.editorconfig](https://github.com/felixge/node-style-guide/blob/master/.editorconfig) 文件来自动设置编辑器的缩进、换行和空格行为, 使其符合下面的规则.

### 2个空格缩进

使用 2 个空格来缩进代码, 并谨记不要将 Tabs 和空格混淆--否则会陷入另一个地狱.

### 换行

使用 Unix 风格的换行(`\n`), 并将一个换行符作为文件的最后一个字符. 任何一个仓库都应该禁止 Windows 风格的换行(`\r\n`).

### 清除尾随空格

就和每次吃饭之后要刷牙一样, 在每次提交之前应该清除 JavaScript 文件中的尾随空格.

### 使用分号

根据 [科学研究](http://news.ycombinator.com/item?id=1547647), 分号的使用是我们社区的核心价值. 考虑到 [对立观点](http://blog.izs.me/post/2353458699/an-open-letter-to-javascript-leaders-regarding), 当谈到滥用纠错机制(abusing error correction mechanisms)时, 传统主义者会更乐于谈简单的语法.

### 每行限制 80 个字符

每行限制 80 个字符. 近几年来, 虽然屏幕变得越来越大, 但是大脑没有. 你的编辑器也支持利用额外的空间来分屏吧？

### 使用单引号

除非在写 JSON, 否则应该优先考虑使用单引号:

正确示例:

```
var foo = 'bar';
```

错误示例:

```
var foo = "bar";
```

### 在同一行书写左大括号

在同一行声明语句块的左大括号.

正确示例:

```
if (true) {
  console.log('winning');
}
```

错误示例:

```
if (true)
{
  console.log('losing');
}
```

另外推荐的是在条件语句前后都使用空格.

### 每个 var 语句只声明一个变量

每个 `var` 语句只声明一个变量, 这也让重编行号变得简单. 然而, 要忽略 [Crockford](http://javascript.crockford.com/code.html) 中提到的不推荐在函数内部声明变量, 记住要把变量生命在更容易理解的地方.

正确示例:

```
var keys   = ['foo', 'bar'];
var values = [23, 42];

var object = {};
while (keys.length) {
  var key = keys.pop();
  object[key] = values.pop();
}
```

错误示例:

```
var keys = ['foo', 'bar'],
    values = [23, 42],
    object = {},
    key;

while (keys.length) {
  key = keys.pop();
  object[key] = values.pop();
}
```

## 命名约定

### 使用小驼峰式命名法对变量、属性和函数名命名

变量、属性和函数名应该使用小驼峰式命名法, 并且名称是可描述的. 应该避免使用单字符变量和不通用的缩写.

正确示例:

```
var adminUser = db.query('SELECT * FROM users ...');
```

错误示例:

```
var admin_user = db.query('SELECT * FROM users ...');
```

### 使用大驼峰式命名法对类名命名

类名应该采用大驼峰式命名法.

正确示例:

```
function BankAccount() {
}
```

错误示例:

```
function bank_Account() {
}
```

### 使用大写字母对常量命名

常量可被声明为普通变量或类的静态属性, 并使用大写字母对其命名.

正确示例:

```
var SECOND = 1 * 1000;

function File() {
}
File.FULL_PERMISSIONS = 0777;
```

错误示例:

```
const SECOND = 1 * 1000;

function File() {
}
File.fullPermissions = 0777;
```

## 变量

### 创建对象/数组变量

使用尾随的逗号进行分隔, 并把简短的声明放在单行.

正确示例:

```
var a = ['hello', 'world'];
var b = {
  good: 'code',
  'is generally': 'pretty',
};
```

错误示例:

```
var a = [
  'hello', 'world'
];
var b = {"good": 'code'
        , is generally: 'pretty'
        };
```

## 条件

### 使用 === 操作符

编程并不是记住 [愚蠢的规则](https://developer.mozilla.org/en/JavaScript/Reference/Operators/Comparison_Operators). 使用 `===` 操作符, 它会达到预期结果.

正确示例:

```
var a = 0;
if (a !== '') {
  console.log('winning');
}
```

错误示例:

```
var a = 0;
if (a == '') {
  console.log('losing');
}
```

### 三目运算符使用多行形式

不推荐将三目运算符写在一行, 而应该将其分成多行.

正确示例:

```
var foo = (a === b)
  ? 1
  : 2;
```

错误示例:

```
var foo = (a === b) ? 1 : 2;
```

### 使用描写性的的条件

任何一个重要的条件判断都应该被重新赋值给一个描写性的变量或者函数.

正确示例:

```
var isValidPassword = password.length >= 4 && /^(?=.*\d).{4,}$/.test(password);

if (isValidPassword) {
  console.log('winning');
}
```

错误示例:

```
if (password.length >= 4 && /^(?=.*\d).{4,}$/.test(password)) {
  console.log('losing');
}
```

## 函数

### 编写简短函数

保持函数简短. 一个好的函数适合展现在一个幻灯片(slide)上, 这样如果在一个比较大房间中, 也便于最后一排的人阅读. 不要指望他们拥有完美的视觉, 每一个函数的代码应该限制在 15 行左右.

### 提前从函数返回

为了避免 `if` 语句过度嵌套, 应该提前将函数值返回.

正确示例:

```
function isPercentage(val) {
  if (val < 0) {
    return false;
  }

  if (val > 100) {
    return false;
  }

  return true;
}
```

错误示例:

```
function isPercentage(val) {
  if (val >= 0) {
    if (val < 100) {
      return true;
    } else {
      return false;
    }
  } else {
    return false;
  }
}
```

对这个示例, 可以选择编写更简短的函数:

```
function isPercentage(val) {
  var isInRange = (val >= 0 && val <= 100);
  return isInRange;
}
```

### 对闭包命名

给闭包随意命名一个名字, 表示很关心它们, 这样便于产生更好的堆栈跟踪、堆和 cpu 配置文件.

正确示例:

```
req.on('end', function onEnd() {
  console.log('winning');
});
```

错误示例:

```
req.on('end', function() {
  console.log('losing');
});
```

### 避免闭包嵌套

合理使用闭包, 避免闭包嵌套, 否则代码会难以阅读.

正确示例:

```
setTimeout(function() {
  client.connect(afterConnect);
}, 1000);

function afterConnect() {
  console.log('winning');
}
```

错误示例:

```
setTimeout(function() {
  client.connect(function() {
    console.log('losing');
  });
}, 1000);
```

### 方法的链式调用

如果有方法的链式调用, 每个方法应该占一行, 并使用缩进来表明它们同属一个调用链.

正确示例:

```
User
  .findOne({ name: 'foo' })
  .populate('bar')
  .exec(function(err, user) {
    return true;
  });
```

错误示例:

```
User
.findOne({ name: 'foo' })
.populate('bar')
.exec(function(err, user) {
  return true;
});

User.findOne({ name: 'foo' })
  .populate('bar')
  .exec(function(err, user) {
    return true;
  });

User.findOne({ name: 'foo' }).populate('bar')
.exec(function(err, user) {
  return true;
});

User.findOne({ name: 'foo' }).populate('bar')
  .exec(function(err, user) {
    return true;
  });
```

## 注释

### 注释使用斜杠语法

单行注释或者多行注释都应该使用斜杠语法. 尝试用注释来解释一些高层次机制(higher level mechanisms) 或者阐述代码中的难点. 不要使用注释来重申琐碎的事情.

正确示例:

```
// 'ID_SOMETHING=VALUE' -> ['ID_SOMETHING=VALUE', 'SOMETHING', 'VALUE']
var matches = item.match(/ID_([^\n]+)=([^\n]+)/));

// This function has a nasty side effect where a failure to increment a
// redis counter used for statistics will cause an exception. This needs
// to be fixed in a later iteration.
function loadUser(id, cb) {
  // ...
}

var isSessionValid = (session.expires < Date.now());
if (isSessionValid) {
  // ...
}
```

错误示例:

```
// Execute a regex
var matches = item.match(/ID_([^\n]+)=([^\n]+)/);

// Usage: loadUser(5, function() { ... })
function loadUser(id, cb) {
  // ...
}

// Check if the session is valid
var isSessionValid = (session.expires < Date.now());
// If the session is valid
if (isSessionValid) {
  // ...
}
```

## 其它杂项

### Object.freeze, Object.preventExtensions, Object.seal, with, eval

避免使用上述方法.

### 将 Requires 语句放在上面

在文件中将 Requires 语句放在上面, 这样能清楚地表明此文件的依赖关系. 这种做法除了提供一个概述帮助他人快速了解文件依赖和可能存在的内存影响之外, 也有利于他人判断在其它地方使用该文件时, 是否还需要他们选择一个 `package.json` 文件.

### Getters 和 setters

不推荐使用 setters, 对于那些试图使用你的软件来解决问题的人, 这会导致更多问题. 可以随意使用 getters, 这不受 [副作用](http://en.wikipedia.org/wiki/Side_effect_(computer_science)) 影响, 如给集合提供一个 `length` 属性.

### 不去扩展内置对象的原型

不要扩展 JavaScript 内置对象的原型, 免得给自己挖坑.

正确示例:

```
var a = [];
if (!a.length) {
  console.log('winning');
}
```

错误示例:

```
Array.prototype.empty = function() {
  return !this.length;
}

var a = [];
if (a.empty()) {
  console.log('losing');
}
```

## License

[CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/)
