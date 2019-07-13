<template>
<div>
<HomeHeader></HomeHeader>
<HomeSwiper :list="swiperList"></HomeSwiper>
<HomeIcons :list="iconList"></HomeIcons>
<HomeRecommend :list="recommendList"></HomeRecommend>
<HomeWeekend :list="weekendList"></HomeWeekend>
</div>
</template>

<script>
import HomeHeader from './components/header.vue'
import HomeSwiper from './components/swiper.vue'
import HomeIcons from './components/icons.vue'
import HomeRecommend from './components/recommend.vue'
import HomeWeekend from './components/weekend.vue'
import { mapState } from 'vuex'
import axios from 'axios'
export default{
  name: 'Home', 
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: [],
      lastCity: []
    }
  },
  computed: {
    ...mapState(['city'])
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json?city=' + this.city)
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data){
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.lastCity = this.city
    this.getHomeInfo()
  },
  activated () {
    if(this.lastCity!== this.city)
      this.lastCity = this.city
      this.getHomeInfo()
  }
  
}
</script>

<style>
</style>
