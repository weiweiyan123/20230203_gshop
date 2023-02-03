<template>
  <div class="footer_guide">
    <span class="guide_item" :class="{on:'/msite'===$route.path}"  @click="go('/msite')">
      <span class="item_icon">
        <i class="iconfont icon-jiaoyupeixun"></i>
      </span>
      <span>外卖</span>
    </span>
    <span class="guide_item" :class="{on:'/search'===$route.path}"  @click="go('/search')">
      <span class="item_icon">
        <i class="iconfont icon-xiangce"></i>
      </span>
      <span>搜索</span>
    </span>
    <span class="guide_item" :class="{on:'/order'===$route.path}" @click="go('/order')">
      <span class="item_icon">
        <i class="iconfont icon-hetongguanli"></i>
      </span>
      <span>订单</span>
    </span>
    <span class="guide_item" :class="{on:'/profile'===$route.path}"  @click="go('/profile')">
      <span class="item_icon">
        <i class="iconfont icon-gangweiguanli"></i>
      </span>
      <span>我的</span>
    </span>
  </div>
</template>

<script>
  export default{
    data(){
      return{

      }
    },
    methods:{
      go(path){
        this.$router.push(path)
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import '../../common/stylus/mixins.styl'
  .footer_guide
    top-border-1px(red)
    position fixed
    z-index 100
    left 0
    right 0
    bottom 0
    background-color #fff
    width 100%
    height 50px
    display flex
    .guide_item
      display flex
      flex 1
      text-align center
      flex-direction column
      align-items center
      margin 5px
      color #999999
      &.on
        color #02a774
      span
        font-size 12px
        margin-top 2px
        margin-bottom 2px
        .iconfont
         font-size 22px
</style>
