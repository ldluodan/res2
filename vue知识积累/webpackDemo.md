#### WebPack总结

```
最好本地安装
```

```
第一步:初始化 npm init -y;初始化之后某些文件可能需要更新，需运行npm install 
-g npm去更新它；之后本地项目就会自动生成一个package.json
```

```
第二步: npm i -D webpack（安装webpack;此版本是4.0之前的版本；如需要4.0以上的
）；则需要npm i -D webpack-cli再次运行一下
```


```
第三步: 在安装完包之后；在webpackDeme里面再新建一个文件夹命名为dist
此文件夹就是指文件压缩之后放置里面的文件夹；再次在dist文件夹里面新建一个
index.html
```


```
第四步:在webpackDeme里面再新建一个文件夹命名为src;文件夹里面再创建有个
入口文件index.js
```
##### 以上步骤均为安装基本安装包和搭建好项目结构


```
第五步:安装lodash依赖和编写js文件；语句:npm i lodash -P;安装完之后package
.json会增加一个生产依赖dependencies
```


```
第六步:编写src/index.js文件
```


```
第七步：新建一个跟package.json同级的webpack.config.js;
```


```
第八步:通过npx webpack命令行语句已经打包出了一个在dist文件夹下面的main.js
在index.html里面导入main.js;再用浏览器打开；之前的打包出来的内容已经显示了
```
