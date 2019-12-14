<template>
  <div>
    Name: <input v-bind:value="name" @keyup="changeName" />
    <h1>{{ name }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Dmytro",
    }
  },
  methods: {
    changeName(event) {
      //console.log(event);
      this.name = event.target.value;
    }
  }
}
</script>
