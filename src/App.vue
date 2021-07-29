<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3.0 + Vite" />
  <combinationAPI />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import combinationAPI from './components/combinationAPI.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    combinationAPI
  }
}
</script>
