<template>
  <section>
    <div>
      ref:{{ state }}
    </div>
    <div>
      <button @click="btn">按钮</button>
    </div>
  </section>
</template>

<script>
import { ref, isRef } from 'vue';

export default {
  name: 'refDome',
  setup() {
    // 创建一个响应式数据
    // 简单值
    // ref本质还是一个reactive,ref函数底层自动将ref转换成reactive
    // ref(18) => reactive({value: 18})
    let state = ref(18)
    function btn() {
      console.log(state);
      state.value = 'hhhh'
      console.log(isRef(state));
    }
    return { state, btn }
  }
}

</script>