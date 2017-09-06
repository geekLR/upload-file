# upload-file

> 使用element-ui的upload组件实现上传图片至七牛云

### 工程要求
1. vue2.4 + express4.14 + es6
2. node版本在`4.0`以上(建议使用 [nvm](https://github.com/creationix/nvm) 来管理node版本)
3. 代码风格检查 [standardjs](https://standardjs.com/readme-zhcn.html)

### 工程依赖
1. [qiniu](https://github.com/qiniu/nodejs-sdk)
2. [element-ui](https://github.com/ElemeFE/element)

### 安装依赖
```bash
npm install
```

### 启动工程
- 融合模式启动 
```bash
npm start
```
- nodemon模式启动
```bash
npm run nodemon
```

### 流程
1. 后端配置公钥、私钥和存储空间名
2. 后端构建上传上传策略用以生成uploadToken
3. 后端暴露api返回uploadToken
4. 前端上传文件前先调用后端api获取uploadToken
5. 前端成功上传图片，获取七牛返回的图片地址

### 七牛
1. [直传文件](https://developer.qiniu.com/kodo/api/1312/upload)
2. [上传凭证](https://developer.qiniu.com/kodo/manual/1208/upload-token)
3. [Node.js SDK](https://developer.qiniu.com/kodo/sdk/1289/nodejs#5)
