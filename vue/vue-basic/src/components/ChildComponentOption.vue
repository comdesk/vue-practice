<template>
    <div>{{ sendProps1 }}</div>
    <div>{{ sendProps2 }}</div>
    <div>{{ sendProps3 }}</div>
    <div>{{ sendProps3.id }}</div>
    <div>{{ sendProps3.name }}</div>
</template>

<script>

export default {
    props: {
        sendProps1: {
            type: String,
            required: true
        },
        sendProps2: Number,
        sendProps3: {
            type: Object,
            // default: () => {
            //     return {
            //         id: 0,
            //         name: ''
            //     }
            // }
        }
        // sendProps3: Object,
    },
    data () {
        

        return {}
    }
}
</script>

<style lang="scss" scoped>

</style>