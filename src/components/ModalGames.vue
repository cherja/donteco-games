<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="modal-container-yo">
        <iframe width="730" height="411" :src="ss" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
      <button class="modal-container__close" @click="$emit('close')">
        <img src="../assets/images/close.svg">
      </button>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  props: {
    ss: {
      type: String,
      required: true
    }
  }

}
</script>

<style lang="scss">

.modal-container-yo {
  position: relative;
  margin: 0px auto;
  padding: 20px 30px;
  transition: all .3s ease;
  font-family: Helvetica, Arial, sans-serif;
  img {
    width: 15px;
    height: 15px;
    margin: 7px;
  }
  &__close {
    right: 0;
    top:0;
    border: none;
    outline: none;
    background: none;
    position: absolute;
    padding: 5px 5px;
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
