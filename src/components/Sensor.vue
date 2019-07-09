<template>
  <div class="sensor" :style="positionStyle" @click="activate">
    <span class="icon">{{icon}}</span>
    {{title}}
  </div>
</template>

<script>
import {eventBus} from "../main"

export default {
  name: "Sensor",
  props: {
    top: Number,
    left: Number,
    right: Number,
    title: String,
    icon: String,
    controllers: Array
  },
  methods: {
    activate() {
      eventBus.$emit("sensorActivated", {
        sensor: this.title,
        controllers: this.controllers
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
