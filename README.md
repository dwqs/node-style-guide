## Nodejs Style Guide(by [felixge](https://github.com/felixge/node-style-guide))

### [格式](#格式)

* [2个空格缩进](#2个空格缩进)
* [换行](#换行)
* [清除尾随空格](#清除尾随空格)
* [使用分号](#使用分号)
* [每行限制 80 个字符](#每行限制80个字符)
* [使用单引号](#使用单引号)
* [在同一行书写左大括号](#在同-行书写左大括号)
* [每个 var 语句只声明一个变量](#每个var语句只声明一个变量)


### [命名约定](#命名约定)

* [使用小驼峰式命名法对变量、属性和函数名命名](#使用小驼峰式命名法对变量、属性和函数名命名)
* [使用大驼峰式命名法对类名命名](#使用大驼峰式命名法对类名命名)
* [使用大写字母对常量命名](#使用大写字母对常量命名)

### [变量](#变量)

* [创建对象/数组](#创建对象/数组)

### [条件](#条件)

* [使用 === 操作符](#使用===操作符)
* [三目运算符使用多行形式](#三目运算符使用多行形式)
* [使用可描述的条件](#使用可描述的条件)

## <a name="格式">格式</a>

可以使用 [.editorconfig](http://editorconfig.org/) 配置文件来强制编辑器的格式配置. 推荐使用 Node.js Style Guide 提供的 [.editorconfig](https://github.com/felixge/node-style-guide/blob/master/.editorconfig) 文件来自动设置编辑器的缩进、换行和空格行为, 使其符合下面的规则.

### <a name="2个空格缩进">2个空格缩进</a>

使用 2 个空格来缩进代码, 并谨记不要将 Tabs 和空格混淆--否则会陷入另一个地狱.

### <a name="换行">换行</a>

使用 Unix 风格的换行(`\n`), 并将一个换行符作为文件的最后一个字符. 任何一个仓库都应该禁止 Windows 风格的换行(`\r\n`).

### <a name="清除尾随空格">清除尾随空格</a>

就和每次吃饭之后要刷牙一样, 在每次提交之前应该清除 JavaScript 文件中的尾随空格.

### <a name="使用分号">使用分号</a>

根据 [科学研究](http://news.ycombinator.com/item?id=1547647), 分号的使用是我们社区的核心价值. 考虑到 [对立观点](http://blog.izs.me/post/2353458699/an-open-letter-to-javascript-leaders-regarding), 当谈到滥用纠错机制(abusing error correction mechanisms)时, 传统主义者会更乐于谈简单的语法.

### <a name="每行限制80个字符">每行限制 80 个字符</a>

每行限制 80 个字符. 近几年来, 虽然屏幕变得越来越大, 但是大脑没有. 你的编辑器也支持利用额外的空间来分屏吧？

### <a name="使用单引号">使用单引号</a>

除非在写 JSON, 否则应该优先考虑使用单引号:

正确示例:

```
var foo = 'bar';
```

错误示例:

```
var foo = "bar";
```

### <a name="在同一行书写左大括号">在同一行书写左大括号</a>

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

### <a name="每个var语句只声明一个变量">每个 var 语句只声明一个变量</a>

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

## <a name="命名约定">命名约定</a>

## <a name="变量">变量</a>

### <a name="创建对象/数组">创建对象/数组</a>

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

## <a name="条件">条件</a>

## License

[CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/)
