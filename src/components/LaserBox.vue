<template>
  <div class="laser-box-block">
    <div class="laser-box"/>
  </div>
</template>

<style lang="scss">
@import "../helpers";
.laser-box-block {
  background-image: url(../assets/images/background_laser_box.jpg);
  background-position: center center;
  background-size: cover;
}
.laser-box {
  width: 1110px;
  height: 900px;
  background-image: url(../assets/images/laser_box.png);
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
}
</style>
