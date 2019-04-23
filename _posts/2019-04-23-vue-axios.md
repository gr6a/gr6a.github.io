---
layout: post
title: 'vue axios'
date: 2019-04-23
author: Gra
cover: ''
tags: vue axios 
---

最近有个需求要做h5

本来的想法还是 老路子 设计出完然后切片 直接套两年前做的静态swiper+animate.css模板 加zepto 然后ajax到php后端拉数据库 最后火速交货

正好最近在撸vue 

发现swiper中文网上也出了 vue-awesome-swiper 

要么就拿这个H5来练练手吧 hhh

##安装 vue-awesome-swiper 

```
npm i vue vue-loader css-loader --save
npm i @vue/cli
npm i  vue-awesome-swiper --save
```

引入vue-awesome-swiper animate.css animate.js

```
    <template>
      <div id="app">
        <swiper :options="swiperOption" ref="mySwiper">
            <swiper-slide class="first-page swiper-no-swiping">
                <img class="ani" src="./assets/images/p1-1.png" width="100%" height="100%" swiper-animate-effect="fadeIn" swiper-animate-delay="5.2s" swiper-animate-duration="0.5s">
            </swiper-slide>
        </swiper>
    </template>
<script>
    import { swiper, swiperSlide } from 'vue-awesome-swiper'
    import * as animate from './assets/js/animate.js'
    
    
    export default {
      name: 'app',
        data(){
        swiperOption: {
          direction: 'vertical',
             effect: 'fade',
            mousewheel: true,
            noSwiping: true,
            width: window.innerWidth,
            height: window.innerHeight,
            on:{
              init:function(){
                animate.swiperAnimateCache(this);//隐藏动画元素
                animate.swiperAnimate(this);//初始化完成开始动画
              },
              slideChangeTransitionEnd: function(){
                animate.swiperAnimate(this);//每个slide切换结束时也运行当前slide动画
                var thisindex = this.activeIndex;
              },
    
            },
          },
        }
        components: {
        swiper,
        swiperSlide
      },
    }
</script>   
 <style scoped>
@import './assets/styles/animate.css';
</style>
```

---

bug未解决 ：发现低版本IOS swiper显示问题  是否是因为Unexpected keyword 'const' [](https://segmentfault.com/a/1190000016334023)

ps:h5做完了 开始前没有说清楚最后的逻辑 先定游戏结束后抽奖 于是在后端php中写了一堆抽奖逻辑 

之后的需求是要抽奖发放出将近5位数的门票来用抽奖替代抢票

大概了解php高并发需要要用到redis 

担心阿里乞丐入门服务器受不住 

上线时间紧 沟通后最终游戏结束改成出成绩排行榜