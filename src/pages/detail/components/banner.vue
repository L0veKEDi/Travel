<template>
  <div>
     <div class="banner" @click="handleBannerClick">
      <img src="http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_350x240_4dd46cd0.jpg" alt="" class="banner-img">
      <div class="banner-info">
        <div class="banner-title">大连圣亚海洋世界(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe634;</span>36</div>
      </div>
    </div>
    <CommonGallary :imgs="imgs" v-show="showGallary" @close="handleGarllaryClose"></CommonGallary>
  </div>
</template>

<script>
  import CommonGallary from 'common/gallary/Gallary'
  export default {
    name: 'DetailBanner',
    components:{
      CommonGallary
    },
    data () {
      return {
        showGallary: false,
        imgs: ['http://img1.qunarzz.com/sight/p0/1709/9b/9b7be1ecb890dc47a3.img.png_r_800x800_55eb4825.png',
        'http://img1.qunarzz.com/sight/p0/1709/9a/9abf0a28659cc45da3.img.png_r_800x800_a02a244c.png']
      }
    },
    methods: {
      handleBannerClick () {
        this.showGallary = true
      },
      handleGarllaryClose () {
        this.showGallary = false
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .banner
    position: relative;
    overflow:hidden
    height: 0;
    padding-bottom: 55%;
    .banner-img
      width: 100%;
    .banner-info
      display:flex
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      line-height: .6rem;
      color: #fff;
      text-align: left;
      background-image: linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8));
      .banner-title
        flex:1
        font-size: .32rem;
        padding: 0 .2rem;
      .banner-number
        margin-top: .14rem;
        padding: 0 .4rem;
        height: .32rem;
        line-height: .32rem;
        border-radius: .2rem;
        background: rgba(0,0,0,8);
        font-size: .24erm;
</style>
