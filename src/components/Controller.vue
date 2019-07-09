<template>
  <div class="controller" :style="positionStyle" :class="activated && 'controller--activated'">
    <span class="icon">{{icon}}</span>
    {{title}}
  </div>
</template>

<script>
import { eventBus } from "../main";

export default {
  name: "Controller",
  data() {
    return {
      activated: false
    };
  },
  props: {
    top: Number,
    left: Number,
    right: Number,
    title: String,
    icon: String,
    activateWhenGreaterThan: Number,
    activateWhenLessThan: Number
  },
  computed: {
    positionStyle() {
      return `position: absolute; top: ${this.top}%; left: ${this.left}%; right: ${this.right}%;`;
    }
  },
  created() {
    eventBus.$on("sensorActivated", data => {
      if (data.controllers.includes(this.title)) {
        this.activated = true;
        setTimeout(() => {
          this.activated = false;
        }, 1000);
      }
    });
    eventBus.$on("rangeSensorChanged", data => {
      if (data.controllers.includes(this.title)) {
        if (
          data.value > this.activateWhenGreaterThan ||
          data.value < this.activateWhenLessThan
        ) {
          this.activated = true;
          setTimeout(() => {
            this.activated = false;
          }, 1000);
        }
      }
    });
  }
};
</script>

<style lang="scss" scoped>
.controller {
  background: #ccc;
  border: 2px solid #fff;
  border-radius: 16px;
  padding: 8px 16px;
  display: flex;
  align-items: center;
  
  &--activated {
    background: #ffaf38;
  }

  img {
    width: 20px;
    margin-right: 8px;
  }
}
</style>
