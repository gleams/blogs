1. [《如何学习Node.js》](https://i5ting.github.io/How-to-learn-node-correctly/)

2. `express`+ `TypeScript`
    1. 初始化项目`npm init`
    1. 安装`npm i express`
    1. 安装`npm i typescript ts-node-dev`
    1. 执行 `.\node_modules\.bin\tsc --init`
    1. 修改`package.json`
        ```json
        "scripts": {
                "test": "echo \"Error: no test specified\" && exit 1",
                "tsc": "tsc",
                "dev": "ts-node-dev --respawn --transpile-only ./index.ts",
                "prod": "tsc && supervisor ./build/app.js"
            }
        ```
3. [typeorm](https://typeorm.biunav.com/zh/#%E5%AE%89%E8%A3%85)