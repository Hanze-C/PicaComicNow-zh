<template lang="pug">
#error-404
  h1 404 Not Found:(
  p 这个页面走丢了>_<
</template>

<script setup lang="ts">
import { onMounted } from 'vue'
import { setTitle } from '../utils/setTitle'
onMounted(() => {
  setTitle('404', 'Error')
})
</script>

<style scoped lang="sass"></style>