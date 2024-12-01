<template lang="pug">
footer.global-footer
  .top.flex.responsive
    section.flex-1
      h4 关于项目
      ul
        li
          router-link(to='/about') 关于项目

    section.flex-1
      h4 关注我们
      ul
        li Free Now Organization
          ul
            li
              e-link(href='https://github.com/FreeNowOrg') @FreeNowOrg
        li COSA Tech
          ul
            li
              e-link(href='https://github.com/COSA-Studios') @COSA-Studios

    section.flex-1
      h4 友情链接
      ul
        li
          e-link(href='https://pixiv.hanze.icu') PixivNow

  .top.responsive
    section.flex-1
      h4 注意
      p This is a fan made website. We are NOT PicACG official. Please DO NOT share this website anywhere.
      p 这是一个粉丝向网站，我们与 PicACG 官方<u>没有任何关系</u>。<u>请勿</u>在任何地方传播本网站——珍惜眼前。

  .bottom.align-center.responsive
    .copyright
      | Copyright &copy; {{ COPYRIGHT_STR }}
      |
      e-link(:href='GITHUB_URL') {{ PROJECT_NAME }}
      |
      em v{{ VERSION }}
      | &nbsp;|&nbsp;
      span 仅供交流与学习
</template>

<script setup lang="ts">
import { } from 'vue'
import {
  PROJECT_NAME,
  COPYRIGHT_STR,
  GITHUB_URL,
  GITHUB_OWNER,
  VERSION,
} from '../config'
</script>

<style scoped lang="sass">
.global-footer
  > div
    color: var(--theme-accent-link-color)

  .top
    background-color: var(--theme-accent-color)
    padding-top: 2rem
    padding-bottom: 2rem
    gap: 1.5rem

  .bottom
    padding: 1rem
    background-color: var(--theme-accent-color-darken)

  h4
    position: relative
    margin: 1rem 0 0.5rem 0
    padding-bottom: 0.2rem
    border-bottom: 2px solid
    font-size: 1.1rem

  ul
    padding-left: 1rem
    margin: 0.2rem 0

    a
      display: inline
      font-weight: 400

a
  --color: #eee
  font-weight: 600

@media  (max-width: 800px)
  .top
    flex-direction: column
</style>
