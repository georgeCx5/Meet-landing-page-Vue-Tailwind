<script>
export default {
   data() {
      return {

      }
   },
   props: {
      textNumber: {
         Number,
         required: true,
      }
   }
}
</script>
<template>
   <div class=" relative z-10 flex flex-col items-center select-none">
      <div class=" w-[1px] h-[84px] bg-neo-gray bg-opacity-25"></div>
      <div
         class=" flex items-center justify-center w-14 h-14 bg-neo-white text-neo-gray text-[16px] leading-[26px] font-black border-[1px] border-neo-gray border-opacity-25 rounded-full">
         0{{ textNumber }}
      </div>
   </div>
</template>