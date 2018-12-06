<template>
<div>
    <home-header></home-header>
    <home-icons :list="iconList"></home-icons>
    <home-swiper :list='swiperList'></home-swiper>
    <home-recommend :list="recommendList"></home-recommend>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeIcons from './components/Icons'
import HomeSwiper from './components/Swiper'
import HomeRecommend from './components/Recommend'
import axios from 'axios'
export default{
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend
  },
  data: function () {
    return {
      swiperList: [],
      iconList: [],
      recommendList: []
    }
  },
  methods: {
    getHomeInfo: function () {
      axios.get('/api/index.json').then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc: function (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
      }
      console.log(res)
    }
  },
  mounted: function () {
    this.getHomeInfo()
  }
}
</script>

<style>

</style>
