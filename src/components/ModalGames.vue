<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="modal-mask-youtube" @click="$emit('close')">
        <div class="modal-container-youtube" @click="$emit('close')">
          <iframe :src="link" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  props: {
    link: {
      type: String,
      required: true
    }
  }

}
</script>

<style lang="scss">
@import "../helpers";
.modal-mask-youtube {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
}

.modal-container-youtube {
  position: relative;
  height: 56.25vw;
  width: 100vw;
  iframe {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    margin: auto;
    width: 50%;
    height: 50%;
    @include screen-md {
      width: 80%;
      height: 80%;
    }
    @include screen-xs {
      width: 100%;
      height: 100%;
    }
  }
}
.modal-enter {
  opacity: 0;
}
.modal-leave-active {
  opacity: 0;
}
</style>
