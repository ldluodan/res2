### vue获取数据vue-resource方法或者axios 
#### 第一种方法vue-resource：前提是在main.js
#### (import VueResource from 'vue-resource';Vue.use(VueResource);)


```
 getData(){
        //请求数据
        var api='http://www.phonegap100.com/appapi.php?a=getPortalList&catid=20&page=1';
        //第一种方法
        // this.$http.get(api).then((response)=>{
        //   console.log(response)
        //   //注意this指向
        //   this.list= response.body.result
        // },function(err){
        //   console.log(err)
        // });
      },
```
#### 第二种方法axios ：前提是在当前页面import Axios from 'axios';

```
getData(){
        //请求数据
        var api='http://www.phonegap100.com/appapi.php?a=getPortalList&catid=20&page=1';
    
        //第二种方法
        Axios.get(api).then((response)=>{
            this.list= response.data.result
        }).catch((error)=>{
            console.log(error)
        })
      },
```

