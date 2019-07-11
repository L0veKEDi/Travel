<template>
<div>
  <div class="recommend-title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <img :src="item.imgUrl" alt="" class="item-img">
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name:'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_200x200_4ab5da75.jpg',
        title:'大连圣亚海洋世界',
        desc:'这里有会太空步的海象',
      },
      {
        id: '0002',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1807/7d/7d64de6b134d10eaa3.img.jpg_200x200_56997205.jpg',
        title:'老虎滩海洋公园',
        desc:'一场极地海洋动物们的盛大派对',
      },
      {
        id: '0003',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1903/89/8965f21723d9da86a3.water.jpg_200x200_90a1a827.jpg',
        title:'大连森林动物园',
        desc:'与可爱温顺的羊驼亲密接触',
      },
      {
        id: '0004',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1712/e0/e04c331341c935afa3.water.jpg_200x200_5e3c94ce.jpg',
        title:'东方威尼斯水城',
        desc:'以威尼斯为蓝本，在这里享受浪漫',
      },
      {
        id: '0005',
        imgUrl:'https://imgs.qunarzz.com/sight/p0/1409/02/f27c6e58008d1ac501e898f38c1cc780.jpg_200x200_45d633bc.jpg',
        title:'大连铭湖国际观光牧场',
        desc:'国内首创新型科技农业观光旅游项目',
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top:.2rem
    line-height:.8rem
    background:#eee
    text-indent:.2rem
    text-align:left
  .item
    overflow:hidden
    display:flex
    height: 1.9rem
    .item-img
      height: 1.7rem
      width: 1.7rem
      padding: .1rem
    .item-info
      flex:1
      padding: .1rem
      min-width:0
      text-align:left
      .item-title
        line-height:.54rem
        font-size:.32rem
        ellipsis()
      .item-desc
        line-height:.4rem
        color:#ccc
        ellipsis()
      .item-button
        line-height:.44rem
        margin-top:.16rem
        background:#ff9300
        padding:0 .2rem
        border-radius:.06rem
        color:#fff
</style>
