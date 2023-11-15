<template>
    <div class="container">
        <section class="card_container">
            <div>
                <h6 class="m-0">Found {{ store.cardList.length }} cards</h6>
            </div>
            <div class="row g-4">
                <CardComponent v-for="(card, index) in store.cardList" :key="index"
                :img="card.card_images[0].image_url"
                :name="card.name"
                :archetype="card.archetype"
                />
                <LoadingComponent v-if="store.loading"/>
            </div>

        </section>
    </div>
</template>

<script>
    import { store } from '../data/store.js';
    import CardComponent from './main/CardComponent.vue';
    import LoadingComponent from './main/LoadingComponent.vue';

    export default {
        name: 'MainComponent',
        components: {
            CardComponent,
            LoadingComponent,
        },
        data() {
            return {
                store
            }
        },
        methods: {
            setParams(search) {
            console.log(search)
            }
        }
      
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.card_container {
    background-color: $White;
    padding: 3rem;
    
    >div:first-child {
        background-color: $DarkBg;
        color: $White;
        padding: 1rem;
    }
}

</style>