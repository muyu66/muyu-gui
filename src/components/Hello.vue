<template>
  <div class="hello">
    <swiper :options="swiperOption" style="height: auto">
      <!-- 幻灯内容 -->
      <swiper-slide>I'm Slide 1</swiper-slide>
      <swiper-slide>I'm Slide 2</swiper-slide>
      <swiper-slide>I'm Slide 3</swiper-slide>
      <swiper-slide>I'm Slide 4</swiper-slide>
      <swiper-slide>I'm Slide 5</swiper-slide>
      <swiper-slide>I'm Slide 6</swiper-slide>
      <swiper-slide>I'm Slide 7</swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'

export default {
  name: 'hello',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        direction: 'vertical',
        slidesPerView: 1,
        paginationClickable: true,
        spaceBetween: 30,
        mousewheelControl: true,
        autoHeight: true
      }
    }
  },
  components: {
      swiper,
      swiperSlide
  }
}
</script>

<style scoped>
    #hallo{
        height: 100%;
        width: 100%;
    }
</style>
