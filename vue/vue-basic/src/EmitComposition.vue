<template>
    <div>
        부모컴포넌트 레이아웃
        <ChildComponent @send-event="parentEvent" @send-event2="parentEvent"/>
    </div>
</template>

<script setup>
import ChildComponent from './components/ChildComponentEmitCom.vue'

const parentEvent = (event) => {
    console.log(event)
}
</script>

<style lang="scss" scoped>

</style>