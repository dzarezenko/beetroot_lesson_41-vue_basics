<template>
  <div>
    <h1>{{ counter }}</h1>
    <form action="http://google.com">
      <input type="submit" @click.prevent="increaseCounter(2, $event)" value="Increase counter" />
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
    increaseCounter(step, e) {
      console.log(e);

      this.counter+= step;
      console.log(`Button clicked! Counter is ${this.counter}`);
    },
    showAlert() {
      alert(`Counter: ${this.counter}`);
    },
  },
}
</script>
