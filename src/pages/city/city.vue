<template>
  <div>
  <cityHeader></cityHeader>
  <cityHot></cityHot>
  <cityAlpha></cityAlpha>
  </div>  
</template>

<script>
import cityHeader from './components/header'
import cityHot from './components/hot'
import cityAlpha from './components/alpha'
import axios from 'axios'

export default {
  name: 'city',
  components: {
    cityHeader,
    cityHot,
    cityAlpha
  }
}
</script>

<style>
</style>