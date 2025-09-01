<template>
    <div>
        <h1>{{ text }}</h1>
        <h1>changeText 함수 호출 값: {{ changeText() }}</h1>
        <h1>changeText 함수 호출 값: {{ changeText() }}</h1>
        <h1>changeText 함수 호출 값: {{ changeText() }}</h1>

        <h2>{{ computedText }}</h2>
        <h2>{{ computedText }}</h2>
        <h2>{{ computedText }}</h2>
    </div>
</template>

<script>
export default {
    data () {

        return {
            text: 'Computed 테스트 데이터입니다.',
        }
    },
    //methods 부분에 선언된 함수와 동일한 로직일 때,
    //캐싱 기능이 없는 methods는 호출될 떄마다 console 값이 출력 되었습니다.
    //반면에, computed는 캐싱 기능이 있기 때문에 methods와 어떤 차이점이 있는지
    //한 번 주의깊게 살펴 보는 것이 포인트입니다.
    computed: {
        // 계산된 속성
        computedText () {
            console.log('Computed 기능을 생성하였습니다.')

            return this.text.split("").reverse().join("")
        },
    },
    methods: {
        // 메서드 핸들러
        changeText () {
            console.log('함수 호출')
            console.log(this.text)

            return this.text.split("").reverse().join("")
        },
    },
}
</script>

<style lang="scss" scoped>

</style>