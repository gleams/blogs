<!--
 * @Author: your name
 * @Date: 2021-02-18 14:31:49
 * @LastEditTime: 2021-02-20 10:22:39
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \blogs\node.md
-->

[whatwg](https://html.spec.whatwg.org/)

## 查看所有HTML元素
```js
Reflect.ownKeys(window).filter(
    (value)=>/^HTML.*/.test(value)?value:'')
```
## 查看HTML元素有的方法
```js
Reflect.ownKeys(window.HTMLElement.prototype)
```

## 查看元素方法
```js
function getEle(ele){
        if(ele=== 'img'){
            ele = 'image'
        }
        ele = ele.slice(0,1).toUpperCase() + ele.slice(1);
        var div = document.createElement(ele);
        var ele = Reflect.getPrototypeOf(window['HTML'+ele+'Element'].prototype);
        var eleAr = []
        for(o in ele){
            eleAr.push([{}.toString.call(div[o]).match(/ (.*)\]/)[1],o]);
        }
        return eleAr.sort()
    }
```

## 继承了Node接口

