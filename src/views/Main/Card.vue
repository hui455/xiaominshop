<template>
  <a :href="data.link" target="_blank" class="flex flex-col items-center text-center cursor-pointer w-[232px] h-[300px] py-5 bg-white hover:shadow-2xl duration-300 hover:translate-y-[-3px]">
     <img loading="lazy" :src="data.src" alt="" class="size-40">
     <h3 class="text-[14px] text-[#333] mt-3 mb-[3px]">{{ data.title }}</h3>
     <p class="text-[13px] text-[#b0b0b0] mb-[10px] line-clamp-1 mx-5">{{ data.desc }}</p>
     <div class="text-[14px]"><span class="text-[#ff6700]">{{ data.price }}</span><span class="line-through text-[#b0b0b0] decoration-[#b0b0b0] ml-2">{{ data.oldPrice }}</span></div>
  </a>
</template>

<script setup>
defineProps({
  data: {
    type: Object,
    default: {
      src:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/adde6bae41441887017824f46cf31602.png?thumb=1&w=250&h=250&f=webp&q=90',
      title:'小米10青春版',
      price:'1999元',
      oldPrice:'2999元',
      desc:'小米10青春版',
      link:'https://www.baidu.com' 
    }
  }
})

</script>