<template>
  <div class="home">
    <img src="../assets/smart-home.svg" alt="Smart Home" class="home__background" />
    <Sensor
      :top="80"
      :left="4"
      title="Door Sensor"
      :img="icons.doorSensor"
      :controllers="['Call Security', 'Notification']"
    />
    <Sensor
      :top="66"
      :left="40"
      title="Smoke Sensor"
      :img="icons.smokeSensor"
      :controllers="['Call Emergency', 'Notification']"
    />
    <Sensor
      :top="28"
      :left="8"
      title="CCTV Camera"
      :img="icons.cctvCamera"
      :controllers="['Call Security', 'Notification']"
    />
    <Sensor
      :top="58"
      :right="2"
      title="CCTV Camera"
      :img="icons.cctvCamera"
      :controllers="['Call Security', 'Notification']"
    />
    <Sensor
      :top="46"
      :left="68"
      title="Water Leak Sensor"
      :img="icons.waterLeakSensor"
      :controllers="['Turn Off Water', 'Notification']"
    />
    <Sensor
      :top="68"
      :left="68"
      title="Water Leak Sensor"
      :img="icons.waterLeakSensor"
      :controllers="['Turn Off Water', 'Notification']"
    />
    <Sensor
      :top="36"
      :left="40"
      title="Wake Up Sensor"
      :img="icons.wakeUpSensor"
      :controllers="['Turn On Music', 'Make Coffee']"
    />
    <RangeSensor
      :top="46"
      :left="10"
      title="Temperature"
      :img="icons.temperatureRangeSensor"
      :controllers="['Turn On Air Condition']"
    />
    <Controller :top="16" :left="20" title="Call Security" :img="icons.callSecurityController" />
    <Controller :top="16" :right="20" title="Call Emergency" :img="icons.callEmergencyController" />
    <Controller :top="86" :left="34" title="Notification" :img="icons.notificationController" />
    <Controller :top="86" :left="60" title="Turn Off Water" :img="icons.turnOffWaterController" />
    <Controller :top="56" :left="50" title="Turn On Music" :img="icons.turnOnMusicController" />
    <Controller :top="76" :left="48" title="Make Coffee" :img="icons.makeCoffeeController" />
    <Controller
      :top="70"
      :left="8"
      title="Turn On Air Condition"
      :img="icons.turnOnAirConditionController"
      :activateWhenGreaterThan="25"
    />
  </div>
</template>

<script>
import Sensor from "./Sensor";
import RangeSensor from "./RangeSensor";
import Controller from "./Controller";
import icons from "../assets/icons";

export default {
  name: "Home",
  components: {
    Sensor,
    RangeSensor,
    Controller
  },
  computed: {
    icons() {
      return icons;
    }
  }
};
</script>

<style lang="scss" scoped>
.home {
  position: relative;
  width: 100%;
  max-width: 960px;
  min-width: 720px;
  margin: 0 auto;
  padding: 100px 16px 16px 16px;

  &__background {
    width: 100%;
  }
}
</style>
