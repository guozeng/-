# nodejs调试之node-inspector

## node-inspector调试原理

node-inspector通过**websocket**与node调试端口（port=5858）通信

## 使用方法

npm安装：

`$ npm install -g node-inspector`

然后需要通过浏览器连接到node-inspector，需要启动inspector服务：

`$ node-inspector &`

node-inspector默认占用端口**8080**，可指定端口号启动服务：

`$ node-inspector --web-port=8088 &`

最后以debug模式运行node.js应用：

`$ node --debug app.js`

通过URL http://127.0.0.1:8080/?port=5858 就可以进行调试了
