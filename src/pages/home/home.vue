<template>
  <div>
    <homeheader :city = "city"></homeheader>
    <HomeSwiper :list = "swiperlist"></HomeSwiper>
    <icon :iconlist = "iconlist"></icon>
    <recommend :reclist = "reclist"></recommend>
    <weekend :weekend = "weekend"></weekend>
  </div>
</template>

<script>
import homeheader from './components/header'
import HomeSwiper from './components/swiper'
import icon from './components/icon'
import recommend from './components/recommend'
import weekend from './components/weekend'
import axios from 'axios'

export default {
  name: 'home', // 组件名
  components: {
    homeheader,
    HomeSwiper,
    icon,
    recommend,
    weekend
  },
  data () {
    return {
      city: '',
      swiperlist: [],
      iconlist: [],
      reclist: [],
      weekend: []
    }
    
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res=res.data
      if (res.ret && res.data) {
        const data = res.data
        this.city = data.city
        this.swiperlist = data.swiperList
        this.iconlist = data.iconList
        this.reclist = data.recommendList
        this.weekend = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo ()
  }
}
</script>

<style>
</style>
