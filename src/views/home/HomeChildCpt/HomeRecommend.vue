<template>
    <div class="recommend">
        <div v-for="(item,index) in recommends" :key="index" class="recommend-item">
            <a :href="item.link">
                <img :src="item.image" alt="">
            </a>
            <div>{{item.title}}</div>
        </div>
    </div>
</template>

<script>
export default {
    name:"HomeRecommend",
    props:{
        recommends:{
            type:Array,
            default(){
                return []
            }
        }
    }
}
</script>

<style scoped>
    .recommend{
        width: 100%;
        display: flex;
        text-align: center;
        padding: 10px 0 20px;
        border-bottom:10px solid #eee ;

        font-size: 14px;
        
     
    }

    .recommend-item{
        flex: 1;
    }

    .recommend img{
        width: 65px;
        height: 65px;
        margin-bottom: 6px;
    }

</style>