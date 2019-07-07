<template>
  <div class="sensor" :style="positionStyle">
    <img :src="img" alt="Sensor">
    {{title}}
    <input type="range" v-model="value" @change="change"/>
    {{value}}
  </div>
</template>

<script>
import {eventBus} from "../main"

export default {
  name: "RangeSensor",
  data() {
    return {
      value: 0
    }
  },
  props: {
    top: Number,
    left: Number,
    right: Number,
    title: String,
    img: String,
    controllers: Array
  },
  methods: {
    change() {
      eventBus.$emit("rangeSensorChanged", {
        sensor: this.title,
        controllers: this.controllers,
        value: this.value
      })
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
  display: flex;
  align-items: center;

  img {
    width: 20px;
    margin-right: 8px;
  }

  input {
    margin: 0 8px;
  }
}
</style>
