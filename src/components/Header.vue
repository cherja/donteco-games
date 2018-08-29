<template>
  <div class="header-block">
    <div class="grib"/>
    <div class="wolf"/>
    <div class="header-btn-contacts">
      <div class="header__front__contacts-mobile">
        <p>Москва <a href="tel: +74953746795">8(495)374-67-95</a></p>
        <p>Ростов-на-Дону <a href="tel: +78633200167">8(863)320-01-67</a></p>
      </div>
      <button @click="$emit('open')">ЗАКАЗАТЬ ЗВОНОК</button>
    </div>
    <div class="header-logo-contacts_background">
    <div class="container">
      <div class="header-logo-contacts">
        <div class="header-logo">
          <img class="img" src="../assets/images/header__logo_text.jpg" alt="Логотип">
          <img class="img2" src="../assets/images/header__logo_text_mobile.png" alt="Логотип">
        </div>
        <div class="header__front__contacts">
          <p>Москва <a href="tel: +74953746795">8(495)374-67-95</a></p>
          <p>Ростов-на-Дону <a href="tel: +78633200167">8(863)320-01-67</a></p>
        </div>
      </div>
    </div>
    </div>
    <div class="header-background">
      <div class="container">
        <div class="header-text">
          <p><span>Разработка</span></p>
          <p><span>игр. Mobile.</span></p>
          <p><span>Steam. VR</span></p>
          <div class="horse"/>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import "../helpers";
.header-block {
  .header-btn-contacts {
    z-index: 100;
    position: absolute;
    bottom: 50px;
    right: 70px;
    @include screen-sm {
      left: 50px;
    }
    @include screen-sm {
      left: 20px;
    }
    .header__front__contacts-mobile {
      display: none;
      @include screen-sm {
        display: block;
            font-family: "SSP";
      p, a {
        font-size: 25px;
        color: #2e00a7;
        text-shadow: -1px 0 1px white, 0 -1px 1px white, 0 1px 1px white, 1px 0 1px white, 0 0 8px white, 0 0 8px white, 0 0 8px white, 2px 2px 3px black;
      }
      a {
        font-weight: 900;
        text-decoration: none;
      }
    }

    }
    button {
      letter-spacing: 2px;
      font-family: Geneva;
      font-size: 1.5vw;
      background-color: #2e00a7;
      color: #ffffff;
      border: none;
      border-radius: 3px;
      padding: 2px 10px;
      margin: 10px 0;
      @include screen-md {
        font-size: 21px;
      }
    }
  }
  .grib {
    background-image: url(../assets/images/grib.png);
    background-position: center center;
    background-size: contain;
    position: absolute;
    background-repeat: no-repeat;
    width: 12%;
    height: 200px;
    bottom: 150px;
    right: 20px;
     @include screen-sm {
     display: none;
    }
  }
  .wolf {
    background-image: url(../assets/images/wolf.png);
    background-position: center center;
    background-size: contain;
    position: absolute;
    background-repeat: no-repeat;
    width: 20%;
    height: 400px;
    bottom: 15px;
    left: 20px;
     @include screen-sm {
     display: none;
    }
  }
  .horse {
    background-image: url(../assets/images/horse.png);
    background-position: center center;
    background-size: contain;
    position: absolute;
    background-repeat: no-repeat;
    width: 22%;
    height: 300px;
    bottom: 0px;
    left: 40%;
    @include screen-max(1450px) {
      left: 45%;
      height: 280px;
      bottom: -30px;
    }
    @include screen-lg {
      left: 50%;
      height: 260px;
    }
    @include screen-md {
      left: 54%;
      bottom: -90px;
    }
    @include screen-sm {
      left: 34%;
      bottom: -250px;
      width: 210px;
      height: 260px;
    }
  }
  .header-text {
    padding: 110px 0 0 110px;
    position: relative;
     @include screen-sm {
      padding: 50px 0 0 50px;
    }
     @include screen-xs {
      padding: 50px 0 0 0;
    }
    p {
      margin-top: 20px;
    }
  }
  span {
    color: #ffffff;
    background-color: #2e00a7;
    font-size: 6vw;
    letter-spacing: 5px;
    padding-left: 10px;
     @include screen-sm {
      font-size: 45px;
    }
    @include screen-xs {
      font-size: 38px;
    }
  }
   p:nth-child(1)>span {
    padding-right: 50px;
  }
  p:nth-child(2)>span {
    padding-right: 60px;
    @include screen-xs {
      padding-right: 10px;
    }
  }
  p:nth-child(3)>span {
    padding-right: 10px;
  }
  position: relative;
}
.header-logo-contacts_background {
  @include screen-sm {
    background-color: #2e00a7;
  }
}
.header-logo {
  width: 16%;
  @include screen-sm {
    width: 21%;
  }
  @include screen-sm {
    width: 35%;
  }
}
.header-logo>.img {
  width: 100%;
  @include screen-sm {
    display: none;
  }
}
.header-logo>.img2 {
  display: none;
  @include screen-sm {
    display: block;
    width: 100%;
  }
}
.header-logo-contacts {
  margin-top: 20px;
  color: #2e00a7;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 110px;
  @include screen-max(1600px) {
    height: 90px;
  }
  @include screen-max(1300px) {
    margin-top: 10px;
    height: 70px;
    margin-top: 0px;
  }
}
.header-background {
  background-image: url(../assets/images/background_header.jpg);
  background-position: center center;
  background-size: cover;
  min-height: 600px;
  height: calc(100vh - 110px);
   @include screen-max(1600px) {
    height: calc(100vh - 90px);
  }
  @include screen-max(1300px) {
    height: calc(100vh - 70px);
  }
}

.header__front__contacts {
  font-family: "SSP";
  p, a {
    font-size: 1.5vw;
  }
  a {
    color: #2e00a7;
    font-weight: 900;
    text-decoration: none;
  }
  @include screen-sm {
    display: none;
  }
}
</style>
