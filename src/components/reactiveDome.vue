<template>
  <section>{{ state }}</section>
</template>

<script>
import { reactive } from 'vue';

export default {
  name: 'reactiveDome',
  components: {},
  data () {
    return {
    };
  },
  setup() {
    // 创建一个响应式数据
    // 本质：将传入的数据包装成一个proxy对象
    // 必须是一个对象类型，否则不能响应式
    let state = reactive({
      state: 'jjjj'
    })
    return { state }
  }
}

</script>