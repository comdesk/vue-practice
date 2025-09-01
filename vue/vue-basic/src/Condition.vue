<template>
    <div>
        <!-- <div v-if="isVisible" class="red"></div>
        <div v-if="isVisible == true" class="blue"></div>
        <div v-else class="black"></div> -->
        <!-- <div v-if="count > 1" class="red"></div>
        <div v-else class="blue"></div>

        <button @click="count++">증가</button>
        <button @click="count--">감소</button> -->

        <div v-show="isVisible" class="red"></div>
        <div v-show="!isVisible" class="blue"></div>
        <div v-if="isVisible" class="black"></div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isVisible: false,
            count: 0,
        }
    },
}
</script>

<style scoped>
.red {
    background-color: red;
    width: 100px;
    height: 100px;
}
.blue {
    background-color: blue;
    width: 100px;
    height: 100px;
}
.black {
    background-color: black;
    width: 100px;
    height: 100px;
}
</style>