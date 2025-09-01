<template>
    <button @click="sendEvent">자식 컴포넌트에서 만든 버튼</button>
</template>

<script setup>
import { ref } from 'vue'

const data = ref('자식컴포넌트에서 선언된 데이터입니다.')
const data2 = ref('자식컴포넌트에서 선언된 추가적인 데이터입니다.')

const emit = defineEmits(['send-event', 'send-event2'])
const sendEvent = () => {
  emit('send-event', data.value)
  emit('send-event2', data2.value)
}

</script>

<style lang="scss" scoped>

</style>