<template>
    <section class="container p-3">
        <select name="searchbar" v-model="textSearch" @change="filterValue"> 
            <option value="">All</option>
            <option value="ABC">ABC</option>
            <option value="Aesir">Aesir</option>
            <option value="Alien">Alien</option>
        </select>
    </section>

</template>

<script>
    export default {
        name: 'SearchComponent',
        data() {
            return {
                textSearch: ''
            }
        },

        methods: {
            filterValue() {
                this.$emit('filterChange', this.textSearch)
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>