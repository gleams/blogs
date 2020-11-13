1. 数组去重排序
```js
  function unique(ar=[]) {
          if(/Array/.test(Object.prototype.toString.call(ar))){
              return [...new Set(ar)].sort((a,b)=>a>b?1:-1)      
          }
          throw new Error('参数类型错误')
          
      }
```

```js
  Object.getOwnPropertyNames();
```