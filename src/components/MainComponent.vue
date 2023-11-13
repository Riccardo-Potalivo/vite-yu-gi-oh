<template>
    <main>
        <div class="container">
            <section class="p-3">
                
            </section>

            <section class="card_container">
                <div>
                    <h6 class="m-0">Found</h6>
                </div>

            </section>
        </div>
    </main>
</template>

<script>
    export default {
        name: 'MainComponent',
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

main {
    background-color: $PrimaryColor;
}

.card_container {
    background-color: $White;
    padding: 3rem;
    
    div:first-child {
        background-color: $DarkBg;
        color: $White;
        padding: 1rem;
    }
}

</style>