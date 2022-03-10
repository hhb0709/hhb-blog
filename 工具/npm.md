#### 查看安装的包
```
# 全局

npm list -g --depth 0

npm ls 插件名字 -g
npm ls nodemon -g

#本地
npm ls nodemon
```
#### 更新全局安装的包
``` bash
npm update -g eslint 
```

#### 删除包

##### 方法1
```
npm uninstall packageName@version


npm uninstall -g packageName@version


```

##### 方法2
从安装位置直接删除,全局包的安装位置在
**C:\Users\用户名\AppData\Roaming\npm\node_modules**
直接找到要删除的包名及命令文件

#### 修改全局依赖下载位置
```
npm config set prefix "D:\Program Files\npm_global_modules\node_modules
```
