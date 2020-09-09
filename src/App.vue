<template>
  <div id="app">
    <router-view></router-view>
<tab-bar>
  <tab-bar-item path='/home'>
<img slot='icon' :src="require('assets/img/tabbar/儿童手绘-房子.png')" alt="">
<img slot='icon-active' :src="require('assets/img/tabbar/儿童手绘-房子 (1).svg')" alt="">
    <div slot='text'>首页</div>
  </tab-bar-item>
   <tab-bar-item path='/category'>
<img slot="icon" :src="require('assets/img/tabbar/儿童手绘-火箭.png')" alt="">
<img slot="icon-active" :src="require('assets/img/tabbar/儿童手绘-火箭 (1).svg')" alt="">
<div slot="text">分类</div>
   </tab-bar-item>
    <tab-bar-item path='/cart'>
 <img slot="icon" :src="require('assets/img/tabbar/儿童手绘-汽车.png')" alt="">
 <img slot="icon-active" :src="require('assets/img/tabbar/儿童手绘-汽车 (1).svg')" alt="">
 <div slot="text">购物车</div>
    </tab-bar-item>
     <tab-bar-item path='/profile'>
 <img slot="icon" :src="require('assets/img/tabbar/儿童手绘-男孩.png')" alt="">
  <img slot="icon-active" :src="require('assets/img/tabbar/儿童手绘-男孩 (1).svg')" alt="">
 <div slot="text">我的</div>
     </tab-bar-item>
  
</tab-bar>

 </div>
</template>

<script>
import TabBar from 'components/tabbar/TabBar'
import TabBarItem from 'components/tabbar/TabBarItem'

export default {
  name: 'App',
  components: {
    TabBar,
    TabBarItem
    
  }
}
</script>

<style>
@import "assets/css/base.css";
</style>
