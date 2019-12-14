<template>
  <div id="simple_header">
    <h1 :style="`color: ${color}`">{{ title }}</h1>
    <button @click="changeColor">Change color</button>
  </div>
</template>

<script>
export default {
  name: "SimpleHeader",
  props: {
    title: {
      type: String,
      default: "Some default title",
    },
    color: {
      type: String,
      default: "#ff0000",
    },
  },
  methods: {
    changeColor() {
      let r = Math.floor(Math.random() * 255).toString(16),
          g = Math.floor(Math.random() * 255).toString(16),
          b = Math.floor(Math.random() * 255).toString(16);

      this.color = `#${r}${g}${b}`;
    },
  },
}
</script>

<style scoped>
#simple_header {
  background-color: green;
}
</style>
