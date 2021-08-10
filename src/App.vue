<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3.0 + Vite" />
  <combinationAPI />
  <reactiveDome />
  <refDemo />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import combinationAPI from './components/combinationAPI.vue'
import reactiveDome from './components/reactiveDome.vue'
import refDemo from './components/refDemo.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    combinationAPI,
    reactiveDome,
    refDemo
  }
}
</script>
