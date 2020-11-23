<template>
  <div class="swiper-container" v-if="options" :class="[options.isDisableDrag ? 'swiper-no-swiping' : '']" :style="{height: options.height + 'px'}" ref="root">
    <div class="swiper-wrapper">
      <slot></slot>
    </div>
    <div class="swiper-pagination"></div>
    <div v-if="!options.hideNavButton" class="swiper-button-prev"></div>
    <div v-if="!options.hideNavButton" class="swiper-button-next"></div>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue'
import Swiper from '@/assets/js/swiper.min.js'
export default {
  props: {
    options: Object
  },
  setup (props) {
    const root = ref(null)
    const swiper = ref(null)
    onMounted(() => {
      console.log(props.options)
      swiper.value = new Swiper(root.value, props.options.swiperOptions ? props.options.swiperOptions : {})
      console.log(swiper.value.activeIndex)
    })
    console.log(swiper)
    return {
      root,
      swiper
    }
  }
}
</script>

<style scoped lang="scss">
@import url("../assets/css/swiper.min.css");
.swiper-container {
  --swiper-pagination-color: #000; /* 两种都可以 */
  --swiper-navigation-color: rgba(255, 255, 255, 0.5);
}
</style>
