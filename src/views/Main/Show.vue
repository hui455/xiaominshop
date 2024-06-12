<template>
<div class="w-[1226px] mx-auto py-4">
  <div class="flex justify-between items-center h-[58px] text-[#333] ">
    <h2 class="text-[22px]">{{ data.title }}</h2>
    <span class="hover:text-[#ff6700] cursor-pointer group" :class="data.Rlist[0].name === undefined ? '':'hidden'">查看更多
      <svg t="1718171666179" class="inline-block fill-[#b0b0b0] group-hover:fill-[#ff6700] size-6" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="6902" data-spm-anchor-id="a313x.search_index.0.i3.7c613a815hrWMh" width="48" height="48"><path d="M890.167652 510.464c-3.606261 209.452522-169.805913 375.652174-379.258435 379.258435-209.452522 3.606261-375.718957-175.237565-379.236174-379.258435-3.606261-209.452522 175.237565-375.718957 379.236174-379.236174 209.474783-3.606261 375.763478 175.237565 379.258435 379.258435 0.690087 39.624348 62.19687 39.66887 61.506783 0-3.917913-228.129391-172.566261-411.269565-397.957565-438.539131-226.103652-27.38087-434.576696 141.178435-476.382609 359.713392-42.674087 222.98713 100.641391 439.251478 314.189913 503.206956 218.957913 65.580522 446.018783-61.128348 530.69913-266.084174 20.591304-49.864348 28.538435-104.69287 29.451131-158.319304 0.667826-39.66887-60.816696-39.624348-61.506783 0z"  p-id="6903"></path><path d="M506.969043 675.328l143.115131-143.11513a31.053913 31.053913 0 0 0 0-43.475479l-143.115131-143.11513c-28.048696-28.048696-71.546435 15.426783-43.497739 43.497739l143.137392 143.09287v-43.475479l-143.137392 143.115131c-28.048696 28.048696 15.426783 71.546435 43.497739 43.475478z"  p-id="6904"></path></svg>
    
    </span>
    <div v-show="data.Rlist[0].name" class="text-base space-x-7">
      <span v-for="(item,index) in data.Rlist" @mousemove="ChangeIndex(index)" class="inline-block cursor-pointer " :class="index === Index ? 'text-[#ff6700] border-b-2 border-[#ff6700]':''">{{ item.name }}</span>
    </div>
  </div>
  <div class="flex h-[614px] w-[1226px] ">
    <div class="h-[614px] basis-60 ">
        <a v-for="item in data.Llist" :href="item.link" target="_blank" class="block mb-[14px]" :class="`h-[${(614 - (14 * (data.Llist.length -1)))/data.Llist.length}px]`"><img  loading="lazy" class="h-full w-full  hover:shadow-2xl duration-300 hover:translate-y-[-3px]"  :src="item.src"></a>
    </div>
    <showItem v-for="(item,index) in data.Rlist" v-show="index === Index" :data="item" ></showItem>
  </div>
</div>
</template>

<script setup>
import showItem from '../Main/showItem.vue'
import {ref} from 'vue'
const {data}= defineProps({
  data:{
    type:Object,
    default:{
      title:'手机',
      Llist:[{
        link:'https://www.mi.com/shop/buy/detail?product_id=19683',
        src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/dcf9ed8c01a7c3d0bf3ecbca3f22537c.png?thumb=1&w=293&h=768&f=webp&q=90'
      }],
      Rlist:[{
        name:'热情',
        list:[{

        }]
      },{
        name:'hhh',
        list:[{}]
      }]
    }
  }
})
let Index = ref(0)
const ChangeIndex = (index) =>{
  Index.value = index
}
</script>