<template>
  <div>
    <h1>{{ counter }}</h1>
    <form action="http://google.com">
      <input type="submit" @mouseout="showAlert" @click.prevent="increaseCounter" value="Increase counter" />
    </form>
  </div>
</template>

<script>
// v-[directive]:[attribute].[modifier]

export default {
  name: "Counter",
  data() {
    return {
      counter: 0,
    }
  },
  methods: {
    increaseCounter(event) {
      console.log(event);

      this.counter++;
      console.log(`Button clicked! Counter is ${this.counter}`);
    },
    showAlert() {
      alert(`Counter: ${this.counter}`);
    },
  },
}
</script>
