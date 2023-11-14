<template>
  <HeaderComponent/>
  <MainComponent/>
</template>

<script>
  import { store } from './data/store.js';
  import axios from 'axios';
  import HeaderComponent from './components/HeaderComponent.vue';
  import MainComponent from './components/MainComponent.vue';

  export default {
    name: 'App',

    components: {
      HeaderComponent,
      MainComponent
    },

    data() {
      return {
        store
      }
    },

    methods: {
      getCard() {
        axios.get(store.apiUrl).then((response) => {
          console.log(response.data.data)
        })
      }
    },

    created() {
      this.getCard()
    },

    computed: {

    }
  }
</script>

<style lang="scss" scoped>

</style>