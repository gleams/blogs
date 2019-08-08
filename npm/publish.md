## publish to npm

1. 需要一个npm 账号
2. 登录
    ```
        npm adduser
    ```
3. 输入用户名密码
4. 通过`npm init`生成初始`package.json`
    1. 如果想使用作用域`npm init --scope=@gleams -y`
    2. `package.json`中的`name`字段变为`@gleams/`
    
5. 在`package.json`需要注意`name`的规范，如果是想提交个人相关`@gleams/webpack-`方式命名，但这种会被认为是私有的。`npm publish --access public`
6. 配置`package.json`是非常重要的。
7. 常用配置[参考](http://javascript.ruanyifeng.com/nodejs/packagejson.html)，
其中`bin`字段，指定bin项用来指定各个内部命令对应的可执行文件的位置。所以在文件头部要指定运行环境`#!/usr/bin/env node`;
8. 最简单配置
```json
{
  "name": "@gleams/lwebpack-demo1",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "bin": {
    "jPack": "./bin/index.js"
  },
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "jPack"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    
  }
}

```
9. 删除已提的包`npm unpublic 包名`，如果报权限方面的错，加上`--force`