<template>
  <h1 :style="`color: ${color}`">{{ title }}</h1>
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
}
</script>
