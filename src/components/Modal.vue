<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="modal-container">
      <input v-model="name" type="text" placeholder="Имя">
      <input v-model="tel" type="tel" placeholder="Телефон">
      <input @click="submitForm" type = "submit" value = "Готов">
      <button class="modal-container__close" @click="$emit('close')">
        <img src="../assets/images/close.svg">
      </button>
      </div>
    </div>
  </transition>
</template>

<script>
import axios from 'axios'

export default {
  name: 'app',
  data () {
    return {
      name: '',
      tel: ''
    }
  },
  methods: {
    submitForm () {
      if (!this.name || !this.tel) {
        alert('Заполните все поля')
        return
      }
      axios.post('mailsender.php', {
        'Имя': this.name,
        'Телефон': this.tel
      })
        .then(() => alert('Благодарим за отправку обращения!'))
        .catch(console.warn)
      this.name = ''
      this.tel = ''
      this.$emit('close')
    }
  }
}
</script>

<style lang="scss">
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, .5);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: opacity .3s ease;
  padding: 0px 20px;
}

.modal-container {
  position: relative;
  width: 580px;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #2e00a7;;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
  transition: all .3s ease;
  font-family: Helvetica, Arial, sans-serif;

  input {
    border-radius: 10px;
  }

   input[type=submit] {
    border-radius: 10px;
   }

   input:first-child {
     margin-top: 30px;
   }

  img {
    width: 15px;
    height: 15px;
    margin: 7px;;
  }

  &__close, &__add {
    border: none;
    outline: none;
    background: none;
    position: absolute;
    padding: 5px 5px;
  }

  &__close {
    right: 0;
    top:0;
  }

  &__add {
    right: 0;
    bottom:0;
  }
}

.modal-enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
</style>
