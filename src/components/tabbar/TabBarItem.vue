<template>
  
    <div class='tab-bar-item' @click="itemClick">
  <slot v-if='!isActive' name='icon'></slot>
  <slot v-else name='icon-active'></slot>
  <div :class='{active:isActive}'><slot  name='text'></slot></div>
  </div>

</template>

<script>


export default {
  name: 'TabBarItem',
  props:{
path:String
  },
data(){
  return{
    // isActive:true
  }
},
computed:{
  isActive(){
    return this.$route.path.indexOf(this.path)!==-1
  }
},
methods:{
  itemClick(){
    console.log('day')
 
    this.$router.replace(this.path)
  }
}

}
</script>

<style>


.tab-bar-item{
  flex:1;
  text-align: center;
  height: 49px;
  color: #136ca8;
}
.tab-bar-item img{
  width: 24px;
  height: 24px;
  vertical-align: middle;
}
.active{
  color:#d4237a;
}
</style>
