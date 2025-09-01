<template>
    <div>
        <ChildComponent v-bind:sendProps1="title" v-bind:sendProps2="createAt" :sendProps3="obj" />
    </div>
</template>

<script setup>
import { reactive, ref } from 'vue'
import ChildComponent from './components/ChildComponent.vue'

const title = ref('부모컴포넌트에서 선언된 데이터입니다.')
const createAt = ref(2024)
const obj = reactive({
    id: 2024,
    name: 'John'
})

</script>

<style lang="scss" scoped>

</style>