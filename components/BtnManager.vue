<script>
export default {
   data() {
      return {
         data: [
            {
               bg: 'bg-neo-cyan hover:bg-neo-hover-sky',
               spanText: 'text-neo-sky-blue'
            }, {
               bg: 'bg-neo-dark-purple hover:bg-neo-hover-purple',
               spanText: 'text-neo-light-purple'
            }
         ],
      }
   },
   props: {
      dataIndex: {
         Number,
         default: 0,
      },
      btnText: {
         String,
         default: 'Empty',
      },
      btnSpanText: {
         String,
      },
      wSize: {
         String,
         default: 'w-[193px]',
      },
   },
}
</script>
<template>
   <button
      :class="` ${wSize} h-[58px] ${data[dataIndex].bg} text-white text-[16px] leading-[26px] font-red-hat-display font-black rounded-[29px] select-none`">
      {{ btnText }}
      <span :class="data[dataIndex].spanText">{{ btnSpanText }}</span>
   </button>
</template>