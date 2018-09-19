<template>
  <div class="form-layout-block">
    <div class="container-center">
    <div class="form-layout-block__content">
    <div class="form-layout-block__text">
      <h3>Остались вопросы?<br>
      Хотите узнать стоимость
      Вашего проекта?
      </h3>
      <p>Оставьте сообщение и наши специалисты свяжуться с Вами в течении 15 минут.</p>
    </div>
    <div class="form">
      <input v-model="name" type="text" placeholder="Имя">
      <input v-model="tel" type="tel" placeholder="Телефон">
      <textarea v-model=" message" placeholder="Введите сообщение"></textarea>
      <input @click="submitForm" type = "submit" value = "Отправить">
    </div>
    </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'app',
  data () {
    return {
      name: '',
      tel: '',
      message: ''
    }
  },
  methods: {
    submitForm () {
      if (!this.name || !this.tel || !this.message) {
        alert('Заполните все поля')
        return
      }
      axios.post('mailsender.php', {
        'Имя': this.name,
        'Телефон': this.tel,
        'Сообщение': this.message
      })
        .then(() => alert('Благодарим за отправку обращения!'))
        .catch(console.warn)
      this.name = ''
      this.tel = ''
      this.message = ''
    }
  }
}
</script>

<style lang="scss">
@import "../helpers";
.form-layout-block {
  background-image: url(../assets/images/background_form_in_layout.jpg);
  background-position: center center;
  background-size: cover;
  color: white;
  font-family: "SSP";

  h3 {
    font-size: 40px;
     @include screen-max(1400px) {
      font-size: 30px;
    }
  }
  p {
    font-size: 25px;
    margin:20px 0;
     @include screen-max(1400px) {
      font-size: 20px;
    }
  }
}
.form-layout-block__content {
  display: flex;
  padding: 120px 0;
  justify-content: space-between;
   @include screen-max(1400px) {
      padding: 80px 0;
    }
    @include screen-md {
      display: block;
      max-width: 400px;
      margin: auto;
    }

    @include screen-xs {
      display: block;
      max-width: 320px;
      padding: 30px 0;
    }
}

.form-layout-block__text {
  max-width: 500px;
  margin-right: 50px;
  @include screen-md {
    margin-right: 0px
    }
}

.form {
  max-width: 510px;

  @include screen-max(1400px) {
      max-width: 400px
    }
}
input {
  width: 100%;
  height: 45px;
  margin-bottom: 30px;
  font-size: 25px;
  font-family: "SSP";
  padding-left: 10px;
  outline:none;
  border:none;
  @include screen-max(1400px) {
      font-size: 20px;
    }
  @include screen-lg {
      height: 38px;
    }
}

textarea {
  width: 100%;
  height: 260px;
  font-size: 25px;
  font-family: "SSP";
  padding-left: 10px;
   @include screen-max(1400px) {
      height: 200px;
      font-size: 20px;
    }
    @include screen-lg {
      height: 130px;
    }
}

 input[type=submit] {
   background: transparent;
   border: 1px solid white;
   color:white;
   margin-top: 30px;
   transition: all .2s;
 }

 input[type=submit]:hover {
 box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
 }
  input[type=submit]:active {
 box-shadow: none;
 }
</style>
