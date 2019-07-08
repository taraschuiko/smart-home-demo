<template>
  <div class="home">
    <img src="../assets/smart-home.svg" alt="Smart Home" class="home__background" />
    <Sensor
      :top="80"
      :left="4"
      title="Door Sensor"
      icon="g"
      :controllers="['Call Security', 'Notification']"
    />
    <Sensor
      :top="66"
      :left="40"
      title="Smoke Sensor"
      icon="l"
      :controllers="['Call Emergency', 'Notification']"
    />
    <Sensor
      :top="28"
      :left="8"
      title="CCTV Camera"
      icon="e"
      :controllers="['Call Security', 'Notification']"
    />
    <Sensor
      :top="58"
      :right="2"
      title="CCTV Camera"
      icon="e"
      :controllers="['Call Security', 'Notification']"
    />
    <Sensor
      :top="46"
      :left="68"
      title="Water Leak Sensor"
      icon="b"
      :controllers="['Turn Off Water', 'Notification']"
    />
    <Sensor
      :top="68"
      :left="68"
      title="Water Leak Sensor"
      icon="b"
      :controllers="['Turn Off Water', 'Notification']"
    />
    <Sensor
      :top="36"
      :left="40"
      title="Wake Up Sensor"
      icon="c"
      :controllers="['Turn On Music', 'Make Coffee']"
    />
    <RangeSensor
      :top="46"
      :left="10"
      title="Temperature"
      icon="k"
      :controllers="['Turn On Air Condition']"
    />
    <Controller :top="16" :left="20" title="Call Security" icon="j" />
    <Controller :top="16" :right="20" title="Call Emergency" icon="h" />
    <Controller :top="86" :left="34" title="Notification" icon="d" />
    <Controller :top="86" :left="60" title="Turn Off Water" icon="m" />
    <Controller :top="56" :left="50" title="Turn On Music" icon="i" />
    <Controller :top="76" :left="48" title="Make Coffee" icon="f" />
    <Controller
      :top="70"
      :left="8"
      title="Turn On Air Condition"
      icon="a"
      :activateWhenGreaterThan="25"
    />
  </div>
</template>

<script>
import Sensor from "./Sensor";
import RangeSensor from "./RangeSensor";
import Controller from "./Controller";

export default {
  name: "Home",
  components: {
    Sensor,
    RangeSensor,
    Controller
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
  padding: 116px 16px 16px 16px;

  &__background {
    width: 100%;
  }
}
</style>
