<template>
    <header class="d-flex p-3">
        <div class="img_container">
            <img src="../assets/image/ygoprodeck_header_logo.png" alt="logo">
        </div>
        <h1>Yu-Gi-Oh Api</h1>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
    }
</script>

<style lang="scss" scoped>

.img_container {
    width: 80px;
    margin-right: 2rem;
}

img {
    width: 100%;
    height: 100%;
    object-fit: contain;
}

</style>