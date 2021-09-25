<template>
    <div class="tab-bar-item" @click="itemClick">
        <!-- 最外层用div包装 防止插槽的属性被替换 -->
      <div v-if="!isActive">
           <slot name="tabbar-icon"></slot>
      </div>
      <div v-else>
           <slot name="tabbar-icon-active"></slot>
      </div>
      <div :style="activeStyle">
           <slot name="tabbar-text"></slot>
      </div>
    </div>
</template>

<script>
export default {
    name:"TabBarItem",
    props:{//拿到自己组件上的值
      link:String,
      activeColor:{
        type:String,
        default:"red"
      }

    },
    data(){
        return {
          
          
        }
    },
    methods:{
      itemClick(){
        // console.log(11);
        this.$router.push(this.link);
      }
    },
    computed:{
      isActive(){
        return this.$route.path.indexOf(this.link)!==-1
      },
      activeStyle(){
        return this.isActive?{color:this.activeColor}:{}
      }
    },
    
}
</script>

<style>
    
  .tab-bar-item{
    flex: 1;
    height: 49px;
    text-align: center;
    font-size: 14px;
  }

  .tab-bar-item img{
      width: 24px;
      height: 24px;
      margin-top: 3px;
      /* 这里可以去除图片下面的3px的空白 */
      vertical-align: middle;
    }

  /* .active{
      color: red;
  } */
</style>