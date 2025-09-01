<template>
    <div>{{ sendProps1 }}</div>
    <div>{{ sendProps2 }}</div>
    <div>{{ sendProps3 }}</div>
    <div>{{ sendProps3.id }}</div>
    <div>{{ sendProps3.name }}</div>
</template>

<script setup>
import { toRefs } from 'vue';

const props = defineProps({
    sendProps1: {
        type: String,
        required: true
    },
    sendProps2: {
        type: Number,
        required: true
    }, 
    sendProps3: {
        type: Object,
        required: true
    }
})
const {sendProps1, sendProps2, sendProps3} = toRefs(props)
</script>

<style lang="scss" scoped>

</style>