<script>
import BtnDownload from './components/BtnDownload.vue'
import BtnLink from './components/BtnLink.vue'
// svg's
import SvgLogo from '@/assets/gallery/starter-code/assets/logo.svg?component'
import decorationMiddle from '@/assets/gallery/starter-code/assets/bg-pattern-2.svg?url'
import decorationCorner from '@/assets/gallery/starter-code/assets/bg-pattern-1.svg?url'
// images
import bgMobile from '@/assets/gallery/starter-code/assets/bg-main-mobile.png'
import bgTablet from '@/assets/gallery/starter-code/assets/bg-main-tablet.png'
import bgDesktop from '@/assets/gallery/starter-code/assets/bg-main-desktop.png'
import phoneImg from '@/assets/gallery/starter-code/assets/illustration-app.png'

export default {
  data() {
    return {
      bgMobile,
      bgTablet,
      bgDesktop,
      phoneImg,
      decorationMiddle,
      decorationCorner,
      txtWhite: 'text-neo-white',
      black: 'bg-neo-black',
      hoverCyan: 'hover:bg-neo-cyan',
      white: 'bg-neo-white',
      hoverYellow: 'hover:bg-neo-yellow',
    }
  },
  components: {
    BtnDownload,
    BtnLink,
    // SVG's
    SvgLogo,
  },
}
</script>
<template>
  <div class=" relative flex flex-col items-center w-[375px] tablet:w-[768px] desktop:w-[1440px] font-IBM-Plex">
    <!-- background -->
    <img class=" absolute -top-[90px] -right-0 tablet:hidden" :src="bgMobile" alt="bgMobile">
    <img class=" absolute tablet:-top-[120px] tablet:left-[0px] hidden tablet:flex desktop:hidden" :src="bgTablet" alt="bgTablet">
    <img class=" absolute desktop:-top-[120px] desktop:left-[0px] hidden desktop:flex" :src="bgDesktop" alt="bgDesktop">
    <!-- decoration corner -->
    <img
      class=" absolute tablet:-top-8 desktop:-top-10 tablet:-right-0 desktop:right-0 hidden tablet:flex tablet:w-[267px] desktop:w-[312px] tablet:h-[400px] desktop:h-[468px]"
      :src="decorationCorner" alt="decorationCorner">
    <header
      class=" flex flex-col gap-16 self-start tablet:gap-[95px] px-6 tablet:px-10 desktop:px-[165px] mt-10 tablet:mt-[62px]">
      <SvgLogo />
      <div
        class=" flex flex-col gap-5 tablet:gap-[28px] w-[327px] tablet:w-[520px] desktop:w-[1015px] h-[320px] tablet:h-[332px] desktop:h-[318px]">
        <h1
          class=" text-[40px] tablet:text-[64px] desktop:text-[88px] leading-[48px] tablet:leading-none tracking-[-0.45px] tablet:tracking-[-0.75px] desktop:tracking-[-1px] font-bold">
          We make your music sound
          extraordinary.</h1>
        <p
          class=" desktop:w-[825px] tablet:text-[18px] desktop:text-[20px] leading-[26px] tablet:leading-[28px] desktop:leading-[34px]">
          A system audio equalizer specifically designed for Android and iOS. Freely tune the
          way your music sounds with a professional grade parametric EQ & volume mixer. Control
          bass, mids, treble, gain control, reverb, and more!
        </p>
      </div>
    </header>
    <main
      class=" relative flex justify-center w-[375px] tablet:w-[696px] desktop:w-[1110px] h-[1024px] tablet:h-[834px] desktop:h-[928px] mt-[68px] tablet:mt-[111px] mb-16 tablet:mb-[88px]">
      <!-- phone image -->
      <img
        class=" absolute tablet:left-16 desktop:left-[121px] w-[209px] tablet:w-[270px] desktop:w-[315px] h-[430px] tablet:h-[556px] desktop:h-[642px] z-10"
        :src="phoneImg" alt="illustration">
      <!-- black -->
      <div
        class=" relative flex justify-center w-[100%] h-[600px] mt-[98px] tablet:mt-[138px] desktop:mt-[213px] bg-neo-black rounded-xl tablet:overflow-hidden">
        <img class=" absolute tablet:-top-[31px] tablet:left-[33%] w-[280px] h-[420px]" :src="decorationMiddle"
          alt="BgPatternMobile">
      </div>
      <!-- orange -->
      <div
        class=" absolute bottom-0 tablet:right-[58px] desktop:right-[95px] bg-neo-orange tablet:w-[399px] desktop:w-[446px] h-[546px] desktop:h-[625px] px-9 tablet:px-12 desktop:px-[54px] pt-12 pb-12 text-neo-white rounded-xl z-20">
        <div class=" flex flex-col gap-3">
          <h2 class=" text-[32px] desktop:text-[40px] leading-10 desktop:leading-[52px] font-bold">Premium EQ</h2>
          <p class=" mb-9 text-lg desktop:text-[20px] desktop:leading-[34px]">
            Get expert-level control with a robust equalizer, volume mixer, and spatial audio. Take
            your listening experience to a whole new level and access all our incredible features!
          </p>
        </div>
        <div class=" flex flex-col pl-[6px] desktop:pl-0">
          <h3 class=" flex justify-between items-center w-[165px] h-[52px] text-xl mb-8"><span
              class=" text-[65px] leading-[52px] font-bold">$4</span>/ month</h3>
          <BtnDownload class=" mb-4 " name="iOS" :bgColor="`${black}`" :bgHoverColor="`${hoverCyan}`"
            :txtColor="`${txtWhite}`" />
          <BtnDownload name="Android" :bgColor="`${white}`" :bgHoverColor="`${hoverYellow}`" />
        </div>
      </div>
    </main>
    <footer
      class=" flex flex-col desktop:flex-row desktop:justify-between gap-8 w-[327px] tablet:w-[696px] desktop:w-[1110px] mb-20">
      <SvgLogo />
      <div class=" flex flex-col tablet:flex-row tablet:items-center desktop:justify-between gap-16 desktop:w-[825px]">
        <p class=" desktop:w-[366px] leading-[26px]">
          All rights reserved © Equalizer 2021 <br />
          Have any problems? Contact us via social media or email us at
          <span class=" font-bold">equalizer@example.com</span>
        </p>
        <div class=" flex justify-between items-center w-[100px] h-5">
          <BtnLink btnName="Facebook" />
          <BtnLink btnName="Instagram" />
          <BtnLink btnName="Twitter" />
        </div>
      </div>
    </footer>
  </div>
</template>