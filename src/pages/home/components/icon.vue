<template>
<div class="icons">
  <swiper :options="swiperOptions">
    <swiper-slide v-for="(page, index) of pages" :key="index">
      <div class="icon" 
      v-for="item of page"
      :key="item.id">
        <div class='icon-image'>
            <img class='image-content' :src='item.imgUrl'/>
        </div>
        <p class="icon-desc">{{item.desc}}</p>
      </div>
    </swiper-slide>
  </swiper>

</div>
</template>

<script>
export default {
  name: 'icon', // 组件名
  props: {
    iconlist: Array
  },
  data () {
    return {
      swiperOptions: {
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages=[]
      this.iconlist.forEach((item,index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
  }
  }
}

</script>

<style scoped> 
.icons {
  height: 0;
  padding-bottom: 50%;
}
.icon {
  position: relative;
  float: left;
  width: 25%;
  height: 0;
  padding-bottom: 25%;
}
.icon-image {
  position: absolute;
  box-sizing: border-box;
  top: .2rem;
  bottom: .44rem;
  right: 0;
  left: 0;
  padding: .1rem;
}
.image-content {
  display: block;
  margin: 0 auto;
  height: 100%;
}
.icon-desc {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  line-height: .44rem;
  height: .44rem;
  text-align: center;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>
