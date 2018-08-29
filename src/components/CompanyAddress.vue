<template>
  <div class="container-center">
    <div class="company-adres-block">
      <div class="company-adres-block__tex-rnd">
        <h2>РОСТОВ-НА-ДОНУ.<br>
        ГЛАВНЫЙ ОФИС И ЦЕНТР<br>
        РАЗРАБОТКИ
        </h2>
        <p><a href="tel: +78633200167">8(863)320-01-67</a><br>
        <a href="mailto:hello@donteco.com">hello@donteco.com</a>
        </p>
        <p>
        БЦ "Купеческий двор"<br>
        ул.Социалистическая, 74,<br>
        офис 915
        </p>
      </div>
      <div class="company-adres-block__tex-moscow">
        <h2>МОСКВА.<br>
        РАБОТА С КЛИЕНТАМИ
        </h2>
        <p><a href="tel: +74953746795">8(495)374-67-95</a><br>
        <a href="mailto:hello@donteco.com">hello@donteco.com</a>
        </p>
        <p>
        ул.Баумовская, 53, стр.1
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import "../helpers";

.company-adres-block {
  display: flex;
  justify-content: space-between;
  @include screen-xs {
    display: block;
  }
}

.company-adres-block__tex-rnd,
.company-adres-block__tex-moscow {
  margin: 110px 0;
  @include screen-xs {
    width: 320px;
    margin: 30px auto;
  }
  h2 {
    font-size: 40px;
    color: #004aca;
    height: 170px;
    font-family: "BNB";
    @include screen-max(1400px) {
      font-size: 35px;
    }
    @include screen-sm {
      font-size: 28px;
      height: 120px;
    }
    @include screen-xs {
      height: auto;
    }
  }
  a {
    text-decoration: none;
    color: #6280b5;
    @include screen-max(1400px) {
      font-size: 18px;
    }
    @include screen-sm {
      font-size: 15px;
    }
  }
  p {
    font-family: "SSP";
    margin: 10px 0;
    font-size: 23px;
    color: #6280b5;
    @include screen-max(1400px) {
      font-size: 18px;
    }
    @include screen-sm {
      font-size: 15px;
    }
  }
}
</style>
