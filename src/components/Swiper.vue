<template>
  <div style="border: 1px solid red">
    <div class="recommendPage">
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide>
          <img class="swiper-img" src="../assets/img/wallpaper_1.jpg" alt="">
        </swiper-slide>
        <swiper-slide>
          <img class="swiper-img" src="../assets/img/wallpaper_2.jpg" alt="">
        </swiper-slide>
        <swiper-slide>
          <img class="swiper-img" src="../assets/img/wallpaper_3.jpg" alt="">
        </swiper-slide>
        <swiper-slide>
          <img class="swiper-img" src="../assets/img/wallpaper_4.jpg" alt="">
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
import 'swiper/dist/css/swiper.css'
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  name: 'Swiper',
  components: {
    swiper,
    swiperSlide
  },
  data () {
    return {
      swiperOption: {
        // 分页器
        pagination: {
          el: '.swiper-pagination',
          // type: 'progressbar', // 分页器形状
          // 点击分页器的指示器可以跳转到指定图片
          clickable: true
        },
        loop: true, // 循环切换
        autoHeight: true, // 设置为true时，wrapper和container会随着当前slide的高度而发生变化
        autoplay: {
          delay: 1000, // 自动循坏时间
          disableOnInteraction: false
        },
        // 滑动图片从开始位置到终止位置所需的时间，单位ms
        speed: 750,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  }
}
</script>

<style scoped>
.recommendPage .swiper-container {
  position: relative;
  width: 100%;
  height: 720px;
}
.recommendPage .swiper-container .swiper-slide {
  width: 100%;
  line-height: 720px;
  background: yellowgreen;
  color: #000;
  font-size: 16px;
  text-align: center;
}
.swiper-img {
  width: 1280px;
  height: 720px;
}
</style>
