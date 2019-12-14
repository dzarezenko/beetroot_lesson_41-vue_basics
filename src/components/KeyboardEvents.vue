<template>
  <input type="text" @keyup.ctrl.c="forceAlert" />
</template>

<script>
export default {
  methods: {
    forceAlert(event) {
      console.log("Copied!");
      //alert("Button pressed");
    }
  }
}
</script>
