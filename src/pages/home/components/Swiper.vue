<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
           <swiper-slide v-for="item of swiperList" :key="item.id">
              <img class="swiper-img" :src="item.imgUrl"/>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
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
        imgUrl: 'https://img1.qunarzz.com/p/tts8/1808/4d/e46f736efea70e02.jpg_r_640x420x90_8d894152.jpg'
      },
      {
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/p/tts8/1706/19/ec33bf49c0e91c02.jpg_r_1280x840x90_237360a8.jpg'
      }]
    }
  }
}
</script>

<style lang='stylus' scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff
    .wrapper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 31.25%
        background-color: #ccc
        .swiper-img
            width: 100%
            height:31.25vw
</style>
