<template>
  <div class="bomb-riders-block games-blocks">
    <button @click="addLink">Открыть</button>
    <div class="container flex-for-block-games">
      <div class="games-text-btn_text-mobile">
        <h1>BOMB RIDERS</h1>
        <p>мобильная игра</p>
      </div>
      <div class="bomb-riders games-img"/>
      <div class="games-text-btn">
        <div class="games-text-btn_text">
          <h1>BOMB RIDERS</h1>
          <p>мобильная игра</p>
        </div>
        <div class="games-text-btn_btn">
          <p><a href="https://play.google.com/store/apps/details?id=com.Donteco.bomberbest"><button class="shop_btn"><img src="../assets/images/google_play.png" alt=""></button></a></p>
          <!-- <p><button class="shop_btn"><img src="../assets/images/app_store.png" alt=""></button></p> -->
          <p><a href="https://store.steampowered.com/app/906950/Bomb_Riders/?beta=0"><button class="shop_btn"><img src="../assets/images/steam.png" alt=""></button></a></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    addLink () {
      this.$emit('emit-media', 'https://www.youtube.com/embed/8uN2bGC76HU')
    }
  }
}
</script>

<style lang="scss">
@import "../helpers";
.bomb-riders-block {
  color: white;
  background-image: url(../assets/images/background_bomb_riders.jpg);
}
.bomb-riders {
  background-image: url(../assets/images/bomb_riders.png);
}
</style>
