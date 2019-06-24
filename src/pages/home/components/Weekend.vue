<template>
    <div>
        <div class = "title">Weekend Options</div>
        <ul>
            <li class="item border-bottom" 
                v-for="(item,index) of recommendList" 
                :key="index">
                <div class="item-img-wrapper">
                <img class="item-img" v-bind:src='item.imgUrl'/>
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name:'HomeWeekend',
    data (){
        return {
            recommendList:[{
            id:'0001',
            imgUrl:'https://p0.meituan.net/deal/e1ae86ee3551b8b35d75ce4336cb1b4b65787.jpg%40450w_280h_1e_1c_1l%7Cwatermark%3D1%26%26r%3D1%26p%3D9%26x%3D2%26y%3D2%26relative%3D1%26o%3D20',
            title:'Painting on Canvas',
            desc:'This is a good hobby for teenage girls'
            },{
            id:'0002',
            imgUrl:'https://p0.meituan.net/deal/e1ae86ee3551b8b35d75ce4336cb1b4b65787.jpg%40450w_280h_1e_1c_1l%7Cwatermark%3D1%26%26r%3D1%26p%3D9%26x%3D2%26y%3D2%26relative%3D1%26o%3D20',
            title:'Painting on Canvas',
            desc:'This is a good hobby for teenage girls'
            },{
            id:'0003',
            imgUrl:'https://p0.meituan.net/deal/e1ae86ee3551b8b35d75ce4336cb1b4b65787.jpg%40450w_280h_1e_1c_1l%7Cwatermark%3D1%26%26r%3D1%26p%3D9%26x%3D2%26y%3D2%26relative%3D1%26o%3D20',
            title:'Painting on Canvas',
            desc:'This is a good hobby for teenage girls'
            }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .title
        margin-top :.2rem
        line-height : .8rem
        background :#eee
        text-indent :.2rem
    .item-img-wrapper
        overflow :hidden
        height:0
        padding-bottom:33.9%
        .item-img
            width :100%
            padding: .1rem
    .item-info
        padding:.1rem
        .item-title
            line-height: .54rem
            font-size:.32rem
            ellipsis() 
        .item-desc
            line-height :.4rem
            color:#ccc
            ellipsis() 

</style>

