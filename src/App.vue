<template>
  <HeaderComponent/>
  <main>
    <SearchComponent @filter-change="setParams"/>
    <MainComponent/>
  </main>
</template>

<script>
  import { store } from './data/store.js';
  import axios from 'axios';
  import HeaderComponent from './components/HeaderComponent.vue';
  import MainComponent from './components/MainComponent.vue';
  import SearchComponent from './components/main/SearchComponent.vue';


  export default {
    name: 'App',

    components: {
      HeaderComponent,
      MainComponent,
      SearchComponent      
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
      },

      setParams(search) {
        console.log(search)
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
@use './assets/styles/partials/variables' as *;


main {
    background-color: $PrimaryColor;
}

</style>