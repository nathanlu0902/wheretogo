<template>
<div>
<div class="rec">
  推荐景点
</div >
  <ul>
    <li class="item" v-for="(item, index) of reclist">
      <img class="img" :src="item.imgUrl" />
      <div class="info">
      <p class="name">{{item.name}}</p>
      <p class="desc">{{item.desc}}</p>
      <button class="btn">查看详情</button>
    </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'recommend',
  props: {
    reclist: Array
  }
}
</script>

<style scoped>
.rec {
  background-color: darkgray;
  line-height: .44rem;
  text-indent: .2rem;
}

.item {
  overflow: hidden;
  display: flex;
  height: 1.9rem;
}

.img {
  width: 1.7rem;
  height: 1.7rem;
  padding: .1rem;
}

.info {
  flex: 1;
  padding: .1rem;
  text-align: left;
}

.name {
  font-size: .32rem;
  line-height: .54rem;
}
.desc {
  font-size: .3rem;
  color: #cccccc;
}
.btn {
  border-radius: .06rem;
  margin-top: .2rem;
  font-size: .2rem;
  background: #ff9300;
  padding: .1rem;
  color: #ffffff;
}
</style>