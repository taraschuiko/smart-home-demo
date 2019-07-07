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
      :top="70"
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
    <Controller :top="16" :left="20" title="Call Security" :img="CallSecurityControllerImage" />
    <Controller :top="16" :right="20" title="Call Emergency" :img="CallEmergencyControllerImage" />
    <Controller :top="86" :left="34" title="Notification" :img="NotificationControllerImage" />
    <Controller :top="86" :left="60" title="Turn Off Water" :img="TurnOffWaterControllerImage" />
  </div>
</template>

<script>
import Sensor from "./Sensor";
import Controller from "./Controller";
import SmokeSensorImage from "../assets/smoke-sensor.svg";
import DoorSensorImage from "../assets/door-sensor.svg";
import CCTVCameraImage from "../assets/cctv-camera.svg";
import WaterLeakSensorImage from "../assets/water-leak-sensor.svg";
import CallSecurityControllerImage from "../assets/call-security-controller.svg";
import CallEmergencyControllerImage from "../assets/call-emergency-controller.svg";
import NotificationControllerImage from "../assets/notification-controller.svg";
import TurnOffWaterControllerImage from "../assets/turn-off-water-controller.svg";

export default {
  name: "Home",
  components: {
    Sensor,
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
