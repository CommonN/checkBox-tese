<template>
  <div id="app">
    <h3>面试题</h3>
    <Head/>
    <Main/>
  </div>
</template>

<script>
import Head from '@/components/head.vue'
import Main from '@/components/main.vue'
export default {
  name: 'App',
  components: {
    Head,
    Main
  }
}
</script>

<style lang="less"></style>
