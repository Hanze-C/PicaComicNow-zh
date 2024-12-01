<template lang="pug">
#about-container
  h1 Pica Comic Now

  h2 版权声明
  .card
    p 请求得到的全部数据以及媒体资源，版权归其原作者所有。
    p PicaComicNow 程序通过 Apache-2.0 协议授权。
    p 仅供交流与学习
  h2 更新日志
  .card
    h3 V0.1.2 Beta/zh-CHS(1732800000)
    p 1.更新简体中文(zh-CHS)
    p 2.删除页面标题，保护隐私。
</template>

<script setup lang="ts">
import { onMounted } from 'vue'
import { setTitle } from '../utils/setTitle'

onMounted(() => {
  setTitle('About')
})
</script>

<style scoped lang="sass"></style>