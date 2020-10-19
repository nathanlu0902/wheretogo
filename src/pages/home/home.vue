<template>
  <div>
    <homeheader></homeheader>
    <HomeSwiper></HomeSwiper>
    <icon></icon>
  </div>
</template>

<script>
import homeheader from './components/header'
import HomeSwiper from './components/swiper'
import icon from './components/icon'
export default {
  name: 'home', // 组件名
  components: {
    homeheader,
    HomeSwiper,
    icon
  }
}
</script>

<style>
</style>
