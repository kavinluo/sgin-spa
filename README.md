# 基于 sing-spa的微前端

## 项目启动

 - 首先启动根目录下的服务

```sh
# First terminal tab
cd root-html-file
npm install
npm run serve
```
- 其次启动各个微服务

```sh
# Second terminal tab
cd app1
npm install
npm run serve
```

```sh
# Third terminal tab
cd app2
npm install
npm run serve
```

```sh
# Fourth terminal tab
cd navbar
npm install
npm run serve
```

## 关于打包部署

只要在各个APP各自打包
然后 创建文件夹将打好的包复制到文件夹里各自分开


```sh
- cd navbar && npm ci && npm run build && rm dist/index.html
- cd ../app1 && npm ci && npm run build && rm dist/index.html
- cd ../app2 && npm ci && npm run build && rm dist/index.html
- cd ..
- mkdir -p static/navbar static/app1 static/app2 && cp -a navbar/dist/* static/navbar && cp -a app1/dist/* static/app1 && cp -a app2/dist/* static/app2 // 批量创建各个APP文件夹将打好的包复制到文件夹中
- cp root-html-file/index.html static
- echo "Files that will be deployed"
- find static
- sed -i 's/http:\/\/localhost:8080/\/navbar\/js/g' static/index.html
- sed -i 's/http:\/\/localhost:8081/\/app1\/js/g' static/index.html
- sed -i 's/http:\/\/localhost:8082/\/app2\/js/g' static/index.html
- cp static/index.html static/200.html
```




