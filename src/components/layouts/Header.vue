<template lang='pug'>
  ul
    li
      router-link(:to="{ name: 'search' }") Search
      router-link(:to="{ name: 'about' }") About
</template>
<script>
export default {
  
}
</script>
<style lang='scss' scoped>
  ul{
    display: flex;

    li{
      padding: 1em;
    }
  }
</style>

