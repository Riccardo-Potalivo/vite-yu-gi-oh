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
      MainComponent,
      
    },

    data() {
      return {
        store,
        params: {
          num: 20,
          offset: 0
        }
      }
    },

    methods: {
      getCards() {
        axios.get(store.apiUrl, {params: this.params}).then((response) => {
          console.log(response.data.data);
          store.cardList = response.data.data;
        })
        .finally(() => {
          store.loading = false
        })
      }
    },

    created() {
      this.getCards()
    },


    computed: {

    }
  }
</script>

<style lang="scss" scoped>

</style>