<template>
  <div class="home">
    <img src="../assets/smart-home.svg" alt="Smart Home" class="home__background" />
    <Sensor
      :top="80"
      :left="4"
      title="Door Sensor"
      :img="DoorSensorImage"
      :controllers="['Call Security', 'Notification']"
    />
    <Sensor
      :top="66"
      :left="40"
      title="Smoke Sensor"
      :img="SmokeSensorImage"
      :controllers="['Call Emergency', 'Notification']"
    />
    <Sensor
      :top="28"
      :left="8"
      title="CCTV Camera"
      :img="CCTVCameraImage"
      :controllers="['Call Security', 'Notification']"
    />
    <Sensor
      :top="58"
      :right="2"
      title="CCTV Camera"
      :img="CCTVCameraImage"
      :controllers="['Call Security', 'Notification']"
    />
    <Sensor
      :top="46"
      :left="68"
      title="Water Leak Sensor"
      :img="WaterLeakSensorImage"
      :controllers="['Turn Off Water', 'Notification']"
    />
    <Sensor
      :top="68"
      :left="68"
      title="Water Leak Sensor"
      :img="WaterLeakSensorImage"
      :controllers="['Turn Off Water', 'Notification']"
    />
    <Sensor
      :top="36"
      :left="40"
      title="Wake Up Sensor"
      :img="WakeUpSensorImage"
      :controllers="['Turn On Music', 'Make Coffee']"
    />
    <RangeSensor
      :top="46"
      :left="10"
      title="Temperature"
      :img="TemperatureRangeSensorImage"
      :controllers="['Turn On Air Condition']"
    />
    <Controller :top="16" :left="20" title="Call Security" :img="CallSecurityControllerImage" />
    <Controller :top="16" :right="20" title="Call Emergency" :img="CallEmergencyControllerImage" />
    <Controller :top="86" :left="34" title="Notification" :img="NotificationControllerImage" />
    <Controller :top="86" :left="60" title="Turn Off Water" :img="TurnOffWaterControllerImage" />
    <Controller :top="56" :left="52" title="Turn On Music" :img="TurnOnMusicControllerImage" />
    <Controller :top="76" :left="48" title="Make Coffee" :img="MakeCoffeeControllerImage" />
    <Controller
      :top="70"
      :left="8"
      title="Turn On Air Condition"
      :img="TurnOnAirConditionControllerImage"
      :activateWhenGreaterThan="25"
    />
  </div>
</template>

<script>
import Sensor from "./Sensor";
import RangeSensor from "./RangeSensor";
import Controller from "./Controller";
import SmokeSensorImage from "../assets/smoke-sensor.svg";
import DoorSensorImage from "../assets/door-sensor.svg";
import CCTVCameraImage from "../assets/cctv-camera.svg";
import WaterLeakSensorImage from "../assets/water-leak-sensor.svg";
import WakeUpSensorImage from "../assets/wake-up-sensor.svg";
import TemperatureRangeSensorImage from "../assets/temperature-range-sensor.svg";
import CallSecurityControllerImage from "../assets/call-security-controller.svg";
import CallEmergencyControllerImage from "../assets/call-emergency-controller.svg";
import NotificationControllerImage from "../assets/notification-controller.svg";
import TurnOffWaterControllerImage from "../assets/turn-off-water-controller.svg";
import TurnOnMusicControllerImage from "../assets/turn-on-music-controller.svg";
import MakeCoffeeControllerImage from "../assets/make-coffee-controller.svg";
import TurnOnAirConditionControllerImage from "../assets/turn-on-air-condition-controller.svg";

export default {
  name: "Home",
  components: {
    Sensor,
    RangeSensor,
    Controller
  },
  computed: {
    SmokeSensorImage() {
      return SmokeSensorImage;
    },
    DoorSensorImage() {
      return DoorSensorImage;
    },
    CCTVCameraImage() {
      return CCTVCameraImage;
    },
    WaterLeakSensorImage() {
      return WaterLeakSensorImage;
    },
    WakeUpSensorImage() {
      return WakeUpSensorImage;
    },
    TemperatureRangeSensorImage() {
      return TemperatureRangeSensorImage;
    },
    NotificationControllerImage() {
      return NotificationControllerImage;
    },
    CallSecurityControllerImage() {
      return CallSecurityControllerImage;
    },
    CallEmergencyControllerImage() {
      return CallEmergencyControllerImage;
    },
    TurnOffWaterControllerImage() {
      return TurnOffWaterControllerImage;
    },
    TurnOnMusicControllerImage() {
      return TurnOnMusicControllerImage;
    },
    MakeCoffeeControllerImage() {
      return MakeCoffeeControllerImage;
    },
    TurnOnAirConditionControllerImage() {
      return TurnOnAirConditionControllerImage;
    }
  }
};
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
