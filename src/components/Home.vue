<template>
  <div class="home">
    <img src="../assets/smart-home.svg" alt="Smart Home" class="home__background">
    <Sensor top="430" left="570" title="Smoke Sensor" :img="SmokeSensorImage"/>
  </div>
</template>

<script>
import Sensor from "./Sensor"
import SmokeSensorImage from "../assets/smoke-sensor.svg"

export default {
  name: "Home",
  components: {
    Sensor
  },
  computed: {
    SmokeSensorImage() {
      return SmokeSensorImage
    }
  }
}
</script>

<style lang="scss" scoped>
.home {
  height: 100%;
  width: 100%;
  position: relative;
  
  &__background {
    height: 720px;
    position: absolute;
    top: 0;
    left: 0;
  }
}
</style>
