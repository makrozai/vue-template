<template lang="pug">
  #app
    pm-header

    router-view
</template>

<script>
import PmHeader from '@/components/layouts/Header.vue'
export default {
  name: 'app',
  components: { PmHeader }
}
</script>

<style lang="scss">
  @import './scss/main.scss';
</style>
