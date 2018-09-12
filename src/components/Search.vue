<template lang="pug">
  main
    img(src='@/assets/logo.png')
    h1 {{ msg }}
    h2 Essential Links
    div
      h3 contador
      p {{ count }}
      p {{ getDouble }}

      div
        button(@click="increment") +
        button(@click="decrement") -
      div
        button(@click="increment10") +10
        button(@click="incrementAsync") +Async
</template>

<script>
  import { mapState, mapMutations, mapGetters } from 'vuex'
  export default {
    name: 'search',

    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    },

    computed: {
      ...mapState(['count']),

      ...mapGetters(['getDouble'])
    },

    methods: {
      ...mapMutations(['increment', 'decrement']),
      increment10() {
        this.$store.commit('increment', {
          number: 10
        })
      },

      incrementAsync(){
        this.$store.dispatch('incrementAsync',{
          number: 2
        })
        .then(() => {
          console.log('action terminada')
        })
      }
    }
  }
</script>
</script>

<style lang="scss">
</style>
