<template>
  <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide>
      <img class="swiper-img" src="https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20208/91d516ade2556cb2f64aae392e6b35ce.jpg_890x330_ba143e24.jpg">
    </swiper-slide>
    <swiper-slide>
      <img class="swiper-img" src="https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/b69773a6eb09369ab16343a1b7133315.JPEG_890x330_ae217c52.jpeg">
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {}
    }
  }
}
</script>

<style scoped>
  .swiper-img {
    width: 100%
  }
</style>
