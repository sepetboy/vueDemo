<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <a class="item-detail" href="#">查看详情</a>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'recommend',
  props: {
    recommendList: Array
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
  .item {
    overflow: hidden;
    height: 1.9rem;
    display: flex;
    .item-img {
      width: 1.7rem;
      height: 1.7rem;
      padding: .1rem;
    }
    .item-info {
      flex: 1;
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
      .item-detail {
        display: inline-block;
        margin-top: .1rem;
        line-height: .2rem;
        padding: .12rem;
        border-radius: .06rem;
        color: #fff;
        background: #a76825;
        font-size: .22rem;
      }
    }
  }
</style>
