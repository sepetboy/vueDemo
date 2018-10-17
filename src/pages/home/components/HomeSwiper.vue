<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item in banners" :key="item.id">
        <img :src="item.imgUrl" class="swiper-image">
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
      banners: [{
        id: '0001',
        imgUrl: '//dimg08.c-ctrip.com/images/fd/tg/g1/M09/7B/AE/CghzfFWwurmAHTyRAAJpsgomXfI109_C_220_330.jpg'
      }, {
        id: '0002',
        imgUrl: '//dimg19.c-ctrip.com/images/fd/tg/g3/M00/6C/00/CggYGlYgmgKAJDqHABa1BmjqnRc404_C_220_330.jpg'
      }, {
        id: '0003',
        imgUrl: '//dimg09.c-ctrip.com/images/fd/tg/g1/M07/7A/98/CghzfVWwtayAcRE2ABaIuxjYffE235_C_220_330.jpg'
      }],
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 1500
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
