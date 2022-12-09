<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <div class="display-flex">
      <ComponentVue2 />
      <component-vue-3 />
      <div>
        Emit outside: {{ isFalseEmit }}
        <TestEmit @handleEmit="handleEmit" :isFalseEmit="isFalseEmit" />
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import ComponentVue2 from "./components/ComponentVue2.vue";
import ComponentVue3 from "./components/ComponentVue3.vue";
import TestEmit from "./components/TestEmit.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    ComponentVue2,
    ComponentVue3,
    TestEmit,
  },
  data() {
    return {
      isFalseEmit: false,
    };
  },
  methods: {
    handleEmit(emitProps) {
      this.isFalseEmit = emitProps;
    },
  },
};
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
