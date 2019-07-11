<template>
<div>
  <div class="recommend-title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <div class="item-img-wrapper">
        <img :src="item.imgUrl" alt="" class="item-img">
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
  name:'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl:'https://imgs.qunarzz.com/sight/source/1812/b4/e9d7f043c4fadf.jpg_r_640x214_713df0cf.jpg',
        title:'大连泡汤圣地',
        desc:'享受生活，放松自己，来一段轻松的旅程。',
      },
      {
        id: '0002',
        imgUrl:'https://imgs.qunarzz.com/sight/source/1505/7f/fa4eb0ca72409d.jpg_r_640x214_2f2a860e.jpg',
        title:'大连必打卡',
        desc:'爱上北方的碧海蓝天',
      },
      {
        id: '0003',
        imgUrl:'https://imgs.qunarzz.com/sight/source/1505/b7/8a08a1023062b3.jpg_r_640x214_d7cb475c.jpg',
        title:'最赞的海滨浴场',
        desc:'跳进海里，享受铺天盖地的清凉吧',
      },
      {
        id: '0004',
        imgUrl:'https://imgs.qunarzz.com/sight/source/1505/89/267342d404cbd7.jpg_r_640x214_8d8d1162.jpg',
        title:'亲子游乐',
        desc:'来生机勃勃的森林野生动物园留下你们珍贵的足迹，这里是儿童的天堂，大人最美好的回忆',
      },
      {
        id: '0005',
        imgUrl:'https://imgs.qunarzz.com/sight/source/1507/6b/70d17d828d87e1.jpg_r_640x214_6a995270.jpg',
        title:'周末游首选',
        desc:'泡温泉，戏冰雪，和宝贝尽情嗨玩整个冬日吧！抚顺给你和孩子一个不一样的冬日体验',
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
  .item-img-wrapper
    overflow:hidden
    height: 0
    padding-bottom:33.9%
  .item-img
    width: 100%;
  .item-info
    padding: .14rem .2rem .2rem .2rem
    text-align:left
    .item-title
      line-height:.54rem
      font-size:.28rem
      ellipsis()
    .item-desc
      font-size: .24rem
      line-height: .42rem
      color:#ccc
      ellipsis()
</style>
