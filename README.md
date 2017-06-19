# Clearupthearea
一些环境的布置指令
#先安装node里面的包管理文件npm 
##使用npm安装less编译css文件,加载到webstorm
```
1. 在安装了node后,检查安安装是是否成功,使用node -v查看  再查看npm -v查看版本号
2. 在线全局安装less指令,在cmd中使用npm install less -g
3. 使用lessc -v查看是否成功
4. 在webstorm中点击设置,查找tools下的file watchers项,添加数据,指定program文件,为lessc文件的路径
```

## gulp使用

### 基本使用

```
1. 全局安装gulp
		npm install -g gulp
2. 局部安装gulp以及相关依赖
		npm install gulp --save-dev
3. 新建一个`gulpfile.js`,在内部引入gulp,在里面书写上我们要处理的文件
	var gulp = require('gulp')
4. 创建任务
		gulp.task('任务名',function(){
			console.log(‘runing task’);
		})
5. 在命令行中执行任务
		gulp 任务名
- 默认任务名
		gulp.task('default',function(){
 			console.log(‘runing task’);
		})
- 运行默认任务
		gulp 
```

## node中安装双版本的信息,使用nvm方法

```
1. 一些指令:nvm arch 查看或者设置平台类型
2. nvm install 按装node
3. nvm list 查看可用的node
4. nvm use 切换node版本
5. nvm version 查看nvm版本号
```

## 多版本安装放式

```
1. 卸载已有的node.js
2. 下载nvm
3. 创建目录c:\dev\nvm并解压进去
4. 配置nvm环境变量NVM_HOME=c:\dev\nvm
5. 配置nodejs环境变量NVM_SYMLINK=c:\dev\nodejs
6. path中添加%NVM_HOME%;5NVM_SYMLINK%
```

## nrm进行淘宝镜像

1. 先全局安装npm install nrm -g
3. 输入nrm ls查看信息
4. 转换到nrm use taobao镜像,以后使用nrm进行安装

## webpack中的配置

1. 先在全局中配置npm install webpack -g
2. 在项目中将npm 初始化 npm  init
3. 再配置项目中的webpack文件npm install webpack --save-dev
4. 使用过程中,我们可以进行简化处理,在package.json中的script对象中配置我们的简写,使用时,直接在cmd使用npm run 简写名称
5. 配置热刷新,需要安装全局的npm install webpack-dev-server -g
6. 在webpack2.0阶段,我们需要在测试文件中配置信息,entry对象中

### webpack中的常用加载器的介绍loader是webpack准备的一些处理工具

- 将我们的jsx和es6转换成es5 
