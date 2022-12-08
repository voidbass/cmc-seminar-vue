<template>
  <div class="vue2">
    <div>This is count: {{ count }}</div>
    <div>This is computedCount: {{ computedCount }}</div>
    <button v-on:click="increaseCount">Button 1</button>
    <button @click="count--">Button 2</button>
  </div>
</template>

<script>
export default {
  name: "ComponentVue2",
  data() {
    return {
      count: 0,
    };
  },
  computed: {
    computedCount() {
      return this.count * 20;
    },
  },
  watch: {
    count: {
      handler(value, oldValue) {
        console.log("new Value", value);
        console.log("old Value", oldValue);
      },
    },
  },
  methods: {
    increaseCount() {
      this.count = this.count + 1;
    },
    decreaseCount() {
      this.count = this.count - 1;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
</style>
