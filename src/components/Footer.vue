<template>
  <div class="footer-block container-center">
    <div class="footer-block-content">
      <div class="footer-block-logo">
        <div class="footer-block-logo__img"/>
        <p>Donteco</p>
      </div>
      <div class="footer-block-contacts">
       <p>Москва  <a href="tel: +74953746795">8(495)374-67-95</a></p>
       <p>Ростов-на-Дону  <a href="tel: +78633200167">8(863)320-01-67</a></p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import "../helpers";

.footer-block {
  background-image: url(../assets/images/background_form_in_layout.jpg);
  background-position: center center;
  background-size: cover;
  color: #ffffff;
  &-logo {
    display: flex;
    align-items: center;
    font-size: 23px;
    font-family: "SSP";
    font-weight: 600;
  }
  .footer-block-logo__img {
    margin-right: 5px;
    width: 28px;
    height: 28px;
    background-position: center center;
    background-size: contain;
    background-repeat: no-repeat;
    background-image: url(../assets/images/logo.png);
  }
}

.footer-block-contacts {
  display: flex;
    a {
    color: #ffffff;
    font-family: "SSP";
    text-decoration: none;
    margin-left: 7px;
    }
  p {
    font-family: "SSP";
    margin-left: 50px;
    @include screen-max(450px) {
      margin-left: 0px;
    }
  }
  @include screen-sm {
     display: block;
  }
  @include screen-max(450px) {
    margin-top:30px;
  }
}

.footer-block-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 35px 0 60px 0;
  @include screen-lg {
     padding: 25px 0 40px 0;
  }
  @include screen-sm {
     padding: 20px 0 30px 0;
  }
  @include screen-xs {
     padding: 20px 10px 30px 10px;
  }
  @include screen-max(450px) {
      flex-direction: column;
      align-items: flex-start;
    }
}

</style>
