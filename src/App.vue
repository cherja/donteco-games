<template>
  <div id="app" class="wrapper">
    <modal-component
      v-if="isShow"
      @close="isShow = false"
    />
    <header-component @open="isShow = true"/>
    <bomb-riders/>
    <death-race/>
    <laser-box/>
    <form-in-layout/>
    <company-address/>
    <footer-component/>
  </div>
</template>

<script>
import ModalComponent from './components/Modal.vue'
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
      isShow: false
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
</style>
