<template>
  <div>
    <h1>{{ counter }}</h1>
    <button @click.once="increaseCounter(2, $event)">Increase counter</button>
  </div>
</template>

<script>
// v-[directive]:[attribute].[modifier]

/*

.prevent - .preventDefault()
.stop    - .stopPropagation()
.once    - run the funciton at most once
.self    - only trigger if the target of the event is itself

*/

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
