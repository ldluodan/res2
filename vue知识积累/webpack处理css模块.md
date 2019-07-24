#### webpack处理css模块

```
第一步:在src->style->index.css文件
```


```
第二步:在index.js里面添加import './style/index.css';//loader =>css loader
module, style loader
```


```
第三步:在终端新建命令行语句：npm i -D style-loader css-loader;
在webpack.congig.js里面添加
 module: {
    rules: [
      {
        test: /\.css$/,
        use: ['style-loader', 'css-loader']
      }
    ]
  }
```


```
第四步:打包npx webpack
```
