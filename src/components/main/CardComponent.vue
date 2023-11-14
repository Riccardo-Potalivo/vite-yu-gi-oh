<template>
    <div class="col-2 text-center">
        <img :src="img" :alt="name">
        <h6>{{ name }}</h6>
        <p>{{ archetype }}</p>
    </div>
</template>

<script>
    export default {
        name: 'CardComponent',
        props: {
            img: String,
            name: String,
            archetype: String,
        }

    }
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

img {
    width: 100%;
}

</style>