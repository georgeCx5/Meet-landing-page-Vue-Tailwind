<script>
import Logo from '@/assets/images/logo.svg?component'
// import coverImg from '@/assets/images/tablet/image-hero.png'
export default {
  data() {
    return {
      coverImg: 'bg-[url(@/assets/images/tablet/image-hero.png)]',
    }
  },
  components: {
    Logo,
  }
}
</script>
<template>
  <body class=" flex flex-col items-center font-red-hat-display">
    <header class=" flex flex-col items-center">
      <Logo />
      <div :class="` w-[414px] h-[153px] ${coverImg} bg-cover`"></div>
      <h1 class=" text-neo-dark-gray text-[40px] leading-[40px] font-black">
        Group Chat for Everyone
      </h1>
      <p class=" text-neo-gray text-[16px] leading-[26px] font-medium">
        Meet makes it easy to connect with others face-to-face virtually and collaborate across any device.
      </p>
    </header>
    <main>
    </main>
    <footer>
    </footer>
  </body>
</template>