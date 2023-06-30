<script>
import gridOne from '@/assets/images/desktop/image-woman-in-videocall.jpg'
import gridTwo from '@/assets/images/desktop/image-women-videochatting.jpg'
import gridThree from '@/assets/images/desktop/image-men-in-meeting.jpg'
import gridFour from '@/assets/images/desktop/image-man-texting.jpg'

export default {
   data() {
      return {
         data: [
            gridOne,
            gridTwo,
            gridThree,
            gridFour,
         ]
      }
   },
   props: {
      imgIndex: {
         Number,
         required: true,
      }
   }
}
</script>
<template>
   <img class=" rounded-lg TB:rounded-xl select-none" :src="data[imgIndex]" :alt="`Image ${imgIndex + 1}`" draggable="false">
</template>