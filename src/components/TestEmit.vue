<template>
  <div class="home">
    Test Emit props: {{ isFalseEmit }}
    <div>Test Emit inside: {{ isFalseInside }}</div>
    <button @click="changeBoolean">click to change</button>
  </div>
</template>

<script>
export default {
  name: "TestEmit",
  props: {
    isFalseEmit: {
      type: String,
    },
    handleEmit: {
      type: Function,
    },
  },
  data() {
    return {
      isFalseInside: false,
    };
  },
  watch: {
    isFalseEmit(val, oldVal) {
      console.log("change",val, oldVal)
    },
  },
  methods: {
    changeBoolean(e) {
      this.isFalseInside = !this.isFalseInside;
      this.$emit("handleEmit", !e.target.value);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped></style>
