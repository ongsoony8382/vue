<script setup>
// props 외부에서 들어오는 데이터 (하드 코어 말고)
// color라는 속성으로 데이터를 받을 수 있다.
const props = defineProps({
    color: String // color가 스트링 타입이라는 뜻. 타입 지정
}); // props라는 객체에 color라는 속성을 추가.

// {{}} template(HTML)안에서 상수 혹은 변수에 담겨있는 값(value)을 표시할 때 사용
</script>

<template>   
    <!-- :style 이것은 vue문법
        중괄호 2개 겹쳐져 있는 것은 콧수염(Mustache 템플릿)
    -->
    <div>Black Tire</div>
    <div :style="{color: props.color}">{{ props.color || 'BLACK' }} TIRE</div> 
    <div style = "background-color: blue; color: #fff;">Black Tire</div>
    <!-- // 뷰는 언디파인드면 표시하지 않는다. 그냥 무시한다. props.color가 언디파인드면 무시  -->
</template>

<style scoped>

</style>