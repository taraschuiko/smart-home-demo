<template>
  <div class="home">
    <img src="../assets/smart-home.svg" alt="Smart Home" class="home__background">
    <Sensor :top="80" :left="4" title="Door Sensor" :img="DoorSensorImage"/>
    <Sensor :top="70" :left="40" title="Smoke Sensor" :img="SmokeSensorImage"/>
    <Sensor :top="28" :left="8" title="CCTV Camera" :img="CCTVCameraImage"/>
    <Sensor :top="58" :right="2" title="CCTV Camera" :img="CCTVCameraImage"/>
    <Sensor :top="46" :left="68" title="Water Leak Sensor" :img="WaterLeakSensorImage"/>
    <Sensor :top="68" :left="68" title="Water Leak Sensor" :img="WaterLeakSensorImage"/>
  </div>
</template>

<script>
import Sensor from "./Sensor"
import SmokeSensorImage from "../assets/smoke-sensor.svg"
import DoorSensorImage from "../assets/door-sensor.svg"
import CCTVCameraImage from "../assets/cctv-camera.svg"
import WaterLeakSensorImage from "../assets/water-leak-sensor.svg"

export default {
  name: "Home",
  components: {
    Sensor
  },
  computed: {
    SmokeSensorImage() {
      return SmokeSensorImage
    },
    DoorSensorImage() {
      return DoorSensorImage
    },
    CCTVCameraImage() {
      return CCTVCameraImage
    },
    WaterLeakSensorImage() {
      return WaterLeakSensorImage
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
