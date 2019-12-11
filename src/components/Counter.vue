<template>
  <div>
    <h1>{{ counter }}</h1>
    <button @click="increaseCounter">Increase counter</button>
  </div>
</template>

<script>
export default {
  name: "Counter",
  data() {
    return {
      counter: 0,
    }
  },
  methods: {
    increaseCounter() {
      this.counter++;
      console.log(`Button clicked! Counter is ${this.counter}`);
    },
  },
}
</script>
