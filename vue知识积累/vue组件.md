### VUE组件

#### 父组件主动获取子组件的数据和方法
```
1.调用子组件的时候的定义一个ref
<v-header ref="header"></v-header>
2.在父组件里通过this.$refs.header.属性 或者 this.$refs.header.方法
```
#### 子组件主动获取父组件的数据和方法

```
this.$parent.数据
this.$parent.方法
```

#### 非父子之间的传值

```
1.新建一个VueEvent.js文件 然后引用vue 然后实例化vue 最后暴露这个实例
import Vue from 'vue';

var VueEvent = new Vue()

export default VueEvent;

2.在要广播的地方引入刚才定义的实例
import VueEvent from '../model/VueEvent.js';

3.通过 VueEvent.$emit('名称','数据')

4.在接收数据的地方通过 $on接收
 VueEvent.$on('名称',function(){
     
 })
```
### VUE router的使用

```
1.安装npm install vue-router(main.js)

2.引入并Vue.use(VueRouter)

3.配置路由 
创建组件（引入组件）
    import Home from './components/Home.vue';
    import News from './components/News.vue';
    
4.定义路由（建议复制)
    const routes = [
        {path:'/home',component: Home},
        {path:'/news',component: News}
    ]
    
5.实例化vueRouter
    const router =new VueRouter({
        routes //(缩写) 相当于 routes：routes
    })
    
6.挂载
    new Vue({
        el: '#app',
        router,
        render: h => h(App)
    })

7.根组件的模板里放上这句话
<router-view></router-view>
```
