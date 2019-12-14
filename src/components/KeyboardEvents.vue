<template>
  <input type="text" @keyup.a_button="forceAlert" />
</template>

<script>
export default {
  methods: {
    forceAlert() {
      alert("Button pressed");
    }
  }
}
</script>
