<template>
  <div class="laser-box-block games-blocks">
    <div class="container flex-for-block-games">
      <div class="games-text-btn_text-mobile">
        <h1>LASER-BOX</h1>
        <div class="medal">
          <img src="../assets/images/medal.png" alt="">
          <p>Топ-20 головоломок<br><span>Google play</span></p>
        </div>
      </div>
      <div class="laser-box games-img">
        <div class="play" @click="emitLink"/>
      </div>
      <div class="games-text-btn">
        <div class="games-text-btn_text">
            <h1>LASER-BOX</h1>
          <div class="medal">
            <img src="../assets/images/medal.png" alt="">
            <p>Топ-20 головоломок<br><span>Google play</span></p>
          </div>
        </div>
        <div class="games-text-btn_btn">
          <p><a href="https://play.google.com/store/apps/details?id=com.dmitrievea.LaserBox2"><button class="shop_btn"><img src="../assets/images/google_play.png" alt=""></button></a></p>
          <p><a href="https://itunes.apple.com/ru/app/laser-box-%D0%B3%D0%BE%D0%BB%D0%BE%D0%B2%D0%BE%D0%BB%D0%BE%D0%BC%D0%BA%D0%B0/id942388640?mt=8"><button class="shop_btn"><img src="../assets/images/app_store.png" alt=""></button></a></p>
          <!-- <p><button class="shop_btn"><img src="../assets/images/steam.png" alt=""></button></p> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    emitLink () {
      this.$emit('emit-link', 'https://www.youtube.com/embed/qNIwdQ8kVYo?autoplay=1')
    }
  }
}
</script>

<style lang="scss">
@import "../helpers";
.laser-box-block {
  span {
    font-weight: 900;
  }
  color: #ffffff;
  background-image: url(../assets/images/background_laser_box.jpg);
}
.laser-box {
  background-image: url(../assets/images/laser_box.png);
}
.medal {
  text-align: left;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 1vw;
  img {
    width: 4vw;
    margin-right: 20px;
    @include screen-md {
     width: 10vw;
    }
  }
}
</style>
