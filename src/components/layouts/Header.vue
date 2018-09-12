<template lang='pug'>
  ul
    li
      router-link(:to="{ name: 'search' }") Search
    li
      router-link(:to="{ name: 'about' }") About
</template>
<script>
export default {
  
}
</script>
<style lang='scss' scoped>
  ul{
    li{
      padding: 1em;
    }
  }
</style>

