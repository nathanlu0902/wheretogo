<template>
<div class="icons">
  <swiper :options="swiperOptions">
    <swiper-slide>
      <div class="icon" 
      v-for="item of iconList"
      :key="item.id">
        <div class='icon-image'>
            <img class='image-content' :src="item.url"/>
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
  data () {
    return {
      iconList: [{
        id: '0001',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: 'first'
      }, {
        id: '0002',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: 'first'
      }, {
        id: '0003',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: 'first'
      }]
    }
  }
}
</script>

<style scoped>
.icons {
  display: flex;
  display: -webkit-flex;
  height: 0;
  padding-bottom: 50%;
  flex-flow: row wrap;
  overflow: hidden;
  background-color: green;
}
div.icon {
  position: relative;
  width: 25%;
  height: 0;
  padding-bottom: 25%;
  box-sizing: border-box;
  overflow: hidden;
  background-color: blue;
}
div.icon-image {
  position: absolute;
  top: .2rem;
  bottom: .44rem;
  right: 0;
  left: 0;
  overflow: hidden;
}
img.image-content {
  position: block;
  margin: 0 atuo;
  height: 80%;
}
p.icon-desc {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  line-height: .44rem;
  height: .44rem;
  text-align: center;
}
</style>
