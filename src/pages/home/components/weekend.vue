<template>
<div>
<div class="rec">
  周末景点
</div >
  <ul>
    <li class="item" v-for="(item, index) of weekend">
      <div class='img-wrapper'>
        <img class="image" :src="item.imgUrl" />
      </div>
      <div class="info">
      <p class="name">{{item.name}}</p>
      <p class="desc">{{item.desc}}</p>
    </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'weekend',
  props: {
    weekend: Array
  }
}
</script>
  
<style scoped>
.rec {
  margin-top: .2rem;
  background-color: darkgray;
  line-height: .8rem;
  text-indent: .2rem;
}
.img-wrapper {
  overflow: hidden;
  padding-bottom: 33.9%;
  height: 0;
}
.image {
  width: 100%;
}
.info {
  padding: .1rem;
}
.name {
  font-size: .32rem;
  line-height: .54rem;
}
.desc {
  line-height: .4rem;
  font-size: .3rem;
  color: #cccccc;
}

</style>