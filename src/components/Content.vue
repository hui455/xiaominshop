<script setup>
import { ref } from 'vue'
const Index = ref(0)
const data =[
  [
    {
      title:'xiao mi',
      price:'1999元',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0dce5029e2367f3e70cd786cb192d04a.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi',
      price:'1999元',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0dce5029e2367f3e70cd786cb192d04a.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi',
      price:'1999元',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0dce5029e2367f3e70cd786cb192d04a.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi',
      price:'1999元',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0dce5029e2367f3e70cd786cb192d04a.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi',
      price:'1999元',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0dce5029e2367f3e70cd786cb192d04a.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi',
      price:'1999元',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0dce5029e2367f3e70cd786cb192d04a.png?thumb=1&w=200&h=138&f=webp&q=90'
    },
  ],[
    {
      title:'xiao mi 电视',
      price:'4999元起',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/59dba1732074d35c9258ef3bcca65624.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi 电视',
      price:'4999元起',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/59dba1732074d35c9258ef3bcca65624.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi 电视',
      price:'4999元起',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/59dba1732074d35c9258ef3bcca65624.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi 电视',
      price:'4999元起',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/59dba1732074d35c9258ef3bcca65624.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi 电视',
      price:'4999元起',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/59dba1732074d35c9258ef3bcca65624.png?thumb=1&w=200&h=138&f=webp&q=90'
    },{
      title:'xiao mi 电视',
      price:'4999元起',
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/59dba1732074d35c9258ef3bcca65624.png?thumb=1&w=200&h=138&f=webp&q=90'
    },
  ]
]
const ChangeIndex = (index) => {
  Index.value =index
}
</script>
<template>
  <div class="w-[1226px] mx-auto " >
     <div class="flex justify-between my-6">
      <a href="https://mi.com"  class="bg-[url('https://cdn.cnbj1.fds.api.mi-img.com/mi.com-assets/shop/img/logo-mi2.png')] block size-[56px] bg-cover"></a>
      <div class="flex-1"></div>
      <nav class="flex mx-10 items-center">
        <a @mouseenter="ChangeIndex(0)" class="hover:text-[#ff6700] h-[56px] leading-[56px] px-[10px] inline-block cursor-pointer peer">Xiaomi手机
          <div class=" bg-white shadow border-t border-t-[#e0e0e0] left-0 top-[144px] scale-y-0 transition-transform origin-top group-hover:scale-y-100  absolute w-full min-w-[1226px]   z-[31]">
            <div class="w-[1226px] mx-auto flex py-6">
               <div v-for="(item,index) in data[0]"  class="text-center cursor-pointer grow">
                    <div class="h-[100px]" :class="index !== data[0].length - 1 ? 'border-r-2': ''"><img class="h-[100px] mx-auto" :src="item.src"></div>
                    <p class="text-[12px] h-5 text-[#333]">{{ item.title }}</p>
                    <p class="text-[12px] h-10 text-[#ff6700]">{{ item.price }}</p>
              </div>
            </div>
          </div>
        </a>
        <a @mouseenter="ChangeIndex(1)" class="hover:text-[#ff6700] h-[56px] leading-[56px] px-[10px] inline-block cursor-pointer  peer">Remi手机
        </a>
        <a @mouseenter="ChangeIndex(0)" class="hover:text-[#ff6700] h-[56px] leading-[56px] px-[10px] inline-block cursor-pointer  peer">电视
        </a>
        <a @mouseenter="ChangeIndex(1)" class="hover:text-[#ff6700] h-[56px] leading-[56px] px-[10px] inline-block cursor-pointer  peer">笔记本
        </a>
       <a @mouseenter="ChangeIndex(0)" class="hover:text-[#ff6700] h-[56px] leading-[56px] px-[10px] inline-block cursor-pointer  peer">平板
        </a>
        <a @mouseenter="ChangeIndex(1)" class="hover:text-[#ff6700] h-[56px] leading-[56px] px-[10px] inline-block cursor-pointer  peer">家电
        </a>
        <a @mouseenter="ChangeIndex(0)" class="hover:text-[#ff6700] h-[56px] leading-[56px] px-[10px] inline-block cursor-pointer  peer">路由器
        </a>
        <a  class="hover:text-[#ff6700] h-[56px] leading-[56px] px-[10px] inline-block cursor-pointer ">服务中心
        </a>
        <a class="hover:text-[#ff6700] h-[56px] leading-[56px] px-[10px] inline-block cursor-pointer  ">社区</a>
        <div class=" bg-white shadow border-t border-t-[#e0e0e0] left-0 top-[144px] scale-y-0 transition-transform duration-300 origin-top peer-hover:scale-y-100  absolute w-full min-w-[1226px]   z-[31]">
            <div class="w-[1226px] mx-auto flex py-6">
               <div v-for="(item,index) in data[Index]"  class="text-center cursor-pointer grow">
                    <div class="h-[100px]" :class="index !== data[0].length - 1 ? 'border-r-2': ''"><img class="h-[100px] mx-auto" :src="item.src"></div>
                    <p class="text-[12px] h-5 text-[#333]">{{ item.title }}</p>
                    <p class="text-[12px] h-10 text-[#ff6700]">{{ item.price }}</p>
              </div>
            </div>
          </div>
      </nav>
      <div class="relative ml-6 flex items-center">
        <input class="h-[50px] w-[250px] px-2 focus:outline-none bor" />
        <button class="h-[50px] w-[52px] ther hover:bg-[#ff6700] group">
          <svg t="1718186138197" class="size-6 mx-auto fill-[#2c2c2c] group-hover:fill-white" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="4278" width="16" height="16"><path d="M459.2 142.208a316.928 316.928 0 0 1 242.368 521.152l188.48 194.56-55.232 56.96-191.552-197.632a316.928 316.928 0 1 1-184.064-574.976z m0 73.152a243.84 243.84 0 1 0 161.92 426.112l25.472-26.368a243.84 243.84 0 0 0-187.456-399.744z" p-id="4279" ></path></svg>
        </button>
      </div>
   </div>    
  </div>
  <RouterView />
</template>