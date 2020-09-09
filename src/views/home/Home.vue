<template>
  

<div id="home"><nav-bar class="home-nav"><div slot="center">购物街</div></nav-bar>
<swiper>
  <swiper-item v-for="item in banners" :key="item.index">
    <a :href="item.link">
      <img :src="item.image" alt="" >
    </a>
  </swiper-item>
</swiper>
<recommend-view :recommends='recommends'></recommend-view>

</div>

</template>

<script>
import NavBar from 'components/navbar/NavBar'
import {getHomeMultiData} from 'network/home'
import {Swiper,SwiperItem} from 'components/common/swiper'
import RecommendView from './childCompls/RecommendView'

export default {
  name: 'Home',
  components:{
    NavBar,
    Swiper,
    SwiperItem,
    RecommendView
    
  },
  data(){
    return {
      banners:[],
      recommends:[]
      }
  },
  created(){
    getHomeMultiData().then(res=>{
      console.log(res);
      this.banners=res.data.banner.list;
      this.recommends=res.data.recommend.list;

    })
  }



}
</script>

<style>
.home-nav{
  background-color: deeppink;
}


</style>
