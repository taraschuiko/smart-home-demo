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