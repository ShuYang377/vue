<template>
    <div>
        <detail-banner></detail-banner>
        <detail-header></detail-header>
        <div class="content">
            <detail-list :list="list"></detail-list>
        </div>
    </div>
</template>

<script>
import DetailBanner from './components/Banner' 
import DetailHeader from './components/Header' 
import DetailList   from './components/List'
export default {
    name: 'Detail',
    components: {
        DetailBanner,
        DetailHeader,
        DetailList
    },
    data (){
        return {
            list: [{
                title:'adult',
                children: [{
                    title: 'adult tickets for 3 days',
                    children: [{
                        title: 'adult tickets for 3 positons for 3 days'
                    }]
                },{
                    title :'adult tickets for 5 days'
                }]
            },{
                title:'student'
            },{
                title:'child'
            },{
                title:'sale'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
    .content
        height : 50rem


</style>
