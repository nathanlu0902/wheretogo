<template>
<div class="header">
    <div class='header-left'>
        <div class='iconfont back-icon'>&#xe743;</div>
    </div>
    <div class='header-input'>
      <span class='iconfont'>&#xe7b3;</span>
      输入城市景点
    </div>
    <div class='header-right'>{{this.city}}
      <span class='iconfont'>&#xe7b2;</span>
    </div>
</div>
</template>
<script>
export default {
  name: 'homeheader',// 组件名
  props: {
    city: String
  }
}
</script>

<style scoped>
  /*样式里引入样式需要加@*/
  .header{
    display: flex;
    background-color: #00bcd4;
    /*1rem=html font-size=50px*/
    line-height : .86rem;
    color: #fff;
  }

  .header-left {
    width: .64rem;
    float : left;
  }
  .back-icon {
    font-size: .4rem;
    text-align: center;
  }
  .header-input {
    flex:1;
    background: #fff;
    line-height: .64rem;
    height: .64rem;
    margin-left: .2rem;
    margin-top: .12rem;
    padding-left: .2rem;
    border-radius: .1rem;
    color: #ccc;
    text-align: left;
  }

  .header-right {
    width : 1.24rem;
    float : right;
    text-align: center;
  }
</style>
