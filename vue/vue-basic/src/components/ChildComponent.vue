<template>
    <button @click="sendEvent">자식 컴포넌트에서 만든 버튼</button>
</template>

<script>
export default {
    data() {
        return {
            text: '자식컴포넌트에서 선언된 데이터입니다.',
            // text2: '자식컴포넌트에서 선언된 추가적인 데이터입니다.'
        }
    },
    methods: {
        sendEvent() {
            this.$emit('send-event', this.text)
        //   this.$emit('send-event2', this.text2)
        }
    }
}
</script>

<style lang="scss" scoped>

</style>