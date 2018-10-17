<template>
  <ul class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) in pages" :key="index">
        <li v-for="item in page" :key="item.id">
          <img :src="item.imgUrl">
          <p>{{item.desc}}</p>
        </li>
      </swiper-slide>
    </swiper>
  </ul>
</template>

<script>
export default {
  name: 'icons',
  props: {
    iconList: Array
  },
  data () {
    return {
      swiperOption: {
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="scss" scoped>
  @import '~styles/mixins.scss';
  .icons {
    width: 100%;
    font-size: 0;
    li {
      display: inline-block;
      width: 25%;
      font-size: 12px;
      margin-top: .2rem;
      text-align: center;
      img {
        width: .80rem;
        height: .80rem;
      }
      p {
        margin-top: .2rem;
        @include ellipsis();
      }
    }
  }
</style>
