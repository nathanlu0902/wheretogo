<template>
<div class="icons">
  <swiper :options="swiperOption">
    <swiper-slide v-for="(page, index) of pages" :key="index">
      <div class="icon" 
      v-for="item of page"
      :key="item.id">
        <div class='icon-image'>
            <img class='image-content' :src='item.url'/>
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
        desc: '2'
      }, {
        id: '0003',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: '3'
      }, {
        id: '0004',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: '4'
      }, {
        id: '0005',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: '5'
      }, {
        id: '0006',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: '6'
      }, {
        id: '0007',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: '7'
      }, {
        id: '0008',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: '8'
      }, {
        id: '0009',
        url: 'https://tse1-mm.cn.bing.net/th/id/OIP.uvHQgVHPPycsGwKWQFVDCAHaHN?w=225&h=220&c=7&o=5&pid=1.7',
        desc: '9'
      }]
    }
  },
    computed: {
      pages () {
        const pages=[]
        this.iconList.forEach((item,index) => {
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
