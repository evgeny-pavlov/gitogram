<template>
  <feeds />
</template>

<script>
import { feeds } from './pages/feeds'
import Feeds from './pages/feeds/feeds.vue'

export default {
  name: 'App',
  components: {
    feeds,
    Feeds
  }
}
</script>

<style src="./global.scss" lang="scss"></style>
