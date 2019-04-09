<a href="#nomal">基础</a>
<a href="#CSS">CSS</a>
<a href="#es6">ES6</a>
<a href="#javascript">javascript</a>
<a href="#vue">vue</a>
<a href="#vuex">vuex</a>

<h1 id="nomal">基础</h1>

# 基础
```
    1.布局
      静态布局
      流式布局
      自适应布局
      弹性布局
      响应式布局
    2.盒模型
      标准盒模型：content+padding+border height和width是content区域
      ie盒模型：  content+padding+border height和width包含padding和border
```
<h1 id="CSS">CSS</h1>

```
    css3动画
```
<h1 id="javascript">javascript</h1>

### 1.js基础

```
  1.原生js ajax请求步骤
  function loadXMLDoc()
    {
      var xmlhttp;
      if (window.XMLHttpRequest)
      {
        //  IE7+, Firefox, Chrome, Opera, Safari 浏览器执行代码
        //1.创建ajax对象
        xmlhttp=new XMLHttpRequest();
      }
      else
      {
        // IE6, IE5 浏览器执行代码
        xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");
      }
      //3.设置响应HTTP状态变化的函数；
      xmlhttp.onreadystatechange=function()
      {
        if (xmlhttp.readyState==4 && xmlhttp.status==200)
        {
          //5.获取异步调用返回的数据； 
          document.getElementById("myDiv").innerHTML=xmlhttp.responseText;
        }
      }
      //2. 创建一个新的HTTP请求，并指定改HTTP请求的方法、URL以及验证信息； 
      xmlhttp.open("GET","/try/ajax/ajax_info.txt",true);
      //4.发送HTTP请求；
      xmlhttp.send();
    }
```
```
  2.post和get的区别
    请求方式：put，delete，post，get
    他们的作用分别是对服务器资源的增，删，改，查。 
    所以，get是获取数据，post是修改数据。
    GET请求只是简单的获取数据，POST请求会修改请求的资源
```
```
  3.localStorage和sessionStorage的区别
  localStorage生命周期是永久，这意味着除非用户显示在浏览器提供的UI上清除localStorage信息，否则这些信息将永远存在。 sessionStorage生命周期为当前窗口或标签页，一旦窗口或标签页被永久关闭了，那么所有通过sessionStorage存储的数据也就被清空了。
```
<h1 id="es6">ES6</h1>

```
  1.原型链
  首先明确： 函数（Function）才有prototype属性，对象（除Object）拥有__proto__。
  通过原型链来查找属性。
```
```
  2.Class类
  //创建Class类
  class Student {
            constructor(name) {
                this.name = name;
                this.color='red'
            }

            hello() {
                alert('Hello, ' + this.name + '!');
            }
        }
  //用Class类实现继承
  class PrimaryStudent extends Student {
      constructor(name, grade) {
          super(name); // 记得用super调用父类的构造方法!
          this.grade = grade;
      }

      myGrade() {
          alert('I am at grade ' + this.grade);
      }
  }
  let xiaoxiao=new PrimaryStudent('xiaoxiao','二年级')
  console.log(xiaoxiao)
```

<h1 id="vue">vue</h1>

```
    1.v-if和v-show的区别
      v-show和v-if的区别： v-show是css切换，v-if是完整的销毁和重新创建。
      使用 频繁切换时用v-show，运行时较少改变时用v-if
```
```
    2.绑定 class 的用法
      对象方法 v-bind:class="{'orange': isRipe, 'green': isNotRipe}"
      数组方法  v-bind:class="[class1, class2]"
```
```
    3.计算属性和 watch 的区别
      计算属性是自动监听依赖值的变化，从而动态返回内容，监听是一个过程，在监听的值变化时，可以触发一个回调，并做一些事情。
      所以区别来源于用法，只是需要动态值，那就用计算属性；需要知道值的改变后执行业务逻辑，才用 watch，用反或混用虽然可行，但都是不正确的用法。
      说出一下区别会加分
      computed 是一个对象时，它有哪些选项？
      computed 和 methods 有什么区别？
      computed 是否能依赖其它组件的数据？
      watch 是一个对象时，它有哪些选项？
      有get和set两个选项
      methods是一个方法，它可以接受参数，而computed不能，computed是可以缓存的，methods不会。
      computed可以依赖其他computed，甚至是其他组件的data
      watch 配置
        handler
        deep 是否深度
        immeditate 是否立即执行
      总结
      当有一些数据需要随着另外一些数据变化时，建议使用computed。
      当有一个通用的响应数据变化的时候，要执行一些业务逻辑或异步操作的时候建议使用watcher
```
```
    4.vue的生命周期
    beforeCreated 组件实例刚被创建
    created       组件实例创建完成，属性已绑定，但dom还未生成，el属性还不存在
    beforeMount   挂载实例之前
    mounted       挂载实例之后
    beforeUpdate  组件更新之前
    updated       组件更新之后
    beforeDestroy 销毁组件之前
    destroyed     销毁组件之后
```
<h1 id="vuex">vuex</h1>

```
    1.vuex是什么
    Vuex 是一个专为 Vue.js 应用程序开发的状态管理模式
    2.vuex的核心概念
    state   存储状态
    getter  获取状态
    mutation    修改状态
    action      也可以修改状态，action是通过提交mutation来修改状态
    module      如果store对象很庞大的化可以将 store 分割成多个模块，每个人模块都拥有自己的state，mutation，action，getter
```

   
