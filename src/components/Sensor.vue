<template>
  <div class="sensor" :style="positionStyle" @click="activate">
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
    right: Number,
    title: String,
    img: String
  },
  methods: {
    activate() {
      alert("activated")
    }
  },
  computed: {
    positionStyle() {
      return `position: absolute; top: ${this.top}%; left: ${this.left}%; right: ${this.right}%;`
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
