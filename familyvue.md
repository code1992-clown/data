# VUE

***

 ## VUE基础知识

1. 兼容性：Vue **不支持** IE8 及以下版本，但它支持所有[兼容 ECMAScript 5 的浏览器](https://caniuse.com/#feat=es5)。

   ***

   

2. 声明式渲染：{{ 文本插值 }}  所有东西都是**响应式的**；也可以通过v-bind来达到响应式的目的

   ***

   

3. 条件与循环：v-if  v-for

   ***

   

4. 处理用户输入：用 `v-on` 指令添加一个事件监听，用`v-model`实现数据的双向绑定

   ***

   

5. 组件化应用构建：允许我们使用小型、独立和通常可复用的组件构建大型应用，一个组件本质上是一个拥有预定义选项的一个 Vue 实例。组件有全局组件和局部组价之分，可以通过props传值，提取组件使项目更加简单

   ***

   

6. 与自定义元素的关系：Web Components 规范已经完成并通过，但未被所有浏览器原生实现，Vue 组件不需要任何 polyfill，并且在所有支持的浏览器 (IE9 及更高版本) 之下表现一致。必要时，Vue 组件也可以包装于原生自定义元素之内。Vue 组件提供了纯自定义元素所不具备的一些重要功能，最突出的是跨组件数据流、自定义事件通信以及构建工具集成。

   ***

   

7. ```vue
   <template>
     <div>
       <h1 :title="title">{{msg}}</h1>
       <h2 v-if="show" @click="show=!show">
         我是可以消失的
       </h2> 
       <div v-for="(item,index) in todos" :key="index" @click="reverser(index)">{{item.text}}</div>
       <button @click="todos.push({text:'打扫卫生'})">增加任务</button>
       <br>
        <p>{{ message }}</p>
     <input v-model="message">
     <br>
     <todoItem></todoItem>
     </div>
   </template>
   <script>
   export default {
     data(){
       return{
         message:"helsds",
         show:true,
         msg:"我是响应式的",
         title: '页面加载于 ' + new Date().toLocaleString(),
             todos: [
         { text: '学习 JavaScript' },
         { text: '学习 Vue' },
         { text: '整个牛项目' }
       ]
       }
     },
     methods:{
       reverser(index){
         this.todos[index].text=this.todos[index].text.split("").reverse().join("")
       }
     },
     watch:{
       show(){
         setTimeout(() => {
           this.show=true
         }, 2000);
       }
     }
   }
   </script>
   
   ```

8. 创建一个vue实例：new Vue({....})  ,虽然没有完全遵循 [MVVM 模型](https://zh.wikipedia.org/wiki/MVVM)，但是 Vue 的设计也受到了它的启发。

   ***

   

9. 数据与方法：当一个 Vue 实例被创建时，它将 `data` 对象中的所有的 property 加入到 Vue 的**响应式系统**中。当这些 property 的值发生改变时，视图将会产生“响应”，值得注意的是只有当实例被创建时就已经存在于 `data` 中的 property 才是**响应式**的。如果你知道你会在晚些时候需要一个 property，但是一开始它为空或不存在，那么你仅需要设置一些初始值；这里唯一的例外是使用 `Object.freeze()`，` Object.freeze(obj)   obj.name="sdsdfasfadfa"`这会阻止修改现有的 property，也意味着响应系统无法再*追踪*变化。 ` this.$watch('name', (newValue, oldValue)=> {})  this.$el  this.$data`

   $data中修改的数据，和平常方法修改数据，有什么不同？实验了一下，也是可以实现响应式的

   ***

   

10. 实例生命周期钩子：不要在选项 property 或回调上使用[箭头函数](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions)，比如 `created: () => console.log(this.a)` 或 `vm.$watch('a', newValue => this.myMethod())`。箭头函数并没有 `this`，`this`作为变量一直向上级词法作用域查找，直至找到为止，经常导致

    ![](C:\Users\Administrator\Desktop\lifecycle.png)

