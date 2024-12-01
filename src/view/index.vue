<template lang="pug">
#index-container
  h1 PicACG

  .info.tips(style='margin-bottom: 1.5rem')
    .title 注意
    p 本站仍在建设中...

  .flex.gap-1
    .card.flex-1
      h2 Pica Comic Now
      p V0.1.2 CHS
      p Developed By FreeNowOrg
      p zh-CHS Version By COSA Tech
      p Copyright © 2021 - 2024 Pica Comic Now@0.1.2
      p 仅供交流与学习
      p {{ time }}
    .card.flex-1
      h2 Links
      p
        router-link.button(to='/profile') 个人资料
        | 
        router-link.button(to='/favourite') 个人收藏

</template>

<script setup lang="ts">
import { setTitle } from '@/utils/setTitle';
import { ref } from 'vue'

setTitle()

const time = ref(new Date().toLocaleString())
setInterval(() => {
  time.value = new Date().toLocaleString()
}, 1000)
</script>

<style scoped lang="sass"></style>
