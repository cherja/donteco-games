<template>
  <div id="app" class="wrapper">
    <modal-games
      v-if="isShowYouTube"
      @close="isShowYouTube = false"
      :link="linkYoutube"
    />
    <modal-component
      v-if="isShow"
      @close="isShow = false"
    />
    <header-component @open="isShow = true"/>
    <bomb-riders  @emit-link="openModalYoutube"/>
    <death-race @emit-link="openModalYoutube"/>
    <laser-box @emit-link="openModalYoutube"/>
    <form-in-layout/>
    <company-address/>
    <footer-component/>
  </div>
</template>

<script>
import ModalComponent from './components/Modal.vue'
import ModalGames from './components/ModalGames.vue'
import HeaderComponent from './components/Header.vue'
import BombRiders from './components/BombRiders.vue'
import DeathRace from './components/DeathRace.vue'
import LaserBox from './components/LaserBox.vue'
import FormInLayout from './components/FormInLayout.vue'
import CompanyAddress from './components/CompanyAddress.vue'
import FooterComponent from './components/Footer.vue'

export default {
  components: {
    ModalComponent,
    ModalGames,
    HeaderComponent,
    BombRiders,
    DeathRace,
    LaserBox,
    FormInLayout,
    CompanyAddress,
    FooterComponent
  },
  name: 'app',
  data () {
    return {
      isShow: false,
      isShowYouTube: false,
      linkYoutube: ''
    }
  },
  methods: {
    openModalYoutube (link) {
      this.linkYoutube = link
      this.isShowYouTube = true
    }
  }
}
</script>

<style lang="scss">
@import "./helpers";

@font-face {
  font-family: "BBB";
  src: url("./assets/fonts/bebasbeuebold.otf");
}

@font-face {
  font-family: "SSP";
  src: url("./assets/fonts/sourcesanspro.ttf");
}

@font-face {
  font-family: "BNB";
  src: url("./assets/fonts/bebasneuebook.ttf");
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
button {
  cursor: pointer;
}
input[type=submit] {
  cursor: pointer;
}

.wrapper {
  max-width: 2000px;
  margin: auto;
  overflow: hidden;
}

.container {
  max-width: 1700px;
  margin: auto;
  padding: 0 50px;
  @include screen-md {
    padding: 0 20px;
  }
}

.container-center {
  margin:auto;
  padding: 0 320px;

   @include screen-max(1600px) {
      padding: 0 200px;
    }

   @include screen-max(1400px) {
      padding: 0 100px;
    }

    @include screen-md {
     padding: 0 50px;
    }

    @include screen-xs {
    padding: 0px;
  }
}
.games-blocks {
  background-position: center center;
  background-size: cover;
  padding: 30px 0;
  h1 {
    font-family: "BBB";
    font-size: 5vw;
    line-height: 80%;
    @include screen-md {
      font-size: 7vw;
    }
    @include screen-md {
      font-size: 10vw;
    }
  }
  p {
    font-family: "SSP";
    font-size: 2vw;
     @include screen-md {
      font-size: 5vw;
    }
  }
}

.games-img {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 50vw;
  height: 45vw;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
  @include screen-md {
    margin: 30px auto;
    width: 80vw;
    height: 55vw;
  }
  @include screen-xs {
    width: 90vw;
    height: 65vw;
  }
}
.shop_btn {
  margin: .5vw 0;
  width: 9vw;
  border: none;
  background-color: transparent;
  outline:none;
  cursor: pointer;
  @include screen-md {
    width: 15vw;
  }
  @include screen-xs {
    width: 25vw;
  }
}

.shop_btn>img {
  width: 100%;
}
.flex-for-block-games {
  display: flex;
  align-items: center;
  @include screen-md {
    display: block;
  }
}
.games-text-btn {
  margin-left: 8%;
  @include screen-md {
    margin-left: 0%;
  }
}
.games-text-btn_text {
  margin-bottom: 2vw;
  @include screen-md {
    display: none;
  }
}
.games-text-btn_text-mobile {
  display: none;
  @include screen-md {
    display: block;
    text-align: center;
  }
}
.games-text-btn_btn {
  @include screen-md {
    display: flex;
    justify-content: space-around;
  }
}
.play {
  width: 11vw;
  height: 11vw;
  background-position: center center;
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(./assets/images/play.png);
  transition: all .2s;
  cursor: pointer;
  @include screen-md {
    width: 14vw;
    height: 14vw;
  }
}
.play:hover {
  transform: scale(1.1);
}
</style>
