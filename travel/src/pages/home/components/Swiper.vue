<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgURL" alt="">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgURL: 'static/img/1.png'
      }, {
        id: '0002',
        imgURL: 'static/img/2.png'
      }, {
        id: '0003',
        imgURL: 'static/img/3.png'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper>>>.swiper-pagination-bullet-active
    background white !important
 .wrapper
   overflow hidden
   width 100%
   height 0
   padding-bottom 25%
   background #eee
  .swiper-img
     width 100%
</style>
