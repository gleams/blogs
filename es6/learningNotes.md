[promise小书](http://liubin.org/promises-book/)

1. 创建一个promise对象

```js
function getURL(URL){
    return new Promise(function(resolve,reject){
        var req = new XMLHttpRequest();
        req.open('GET',URL,true);
        req.onload = function(){
            if(req.status === 200){
                resolve(req.responseText);
            }else{
                reject(new Error(req.statusText));
            }
        };
        req.onerror=function(){
            reject(new Error(req.statusText));
        };
        req.send();
    })
}

var url = 'http://httpbin.org/get';
getURL(url).then((value)=>{
    console.log('----',value)
}).catch((error)=>{
    console.error(error)
})
```
