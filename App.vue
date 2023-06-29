<script>
import HeaderBtn from './components/HeaderBtn.vue';
import GridImages from './components/GridImages.vue';
import RoundedArrow from './components/RoundedArrow.vue';

import Logo from '@/assets/images/logo.svg?component'

export default {
  data() {
    return {
      coverImgMB: 'bg-[url(@/assets/images/tablet/image-hero.png)]',
      coverImgLeft: 'bg-[url(@/assets/images/desktop/image-hero-left.png)]',
      coverImgRight: 'bg-[url(@/assets/images/desktop/image-hero-right.png)]',
      imgFooterMB: 'bg-[url(@/assets/images/mobile/image-footer.jpg)]',
    }
  },
  components: {
    HeaderBtn,
    GridImages,
    RoundedArrow,

    Logo,
  }
}
</script>
<template>
  <body class=" flex flex-col items-center bg-neo-white font-red-hat-display overflow-hidden">
    <header class=" flex flex-col items-center w-full max-w-[425px] pt-12 pb-16">
      <Logo class=" mb-[58px]" />
      <div :class="` w-[414px] h-[153px] mb-12 ${coverImgMB} bg-cover`"></div>
      <div class=" flex flex-col gap-6 mb-8 px-6 text-center">
        <h1 class=" text-neo-dark-gray text-[40px] leading-[40px] font-black">
          Group Chat for Everyone
        </h1>
        <p class=" text-neo-gray text-[16px] leading-[26px] font-medium">
          Meet makes it easy to connect with others face-to-face virtually and collaborate across any device.
        </p>
      </div>
      <div class=" flex flex-col items-center gap-4">
        <HeaderBtn :data-index="0" btn-text="Download" btn-span-text="v1.3" />
        <HeaderBtn :data-index="1" btn-text="What is it?" w-size="w-[139px]" />
      </div>
    </header>
    <main class=" flex flex-col gap-16 w-full max-w-[425px] px-6">
      <RoundedArrow :text-number="1" />
      <div class=" grid grid-cols-2 gap-6">
        <GridImages :img-index="0" />
        <GridImages :img-index="1" />
        <GridImages :img-index="2" />
        <GridImages :img-index="3" />
      </div>
      <div class="  text-[16px] leading-[26px] text-center">
        <h3 class=" mb-6 text-neo-cyan tracking-[4px] font-black uppercase">Built for modern use</h3>
        <h2 class=" mb-8 text-neo-dark-gray text-[32px] leading-[36px] font-black">Smarter meetings, all in one place</h2>
        <p class=" text-neo-gray font-medium">
          Send messages, share files, show your screen, and record your meetings — all in one
          workspace. Control who can join with invite-only team access, data encryption, and data export.
        </p>
      </div>
      <RoundedArrow :text-number="2" />
    </main>
    <footer :class="` relative w-full max-w-[425px] mt-[-28px] pt-[92px] pb-[72px] bg-neo-cyan text-neo-white`">
      <div :class="` absolute top-0 w-full h-full ${imgFooterMB} bg-cover opacity-10 pointer-events-none`"></div>
      <div class=" relative flex flex-col items-center px-6 text-center z-10">
        <h2 class=" mb-6 text-[32px] leading-[36px] font-black">Experience more together</h2>
        <p class=" mb-8 text-[18px] leading-[26px] font-medium">
          Stay connected with reliable HD meetings and unlimited one-on-one and group video sessions.
        </p>
        <HeaderBtn :data-index="1" btn-text="Download" btn-span-text="v1.3" />
      </div>
    </footer>
  </body>
</template>