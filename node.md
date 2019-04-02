# 1.vue
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