<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in weekendList" :key="item.id">
        <div class="item-img-wrapper">
         <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'weekend',
  props: {
    weekendList: Array
  }
}
</script>

<style lang="scss" scoped>
  @import '~styles/mixins.scss';
  .title {
    width: 100%;
    background: #ccc;
    margin-top: .3rem;
    line-height: .6rem;
    text-indent: .3rem;
  }
  .item-img-wrapper {
    overflow: hidden;
    height: 0;
    padding-bottom: 33.9%;
    .item-img {
      width: 100%;
    }
  }
  .item-info {
    padding: .1rem;
    .item-title {
      line-height: .54rem;
      font-size: .32rem;
      @include ellipsis();
    }
    .item-desc {
      color: #ccc;
      line-height: .4rem;
      @include ellipsis();
    }
  }
</style>
