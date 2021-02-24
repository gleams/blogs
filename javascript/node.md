1. `eval`执行代码字符串
1. 表达式与语句。
1. 使用()小括号，小括号中只能是表达式。
1. `eval`会返回小括号表达式的值。
1. `eval`会返回中括号[]的值。
1.  `eval` 不会返回{}的对象，只会返回值
```js
eval('alert(1)');

```
1. `eval`的返回值
```js
var a = eval('[1,2,3,4]');
 console.log(a) //[1,2,3,4];
```
```js
var a = eval('{name:"张三"}')
console.log(a)//输出张三 
```
```js
var a = eval('({name:"张三"})');
console.log(a);//输出{name:"张三"};
```