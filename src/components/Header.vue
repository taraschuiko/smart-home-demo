<template>
  <div class="header">
    <h1>Smart Home</h1>
  </div>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style lang="scss" scoped>
.header {
  background: #fff;
  padding: 8px;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  border-bottom: 1px solid #ccc;
  z-index: 100;

  h1 {
    padding: 0;
    margin: 0;
  }
}
</style>
