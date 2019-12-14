<template>
  <ol v-if="data.length">
    <li v-for="(value, key) in data" :key="key">{{ value }}</li>
  </ol>
</template>

<script>
export default {
  props: {
    data: {
      type: Array,
      default: [],
    }
  },
}
</script>
