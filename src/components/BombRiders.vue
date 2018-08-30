<template>
  <div class="bomb-riders-block">
    <button class="google-play_btn"></button>
    <button class="app-store_btn"></button>
    <button class="steam_btn"></button>
    <div class="bomb-riders"/>
  </div>
</template>

<style lang="scss">
@import "../helpers";
.bomb-riders-block {
  background-image: url(../assets/images/background_bomb_riders.jpg);
  background-position: center center;
  background-size: cover;
  padding: 30px 0;
  .google-play_btn {
    width: 10vw;
    height: 50px;
    background-image: url(../assets/images/google_play.png);
    background-position: center center;
    background-size: contain;
    background-repeat: no-repeat;
    border: none;
    border-radius: 5px;
    background-color: transparent;
  }
  .app-store_btn {
    width: 200px;
    height: 50px;
    background-image: url(../assets/images/app_store.png);
    background-position: center center;
    background-size: contain;
    background-repeat: no-repeat;
    border: none;
    border-radius: 5px;
    background-color: transparent;
  }
  .steam_btn {
    width: 200px;
    height: 50px;
    background-image: url(../assets/images/steam.png);
    background-position: center center;
    background-size: contain;
    background-repeat: no-repeat;
    border: none;
    border-radius: 5px;
    background-color: transparent;
  }
}
.bomb-riders {
  width: 1110px;
  height: 900px;
  background-image: url(../assets/images/bomb_riders.png);
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
}
</style>
