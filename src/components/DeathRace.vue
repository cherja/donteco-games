<template>
  <div class="death-race-block games-blocks">
    <div class="container flex-for-block-games">
      <div class="games-text-btn_text-mobile">
        <h1>DEATH RACE</h1>
        <p>VR игра</p>
      </div>
      <div class="death-race games-img">
        <div class="play" @click="emitLink"/>
      </div>
      <div class="games-text-btn">
        <div class="games-text-btn_text">
          <h1>DEATH RACE</h1>
          <p>VR игра</p>
        </div>
        <div class="games-text-btn_btn">
          <!-- <p><button class="shop_btn"><img src="../assets/images/google_play.png" alt=""></button></p>
          <p><button class="shop_btn"><img src="../assets/images/app_store.png" alt=""></button></p> -->
          <p><button class="shop_btn"><img src="../assets/images/steam.png" alt=""></button></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    emitLink () {
      this.$emit('emit-link', 'https://www.youtube.com/embed/TnDGmCRCf7E?autoplay=1')
    }
  }
}
</script>

<style lang="scss">
@import "../helpers";
.death-race-block {
  color: #fe0f0f;
  background-image: url(../assets/images/background_death_race.jpg);
}
.death-race {
  background-image: url(../assets/images/death_race.png);
}
</style>
