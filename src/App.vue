<template>
  <div>
    <h1 v-once>{{ title }}</h1>
    <p>
      {{ getTitle() }}
    </p>
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      title: "Some title",
      url: "https://google.com",
    }
  },
  methods: {
    getTitle() {
      this.title = "Some other title";

      return this.title;
    },
  },
}
</script>
