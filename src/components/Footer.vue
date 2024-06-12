<template>
  <div class="w-[1226px] mx-auto">
    <div class="flex border-b border-[#e0e0e0] justify-around item-center text-[#616161]">
      <div class="flex-basis-1/5 grow text-center my-[27px]  "><a class="text-base cursor-pointer   hover:text-[#ff6800]">预约维修服务</a></div>
      <div class="flex-basis-1/5 grow text-center my-[27px] border-l "><a class="text-base cursor-pointer   hover:text-[#ff6800]">7天无理由退货</a></div>
      <div class="flex-basis-1/5 grow text-center my-[27px] border-l "><a class="text-base cursor-pointer   hover:text-[#ff6800]">预约维修服务</a></div>
      <div class="flex-basis-1/5 grow text-center my-[27px] border-l "><a class="text-base cursor-pointer   hover:text-[#ff6800]">预约维修服务</a></div>
      <div class="flex-basis-1/5 grow text-center my-[27px] border-l "><a class="text-base cursor-pointer   hover:text-[#ff6800]">预约维修服务</a></div>
    </div>
    <div class="flex justify-end py-8 " >
      <div class="flex justify-around grow ml-[60px] mr-[30px]">
      <dl v-for="item in data">
      <dt class="text-[#424242] text-[14px]  pb-3">{{ item.title }}</dt>
      <dd v-for="item in item.list" class="mt-2"><a class="text-[#757575] text-[12px] cursor-pointer hover:text-[#ff6800]">{{ item }}</a></dd>
      </dl>
     </div>
     <div clas="">
      <div class="text-center px-[48px] mb-4 border-l">
        <p class="text-[#ff6800] text-[22px]">400-100-5678</p>
        <p class="text-[#616161] text-[12px] mb-1">8:00-18:00 （仅收市话费）</p>
        <a class="after:content-['人工客服'] text-[#ff6800] text-[12px] cursor-pointer hover:bg-[#ff6800] hover:text-white  border-[#ff6800] border after:leading-[30px] h-[30px] w-[120px] block mx-auto"></a>
      </div>
      <div class="text-center">
        <p class="text-[#ff6800] text-[22px] ">400-180-8888</p>
        <div class="w-[200px] mx-auto text-start translate-x-6">
          <p class="text-[#616161] text-[12px] mb-1">8:00-18:00（仅收市话费）<br/> 适用于：MIX FOLD、巨屏电视系列</p>
        </div>
        <a class="after:content-['人工客服'] text-[#ff6800] text-[12px] cursor-pointer hover:bg-[#ff6800] hover:text-white border-[#ff6800] border after:leading-[30px] h-[30px] w-[120px] block mx-auto"></a>
      </div>
    </div>
  </div>
  </div>
</template>
<script setup >
const data =[
  {
    title:'选购指南',
    list:[
      '手机',
      '电视',
      '笔记本',
      '平板',
      '穿戴',
      '耳机',
      '家电',
      '路由器',
      '音箱',
      '配件'
    ]
  },
  {
    title:'服务中心',
    list:[
      '申请售后',
      '售后政策',
      '维修服务价格',
      '订单查询',
      '以旧换新',
      '保障服务',
       '防伪查询',
       'F码查询'
      ]
  },{
    title:'线下门店',
    list:[
      '小米之家',
      '服务网点',
      '授权体验店'
  ]
  },
  {
    title:'关于小米',
    list:[
      '了解小米',
      '加入小米',
      '联系我们',
      '友情链接',
      '销售联盟',
      '企业采购',
  ]
  },
  {
    title:'关注我们',
    list:[
      '新浪微博',
      '官方微信',
      '联系我们',
      '公益基金会'
    ]
  }
]
</script>