<script>
import BtnManager from './components/BtnManager.vue';
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
      imgFooterTB: 'TB:bg-[url(@/assets/images/tablet/image-footer.jpg)]',
      imgFooterDT: 'DT:bg-[url(@/assets/images/desktop/image-footer.jpg)]',
    }
  },
  components: {
    BtnManager,
    GridImages,
    RoundedArrow,

    Logo,
  }
}
</script>
<template>
  <body class=" flex flex-col items-center bg-neo-white font-red-hat-display overflow-hidden">
    <header
      class=" flex flex-col items-center w-full max-w-[425px] TB:max-w-[1024px] DT:max-w-[1920px] pt-12 DT:pt-20 pb-16 DT:pb-[110px]">
      <Logo class=" mb-[58px] TB:mb-16" />
      <div class=" flex flex-col DT:flex-row DT:justify-center items-center DT:gap-[88px] DT:h-[358px]">
        <div
          :class="` DT:hidden w-[414px] TB:w-[820px] h-[153px] TB:h-[303px] mb-12 TB:mb-[72px] ${coverImgMB} bg-cover`">
        </div>
        <div :class="` relative -left-8 self-start hidden DT:block w-[394px] h-[303px] ${coverImgLeft} bg-cover`"></div>
        <div class=" flex flex-col items-center DT:self-end DT:w-[33.1%] DT:pb-2">
          <div class=" flex flex-col gap-6 DT:gap-8 mb-8 px-6 TB:px-[155px] DT:px-0 text-center">
            <h1
              class=" text-neo-dark-gray text-[40px] TB:text-[48px] DT:text-[64px] leading-[40px] TB:leading-[48px] DT:leading-[64px] font-black">
              Group Chat for Everyone
            </h1>
            <p class=" text-neo-gray text-[16px] leading-[26px] font-medium">
              Meet makes it easy to connect with others face-to-face virtually and collaborate across any device.
            </p>
          </div>
          <div class=" flex flex-col TB:flex-row items-center gap-4">
            <BtnManager :data-index="0" btn-text="Download" btn-span-text="v1.3" />
            <BtnManager :data-index="1" btn-text="What is it?" w-size="w-[139px]" />
          </div>
        </div>
        <div :class="` relative -right-8 hidden DT:block self-end w-[394px] h-[303px] ${coverImgRight} bg-cover`"></div>
      </div>
    </header>
    <main
      class=" flex flex-col DT:items-center gap-16 TB:gap-0 w-full max-w-[425px] TB:max-w-[1024px] DT:max-w-[1920px] px-6 TB:px-10 DT:px-[165px]">
      <RoundedArrow class=" TB:mb-[68px] DT:mb-16" :text-number="1" />
      <div class=" grid grid-cols-2 TB:grid-cols-4 gap-6 TB:mb-12 DT:mb-[76px]">
        <GridImages :img-index="0" />
        <GridImages :img-index="1" />
        <GridImages :img-index="2" />
        <GridImages :img-index="3" />
      </div>
      <div class=" DT:w-[52%] TB:mb-20 DT:mb-[72px] TB:px-14 text-[16px] leading-[26px] text-center">
        <h3 class=" mb-6 TB:mb-4 text-neo-cyan tracking-[4px] font-black uppercase">
          Built for modern use</h3>
        <h2
          class=" mb-8 TB:px-16 DT:px-4 text-neo-dark-gray text-[32px] TB:text-[40px] leading-[36px] TB:leading-[44px] font-black">
          Smarter meetings, all in one place</h2>
        <p class=" text-neo-gray font-medium">
          Send messages, share files, show your screen, and record your meetings — all in one
          workspace. Control who can join with invite-only team access, data encryption, and data export.
        </p>
      </div>
      <RoundedArrow class=" mb-[-28px]" :text-number="2" />
    </main>
    <footer
      :class="` relative w-full max-w-[425px] TB:max-w-[1024px] DT:max-w-[1920px] pt-[92px] DT:pt-[116px] pb-[72px] TB:pb-[66px] DT:pb-[104px] bg-neo-cyan text-neo-white`">
      <div
        :class="` absolute top-0 w-full h-full ${imgFooterMB} ${imgFooterTB} ${imgFooterDT} bg-cover opacity-10 pointer-events-none`">
      </div>
      <div
        class=" relative flex flex-col DT:flex-row DT:justify-center items-center px-6 TB:px-24 DT:px-[0px] text-center DT:text-left z-10">
        <h2
          class=" DT:w-[24.3%] mb-6 TB:mb-8 DT:mb-0 DT:mr-[125px] TB:px-8 DT:p-0 text-[32px] TB:text-[40px] leading-[36px] TB:leading-[44px] font-black">
          Experience more together
        </h2>
        <p class=" DT:w-[24.3%] mb-8 TB:mb-10 DT:mb-0 DT:mr-[92px] text-[18px] leading-[26px] font-medium">
          Stay connected with reliable HD meetings and unlimited one-on-one and group video sessions.
        </p>
        <BtnManager :data-index="1" btn-text="Download" btn-span-text="v1.3" />
      </div>
    </footer>
  </body>
</template>