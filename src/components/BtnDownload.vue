<script>
import LogoiOS from '@/assets/gallery/starter-code/assets/icon-apple.svg?component'
import LogoAndroid from '@/assets/gallery/starter-code/assets/icon-android.svg?component'

export default {
   components: {
      LogoiOS,
      LogoAndroid,
   },
   props: {
      name: {
         String,
         default: 'No name',
      },
      bgColor: {
         String,
         default: 'bg-red-400',
      },
      bgHoverColor: {
         String,
         default: 'hover:bg-red-700',
      },
      txtColor: {
         String,
         default: 'text-neo-black',
      }
   }
}
</script>
<template>
   <button :class="`${bgColor} ${bgHoverColor} ${txtColor}`"
      class=" w-[100%] h-[61px] flex justify-center items-center gap-2 text-[18px] leading-[34px] font-bold rounded-xl">
      <component :is="`Logo${name}`" />
      {{ name }} Download
   </button>
</template>