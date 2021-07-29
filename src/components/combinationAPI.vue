<template>
  <h1>{{ count }}</h1>
  <button @click="myFn">按钮</button>
  <ul>
    <li v-for="(stu, index) in state.stus" :key="index">
      <span>{{ stu.name }}</span>
    </li>
  </ul>
</template>

<script>
import { ref } from 'vue';
// ref函数只能监听简单类型的变化
import { reactive } from 'vue';

export default {
  name: 'combinationAPI',
  props: {
    msg: String
  },
  data() {
    return {
      combinationAPI: '组合式API'
    }
  },
  setup() {
    // 定义名称为count的变量，初始值0，双向绑定
    let count = ref(0)
    function myFn() {
      this.count++
      console.log(count)
    }
    // 注意点：
    // 如果要在外界使用，需要return暴露给外界
    return { count, myFn }
  },
  setup() {
    // 定义名称为count的变量，初始值0，双向绑定
    let state = reactive({
      stus: [
        {id: 1, name: 'zs'},
        {id: 2, name: 'ls'},
      ]
    })
    // 注意点：
    // 如果要在外界使用，需要return暴露给外界
    return { state }
  }
}
</script>