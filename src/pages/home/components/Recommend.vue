<template>
    <div>
        <div class = "title">Hot Sale</div>
        <ul>
            <li class="item border-bottom" 
                v-for="(item,index) of recommendList" 
                :key="index">
                <img class="item-img" v-bind:src='item.imgUrl'/>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button>Detail</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name:'HomeRecommend',
    data (){
        return {
            recommendList:[{
            id:'0001',
            imgUrl:'https://p1.meituan.net/dpdeal/9a538276d0052e600cf3a036db28546e771381.jpg%40450w_280h_1e_1c_1l%7Cwatermark%3D1%26%26r%3D1%26p%3D9%26x%3D2%26y%3D2%26relative%3D1%26o%3D20',
            title:'Painting on Canvas',
            desc:'This is a good hobby for teenage girls'
            },{
            id:'0001',
            imgUrl:'https://p1.meituan.net/dpdeal/9a538276d0052e600cf3a036db28546e771381.jpg%40450w_280h_1e_1c_1l%7Cwatermark%3D1%26%26r%3D1%26p%3D9%26x%3D2%26y%3D2%26relative%3D1%26o%3D20',
            title:'Painting on Canvas',
            desc:'This is a good hobby for teenage girls'
            },{
            id:'0001',
            imgUrl:'https://p1.meituan.net/dpdeal/9a538276d0052e600cf3a036db28546e771381.jpg%40450w_280h_1e_1c_1l%7Cwatermark%3D1%26%26r%3D1%26p%3D9%26x%3D2%26y%3D2%26relative%3D1%26o%3D20',
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
    .item
        overflow :hidden
        display: flex
        height: 1.9rem
        .item-img
            width :1.7rem
            height :1.7rem
            padding: .1rem
        .item-info
            flex : 1
            padding :.1rem
            min-width :0
            .item-title
                line-height: .54rem
                font-size:.32rem
                ellipsis() 
            .item-desc
                line-height :.4rem
                color:#ccc
                ellipsis() 
            .item-button
                line-height :.44rem
                margin-top : .2rem
                background : #ff9300
                padding: 0.2 rem
                border-radius: .06rem

</style>
