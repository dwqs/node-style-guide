## Nodejs Style Guide(by [felixge](https://github.com/felixge/node-style-guide))

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [格式](#%E6%A0%BC%E5%BC%8F)
  - [2个空格缩进](#2%E4%B8%AA%E7%A9%BA%E6%A0%BC%E7%BC%A9%E8%BF%9B)
  - [换行](#%E6%8D%A2%E8%A1%8C)
  - [清除尾随空格](#%E6%B8%85%E9%99%A4%E5%B0%BE%E9%9A%8F%E7%A9%BA%E6%A0%BC)
  - [使用分号](#%E4%BD%BF%E7%94%A8%E5%88%86%E5%8F%B7)
  - [每行限制 80 个字符](#%E6%AF%8F%E8%A1%8C%E9%99%90%E5%88%B6-80-%E4%B8%AA%E5%AD%97%E7%AC%A6)
  - [使用单引号](#%E4%BD%BF%E7%94%A8%E5%8D%95%E5%BC%95%E5%8F%B7)
  - [在同一行书写左大括号](#%E5%9C%A8%E5%90%8C%E4%B8%80%E8%A1%8C%E4%B9%A6%E5%86%99%E5%B7%A6%E5%A4%A7%E6%8B%AC%E5%8F%B7)
  - [每个 var 语句只声明一个变量](#%E6%AF%8F%E4%B8%AA-var-%E8%AF%AD%E5%8F%A5%E5%8F%AA%E5%A3%B0%E6%98%8E%E4%B8%80%E4%B8%AA%E5%8F%98%E9%87%8F)
- [命名约定](#%E5%91%BD%E5%90%8D%E7%BA%A6%E5%AE%9A)
- [变量](#%E5%8F%98%E9%87%8F)
  - [创建对象/数组变量](#%E5%88%9B%E5%BB%BA%E5%AF%B9%E8%B1%A1%E6%95%B0%E7%BB%84%E5%8F%98%E9%87%8F)
- [条件](#%E6%9D%A1%E4%BB%B6)
- [License](#license)

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

## License

[CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/)
