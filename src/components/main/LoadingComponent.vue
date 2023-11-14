<template>
    <div>
        <i class="fa-solid fa-circle-notch fa-spin"></i>
    </div>
</template>

<script>
    export default {
        name: 'LoadingComponent'
        
    }
</script>

<style lang="scss" scoped>
div {
    background-color: #00000070;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

</style>