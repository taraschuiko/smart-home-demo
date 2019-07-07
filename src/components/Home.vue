<template>
  <div class="home">
    <img src="../assets/smart-home.svg" alt="Smart Home" class="home__background">
    <Sensor top="70" left="40" title="Smoke Sensor" :img="SmokeSensorImage"/>
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
  position: relative;
  max-width: 960px;
  min-width: 720px;
  margin: 0 auto;
  padding: 100px 10px 0 10px;
  
  &__background {
    width: 100%;
  }
}
</style>
