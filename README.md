# 系统学习React的笔记
### 一. react入门

1. **npx create-react-app**

   1.  npx 解决的问题：
      1. 不需要安装全局工具 npm -g XXX
      2. 先在本地(./node_modules/.bin/XXX)找npx后面的命令，找不到则下载最新版本执行命令，命令完成后自动删除。

   2. npx -p：允许指定安装包，并将其添加到**正在运行的$PATH中**，

      例如使用`npx -p node@6 npm run test`：（也可以事先使用nvm use v6.0）

      - npx会帮助你下载node@6
      - 将此时的环境变成node@6版本
      - 使用node@6帮你执行npm run test
      - 命令执行完毕之后不会修改你原来的node版本

   3. 与cnpm一起使用：切换npm的镜像源: npm config set registry [https://registry.npm.taobao.org](https://registry.npm.taobao.org/)

   



2. create-react-app 生成一个项目后，**npm run eject**暴露配置项，从package.json中可以找到config/webpack.config.js从而找到相关文件



3. **react与react-dom**
   1. 使用JSX时必须显示引入React，JSX => React.createElement(...)
   2. React负责逻辑控制，数据 -> vdom
   3. ReactDom负责渲染dom，vdom -> dom
   4. Babel-loader把JSX编译成相应的js对象，React.CreateElement把该js对象构造成React需要的vdom。

