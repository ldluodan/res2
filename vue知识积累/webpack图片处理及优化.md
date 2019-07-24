

```
第一步:npm install  --save-dev file-loader
```


```
第二步：在webpack.config.js加入 {
+         test: /\.(png|svg|jpg|gif)$/,
+         use: [
+           'file-loader'
+         ]
+       }
```


```
第三步:此时运行打包,发现dist目录下面多一个打包之后的图片
```

##### 图片还可以进行再次优化


```
第一步:npm install  image-webpack-loader --save-dev
```
##### 当图片有些打包之后的 还可以再通过base64编码把图片比较小的压缩成base64编码限制是小于1000即10kb


```
url-loader功能类似于 file-loader，可以把 url 地址对应的文件，打包成 base64
的 DataURL，提高访问的效率。
```


```
npm install --save-dev url-loader
```

```
{
    test: /\.(png|svg|jpg|gif|jpeg|ico|woff|woff2|eot|ttf|otf)$/,
    use: [
      {
        loader: 'url-loader', // 根据图片大小，把图片优化成base64
        options: {
          limit: 10000
        }
 },
```
