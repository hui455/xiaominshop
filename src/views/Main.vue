<script setup>
import Show from './Main/Show.vue'
import { ref } from 'vue'
const asideShowData = ['手机','电视','家电','笔记本 平板','出行 穿戴','耳机 音箱','健康 儿童','生活 箱包','智能 路由器','电源 配件']
let CarouselIndex = ref(0)
const changeIndex = (num) => {
  CarouselIndex.value += num
  if(CarouselIndex.value > 4) CarouselIndex.value = 0
  if(CarouselIndex.value < 0) CarouselIndex.value = 4

}
let timer = null; // 初始时设置为null  
// 开始定时器的函数  
function startTimer() {  
  if (timer !== null) {  
    // 如果定时器已经存在，则不需要重新创建  
    return;  
  }  
  timer = setInterval(() => {  
    changeIndex(1);  
  }, 3000);  
}  
startTimer()
// 暂停定时器的函数  
function pauseTimer() {
  if (timer !== null) {  
    clearInterval(timer); // 清除定时器  
    timer = null; // 将变量重置为null  
  }  
} 
const asideData=[
  {
    name:'保障服务',
    src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82abdba456e8caaea5848a0cddce03db.png?w=48&h=48'
  },{
    name:'企业团购',
    src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/806f2dfb2d27978e33fe3815d3851fa3.png?w=48&h=48'
  },{
     name:'F码通道',
     src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/eded6fa3b897a058163e2485532c4f10.png?w=48&h=48'
  },{
    name:'米粉卡',
    src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/43a3195efa6a3cc7662efed8e7abe8bf.png?w=48&h=48'
  },{
    name:'以旧换新',
    src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f4846bca6010a0deb9f85464409862af.png?w=48&h=48'
  },{
    name:'话费充值',
    src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9a76d7636b08e0988efb4fc384ae497b.png?w=48&h=48'
  }
]

const fiexData =[
  {
    name:'手机APP',
    src1:'https://i8.mifile.cn/b2c-mimall-media/98a23aae70f25798192693f21c4d4039.png',
    src2:'https://i8.mifile.cn/b2c-mimall-media/74c4fcb4475af8308e9a670db9c01fdf.png'
  },
  {
    name:'个人中心',
    src1:'https://i8.mifile.cn/b2c-mimall-media/55cad219421bee03a801775e7309b920.png',
    src2:'https://i8.mifile.cn/b2c-mimall-media/41f858550f42eb1770b97faf219ae215.png'
  },{
    name:'售后服务',
    src1:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/12eb0965ab33dc8e05870911b90f3f13.png',
    src2:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/95fbf0081a06eec7be4d35e277faeca0.png'
  },{
    name:'人工客服',
    src1:'https://i8.mifile.cn/b2c-mimall-media/4f036ae4d45002b2a6fb6756cedebf02.png',
    src2:'https://i8.mifile.cn/b2c-mimall-media/5e9f2b1b0da09ac3b3961378284ef2d4.png'
  },
  {
    name:'购物车',
    src1:'https://i8.mifile.cn/b2c-mimall-media/d7db56d1d850113f016c95e289e36efa.png',
    src2:'https://i8.mifile.cn/b2c-mimall-media/692a6c3b0a93a24f74a29c0f9d68ec71.png'
  }
]

const Data1 ={
      title:'手机',
      Llist:[{
        link:'https://www.mi.com/shop/buy/detail?product_id=19683',
        src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/dcf9ed8c01a7c3d0bf3ecbca3f22537c.png?thumb=1&w=293&h=768&f=webp&q=90'
      }],
      Rlist:[{
        list:[{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },
       ]
      }]
    }
   const Data2 ={
      title:'手机',
      Llist:[{
        link:'https://www.mi.com/shop/buy/detail?product_id=19683',
        src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/644966333bed3ed0323ae3f7086baa72.jpg?thumb=1&w=293&h=375&f=webp&q=90'
      },{
        link:'https://www.baidu.com',
        src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/23ea3bb9378ff3a7fc65b57731730576.jpg?thumb=1&w=293&h=375&f=webp&q=90'
      }],
      Rlist:[{
        name:'手机',
        list:[
          {
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },
    {
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },{
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    },
       ]
      },{
        name:'热情',
        list:[]
      }]
    }
  let isTop = ref(true)
  const toTop = ()=>{
    window.scrollTo(0,0)
  }
  (function() {
  window.addEventListener('scroll', scrollThrottler, false);

  var scrollTimeout;
  function scrollThrottler() {
    if (!scrollTimeout) {
      scrollTimeout = setTimeout(function () {
        scrollTimeout = null;
        actualScrollHandler();
      }, 100);
    }
  }
  function actualScrollHandler() {
    const Y = window.scrollY
    if((Y > 800 && !isTop.value) || (Y<800 && isTop.value)) isTop.value = !isTop.value
  }
}());

</script>
<template>
   <div class="w-[1226px] mx-auto" >
    <div>
     <!-- 侧边导航栏以及轮播图 -->
     <div class="relative h-[472px]">
      <!-- 侧边导航栏 -->
      <div class="z-30 flex flex-col  py-5 w-60 bg-[rgba(105,101,101,.6)] absolute top-0 left-0">
        <div v-for="(item,index) in asideShowData" :key="index" class="flex justify-between items-center h-[42px] pl-7 pr-4 cursor-pointer hover:bg-[#ff6700]">
           <span class="text-white text-[14px]">{{ item }}</span>
           <svg t="1718035651279" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="4272" width="14" height="14"><path d="M266.605714 877.129143a68.973714 68.973714 0 0 0 3.291429 97.572571 78.994286 78.994286 0 0 0 107.958857 0L809.545143 571.245714a68.973714 68.973714 0 0 0 19.602286-68.169143 68.900571 68.900571 0 0 0-19.602286-68.169142L377.856 31.670857a78.994286 78.994286 0 0 0-107.958857 0 68.973714 68.973714 0 0 0 0 100.790857L666.624 503.222857 269.897143 873.837714a69.046857 69.046857 0 0 0-1.682286 1.609143z" fill="#fff" p-id="4273"></path></svg>
        </div>
      </div>
      <!--轮播图-->
      <div @mouseover="pauseTimer" @mouseleave="startTimer"  class="absolute top-0 left-0 w-full h-full">
        <a href="#" class="absolute top-0 left-0 transition-opacity duration-700" :class="CarouselIndex === 0 ? 'opacity-100':'opacity-0'"><img  src="../assets/img/1.jpg"></a>
        <a href="#" class="absolute top-0 left-0 transition-opacity duration-700" :class="CarouselIndex === 1 ? 'opacity-100':'opacity-0'"><img  src="../assets/img/2.webp"></a>
        <a href="#" class="absolute top-0 left-0 transition-opacity duration-700" :class="CarouselIndex === 2 ? 'opacity-100':'opacity-0'"><img  src="../assets/img/3.webp"></a>
        <a href="#" class="absolute top-0 left-0 transition-opacity duration-700" :class="CarouselIndex === 3 ? 'opacity-100':'opacity-0'"><img  src="../assets/img/4.webp"></a>
        <a href="#" class="absolute top-0 left-0 transition-opacity duration-700" :class="CarouselIndex === 4 ? 'opacity-100':'opacity-0'"><img  src="../assets/img/5.webp"></a>
        <div @click="changeIndex(-1)" class="absolute bottom-1/2 left-60  translate-y-1/2  h-[70px] w-10 flex justify-center items-center cursor-pointer hover:bg-[#333] group">
          <svg t="1718089368462" class="group-hover:fill-white fill-[#cdcdcd]" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="4253" width="32" height="32"><path d="M729.6 931.2l-416-425.6 416-416c9.6-9.6 9.6-25.6 0-35.2-9.6-9.6-25.6-9.6-35.2 0l-432 435.2c-9.6 9.6-9.6 25.6 0 35.2l432 441.6c9.6 9.6 25.6 9.6 35.2 0C739.2 956.8 739.2 940.8 729.6 931.2z" p-id="4254" ></path></svg>
        </div>
        <div  @click="changeIndex(1)" class="absolute bottom-1/2 right-0 translate-y-1/2 rotate-180  h-[70px] w-10 flex justify-center items-center cursor-pointer hover:bg-[#333] group">
         <svg t="1718089368462" class="group-hover:fill-white fill-[#cdcdcd]" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="4253" width="32" height="32"><path d="M729.6 931.2l-416-425.6 416-416c9.6-9.6 9.6-25.6 0-35.2-9.6-9.6-25.6-9.6-35.2 0l-432 435.2c-9.6 9.6-9.6 25.6 0 35.2l432 441.6c9.6 9.6 25.6 9.6 35.2 0C739.2 956.8 739.2 940.8 729.6 931.2z" p-id="4254" ></path></svg>
        </div>
        <div class="flex justify-between items-center absolute  bottom-6 right-6 h-10 w-[80px]">
          <div v-for="(_,index) in 5" @click="CarouselIndex = index" class="size-[9px] border  rounded-full  cursor-pointer hover:border-[#444] hover:bg-[#cdcdcd]" :class="index === CarouselIndex ?'border-[#444] bg-[#cdcdcd]' :'bg-[#444] border-[#cdcdcd]'"></div>
        </div>
      </div>
    </div>
   </div>
   <div class="flex justify-between items-center w-full mt-4 mb-6 gap-4 ">
    <div class="flex w-60 h-[170px] bg-[#5f5750] flex-wrap justify-center px-2 py-2 ">
      <a class="h-[76px] basis-1/3 block pt-4 text-center opacity-80 text-white hover:opacity-100 text-[12px] gorup cursor-pointer" v-for="item in asideData"><img class="size-6 mx-auto mb-1 " :src="item.src"><span >{{ item.name }}</span></a>
    </div>
    <a><img  width="316" height="170"  src="../assets/img2/6b67117bc92924fb2ff0e7ad2be86084.png"></a>
    <a><img  width="316" height="170" src="../assets/img2/8dede2520f8dfff9c9b690af498cafe8.jpg"></a>
    <a><img width="316" height="170"  src="../assets/img2/1ac77590368ff636d0b4f6a988133f55.png"></a>
   </div>
    </div>
    <div class="bg-[#f5f5f5] w-full min-w-[1226px]">
      <div class="w-[1226px] mx-auto py-6">
         <a href="#"><img  src="../assets/img2/a2011078db9b3708d3caae52df7be3cc.webp" alt=""></a>
      </div>  
      <Show :data="Data1"></Show>
      <Show :data="Data2"></Show>
      <div class="w-[1226px] mx-auto py-6">
         <a href="#"><img  src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/88e35cffc82cd98cd53172460067af17.jpg?thumb=1&w=1533&h=150&f=webp&q=90" alt=""></a>
      </div>
    </div>
    <!-- 右侧导航 -->
    <div class="fixed right-0 bottom-[80px] flex flex-col items-center">
      <div v-for="(item,index) in fiexData" :class="index === fiexData.length -1 ?'border-b' :''" class="border-t bg-white border-l  border-[#e0e0e070] xl:w-[70px] flex flex-col items-center text-center px-[5px] xl:py-[14px] pt-[6px] group">
        <img class="size-5 xl:size-8 mb-[6px] group-hover:hidden " :src="item.src1">
        <img class="size-5 xl:size-8 mb-[6px] hidden group-hover:block " :src="item.src2">
        <span class="text-[#999] text-[14px] group-hover:text-[#ff6700] hidden xl:inline">{{ item.name }}</span>
      </div>
      <div v-show="isTop" @click="toTop" class="border-t bg-white border-l border-b cursor-pointer border-[#e0e0e070] mt-4 xl:w-[70px] flex flex-col items-center text-center px-[5px] xl:py-[14px] pt-[6px] group">
        <img class="size-5 xl:size-8 mb-[6px] group-hover:hidden " src="https://i1.mifile.cn/f/i/2018/home/totop.png">
        <img class="size-5 xl:size-8 mb-[6px] hidden group-hover:block " src="https://i1.mifile.cn/f/i/2018/home/totop_hover.png">
        <span class="text-[#999] text-[14px] group-hover:text-[#ff6700] hidden xl:inline">回顶部</span>
      </div>
    </div>
    
</template>