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
  width: calc(100% - 8px * 2);
  background: #fff;
  padding: 8px;
  position: fixed;
  border-bottom: 1px solid #ccc;
  z-index: 999;

  h1 {
    padding: 0;
    margin: 0;
  }
}
</style>
