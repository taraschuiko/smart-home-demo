<template>
  <div class="sensor" :style="positionStyle">
    <img :src="img" alt="Sensor">
    {{title}}
  </div>
</template>

<script>
export default {
  name: "Sensor",
  props: {
    top: Number,
    left: Number,
    title: String,
    img: String
  },
  computed: {
    positionStyle() {
      return `position: absolute; top: ${this.top}px; left: ${this.left}px`
    }
  }
}
</script>

<style lang="scss" scoped>
.sensor {
  background: #fff;
  border: 2px solid #ccc;
  border-radius: 16px;
  padding: 8px 16px;
  cursor: pointer;
  display: flex;
  align-items: center;

  &:hover {
    background: #ccc;
  }

  img {
    width: 20px;
    margin-right: 8px;
  }
}
</style>
