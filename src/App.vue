<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div class="display-flex">
      <ComponentVue2 />
      <component-vue-3 />
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ComponentVue2 from './components/ComponentVue2.vue'
import ComponentVue3 from './components/ComponentVue3.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ComponentVue2,
    ComponentVue3,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.display-flex {
  display: flex;
  justify-content: space-evenly;
}
</style>
