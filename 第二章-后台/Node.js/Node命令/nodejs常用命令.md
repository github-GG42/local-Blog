# nodejs常用命令

```shell
#查看node,npm版本
node -version
npm -version

#node 项目 初始化  node创建package.json
#快速初始化
npm init -yes 
#指引初始化[根据提示,自定义初始化]
npm init

#查看已经安装的模块
npm list

#查看模块详情
npm show xxx[某一模块名]

#安装模块
#安装模块信息不保存到项目中的package.json中
npm install xxx[某一模块名] 
#安装信息保存到项目中的package.json中
npm install --save xxx[某一模块名] 
#全局安装模块
npm install -global xxx[某一模块名]


#更新模块
#全部模块更新
npm update
#指定更新模块
npm update xxx[某一模块名]
#更新全局模块
npm update -global xxx[某一模块名]

#删除执行模块
npm uninstall xxx[某一模块名]
```

