<template>
  <div class="sign-in">
    <div class="sign-in__info">
      <LogoHeader />
      <FormClass />
      <CopyrightFooter />
    </div>

    <div class="sign-in__bg">
      <BackgroundImg :src="require('@/assets/bg.png')" alt="bg" />
    </div>
  </div>
</template>

<script>

import FormClass from './components/FormClass.vue';
import CopyrightFooter from './components/CopyrightFooter.vue'
import LogoHeader from './components/LogoHeader.vue';
import BackgroundImg from './components/BackgroundImg.vue'


export default {
  components: {
    FormClass, CopyrightFooter, LogoHeader, BackgroundImg
  }
}
</script>

<style lang="scss">
@import "scss/style";
</style>