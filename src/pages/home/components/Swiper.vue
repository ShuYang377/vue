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
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1561551398&di=23805ac35bb0b5fa407acd6fa4f5f3e0&imgtype=jpg&er=1&src=http%3A%2F%2Fwww.ahstatic.com%2Fphotos%2F2117_de_00_p_2048x1536.jpg'
            },{
              id: '0002',
              imgUrl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1560956802598&di=3085340848f75fbfed7ac8704501ca41&imgtype=0&src=http%3A%2F%2Fs2.sinaimg.cn%2Fmw690%2F002FJYilzy7mFXNBZRvb1%26690'
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