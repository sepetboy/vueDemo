<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide>
        <img src="~images/swiper1.jpg" class="swiper-image">
      </swiper-slide>
      <swiper-slide>
        <img src="~images/swiper2.jpg" class="swiper-image">
      </swiper-slide>
      <swiper-slide>
        <img src="~images/swiper3.jpg" class="swiper-image">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  .wrapper /deep/ .swiper-pagination-bullet-active {
    background: red !important
  }
  .wrapper {
    position: absolute;
    top: 0.86rem;
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom: 31.25%;
    background: #ccc;
    .swiper-image {
      width: 100%;
      // 轮播图的pagination是距离图片高度的bottom相差10px，所以图片要设置高度，否则，pagination可能不显示
      height: 31.25vw;
    }
  }
</style>
