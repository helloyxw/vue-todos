<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <ul class="todos">  
       <li v-for="(todo, index) in todos" :id="index" :class="{'checked': todo.done}">
           <label>{{ index + 1 }}.{{ todo.value }}</label>
       </li>
    </ul>
  </div>
</template>

<script>
import './assets/site.less';

export default {
  name: 'app',
  data () {
    return {
      title: "vue-todos",
      todos: [
          { value: "阅读一本关于前端开发的书", done: false },
          { value: "补充范例代码", done: true },
          { value: "写心得啦", done: false }
      ]
    }
  }
}
</script>

<style lang="less" scoped>
 @import './assets/todos.less';
</style>
