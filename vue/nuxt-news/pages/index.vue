<template>
    <div class="page">
        <CardComponent v-for="article in data?.articles" :key="article.url" :data="article" />
    </div>
</template>

<script setup lang="ts">
import type { ApiStructure } from '~/types/api';
import CardComponent from './components/Card.vue';

const API_KEY = "8014040a743e47ec8c162fa0f44b7176";
const API_URL = `https://newsapi.org/v2/everything?q=Apple&from=2025-03-28&sortBy=popularity&apiKey=${API_KEY}`;
const {data, pending, error, refresh} = await useAsyncData<ApiStructure>('getNews', () => $fetch(API_URL));

console.log(data.value);
</script>

<style lang="scss" scoped>
.page {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-content: flex-start;

    // width: calc(100% - 96px);
    width: 100%;

    padding: 48px;
    gap: 24px;
}
</style>