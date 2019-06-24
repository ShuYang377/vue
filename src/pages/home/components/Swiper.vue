<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
        <swiper-slide v-for="item of swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl" />
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
    name :'HomeSwiper',
    data: function (){
        return {
            swiperOption:{
              pagination: '.swiper-pagination',
              loop:true
            },
            swiperList:[{
              id: '0001',
              imgUrl:'https://farm8.staticflickr.com/7146/6708815591_ef08beeab4.jpg'
            },{
              id: '0002',
              imgUrl:'https://farm3.staticflickr.com/2338/2203309828_e753de355f.jpg'
            }]
        }
    }
}
</script>

<style lang ="stylus" scoped> 
  ..wrapper >>> .swiper-pagination-bullet-active
    background: red !important 
  .wrapper 
    overflow:hidden
    width:100%
    height:0
    padding-bottom:31.25%
    backgrounf: #eee
  .swiper-img
    width:100%
</style>