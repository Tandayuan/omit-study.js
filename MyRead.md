# 学习到的知识：
+ typescript 
    + 安装：`npm i -D typescript`
    + 初始化：`npx tsc --init`
+ babel
    + 安装babel兼容esMoudel方式(`import from`)在test文件夹的引入测试目标。默认jest只支持commonModule(`require 'xxx'`)的方式。
    + 安装babel和它的插件：`npm install --save-dev babel-jest @babel/core @babel/preset-env`
    + `babel.config.js`配置：
    ```javascript
    module.exports = {
        presets: [['@babel/preset-env', {targets: {node: 'current'}}]],
    };
    ```
+ jest: 单元测试 可以兼容typeScript
    + `npm i -D jest ts-jest @types/jest`安装jest支持ts的插件
    + `jest.config.js`: `preset: 'ts-jest'`配置jest支持ts的插件
+ np: 发布包到npm网站上
    + `npm login`
    + 发布前预检查：`npm run prepublishOnly`,预见通过：`npm publish`