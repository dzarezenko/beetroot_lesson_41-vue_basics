<template>
  <div>
    Name: <input v-model="name" />
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
}
</script>
