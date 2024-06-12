<template>
 <div class="grid grid-cols-4 gap-[14px] pl-3 content-between h-[614px] grow">
   <Card v-for="(item,index) in newArr " :key="index" :data="item"  />
   <div class="w-[232px] h-[300px] flex flex-col justify-between " :class="data.name ? '':'hidden'">
    <a v-if="newArr.length === 7 || data.list[7]" :href="data.list[7].link" class="h-[143px] w-full flex justify-between items-center  cursor-pointer px-7  py-5 bg-white hover:shadow-2xl duration-300 hover:translate-y-[-3px]">
         <div>
           <p class="text-[#333] text-[14px] w-[94px]">{{ data.list[7].title }}</p>
           <p  class="text-[#ff6700] text-[12px] pt-[6px]">{{ data.list[7].price }}</p>
         </div>
         <img class="size-20" :src="data.list[7].src">
      </a>
      <a class="h-[143px] w-full flex justify-between items-center  cursor-pointer px-7  py-5 bg-white hover:shadow-2xl duration-300 hover:translate-y-[-3px]">
         <div>
           <h1 class="text-[#333] text-[18px]">浏览更多</h1>
           <p  class="text-[#757575] text-[12px]">{{ data.name }}</p>
         </div>
         <svg t="1718171666179" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="6902" data-spm-anchor-id="a313x.search_index.0.i3.7c613a815hrWMh" width="48" height="48"><path d="M890.167652 510.464c-3.606261 209.452522-169.805913 375.652174-379.258435 379.258435-209.452522 3.606261-375.718957-175.237565-379.236174-379.258435-3.606261-209.452522 175.237565-375.718957 379.236174-379.236174 209.474783-3.606261 375.763478 175.237565 379.258435 379.258435 0.690087 39.624348 62.19687 39.66887 61.506783 0-3.917913-228.129391-172.566261-411.269565-397.957565-438.539131-226.103652-27.38087-434.576696 141.178435-476.382609 359.713392-42.674087 222.98713 100.641391 439.251478 314.189913 503.206956 218.957913 65.580522 446.018783-61.128348 530.69913-266.084174 20.591304-49.864348 28.538435-104.69287 29.451131-158.319304 0.667826-39.66887-60.816696-39.624348-61.506783 0z" fill="#ff6700" p-id="6903"></path><path d="M506.969043 675.328l143.115131-143.11513a31.053913 31.053913 0 0 0 0-43.475479l-143.115131-143.11513c-28.048696-28.048696-71.546435 15.426783-43.497739 43.497739l143.137392 143.09287v-43.475479l-143.137392 143.115131c-28.048696 28.048696 15.426783 71.546435 43.497739 43.475478z" fill="#ff6700" p-id="6904"></path></svg>
      </a>
   </div>
 </div>
</template>

<script setup>
import Card from './Card.vue';
const {data} = defineProps({
  data:{
    type:Object,
    default:{
      name:'热情',
      list:[]
    }
  }
})
const newArr = data.name ? data.list.slice(0,7) : data.list.slice(0,8)

</script>