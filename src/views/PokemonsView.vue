<script setup>
    import {
        RouterLink
    } from 'vue-router';

    import {
        useGetData
    } from '@/composables/getData'


    const {
        data,
        getData,
        loading
    } = useGetData()


    getData("https://pokeapi.co/api/v2/pokemon")
</script>



<template>
    <h1>pokemons</h1>
    <div class="spinner-border" role="status" v-if="loading">
        <span class="visually-hidden">Loading...</span>
    </div>
    <div v-if="data">
        <ul>
            <li v-for="pokemon in data.results">
                <RouterLink :to="`/pokemons/${pokemon.name}`">{{ pokemon.name  }}</RouterLink>
            </li>
        </ul>
    </div>
   
</template>