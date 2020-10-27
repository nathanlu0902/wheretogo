<template>
  <div class='title'>您的位置
    <div class='currentCityWrapper'>
    <button class='currentCity'>北京</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'cityHeader'
}
</script>

<style>
.title {
  position: relative;
  background-color: lightblue;
  width: 100%;
  height: .44rem;
  line-height: .44rem;
  border: 1 solid;
}
.currentCity {
  position: absolute;
  border: 1px solid black;
  width: 33.3%;
  border-radius: 10%;
}
</style>