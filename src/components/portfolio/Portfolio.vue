<template>
    <div>
        <h1>Your current stocks</h1>
        <br>
        <app-stock v-for="stock in stocks" :stock="stock"></app-stock>
    </div>
</template>

<script>
    import {mapGetters} from 'vuex';
    import Stock from './Stock.vue';

    export default {
        computed: {
            ...mapGetters({
                stocks: 'stockPortfolio'
            })
        },
        components: {
            appStock: Stock
        }
    }
</script>

<style scoped>
    h1{
        text-align: center;
        color: white;
        font-family: 'Poppins', sans-serif;
    }
</style>