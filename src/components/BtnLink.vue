<script>
import IconFacebook from '@/assets/gallery/starter-code/assets/icon-facebook.svg?component'
import IconInstagram from '@/assets/gallery/starter-code/assets/icon-instagram.svg?component'
import IconTwitter from '@/assets/gallery/starter-code/assets/icon-twitter.svg?component'

export default {
   components: {
      IconFacebook,
      IconInstagram,
      IconTwitter,
   },
   props: {
      btnName: String,
   }
}
</script>
<template>
   <button>
      <component :is="`Icon${btnName}`" />
   </button>
</template>