<script setup>
import {onMounted, onUpdated, onUnmounted, reactive} from 'vue';

//화면에 그려질 때 딱 한 번만 호출된다.
// 즉, 화면에 그려질 때 작업하고 싶은 내용이 있으면
// onMounted 콜백 함수에 작성하면 됨. 
onMounted(()=>{
    console.log('컴포넌트가 마운트 됐다.');
});

const state = reactive({
    message: 'Hello!'
}); 
onUpdated(()=>{
    console.log('속성값이 변경되었다면', state.message);
});

onUnmounted(() => {
    alert('나 가유~~~~~~');
});

</script>

<template>
    <h1>Chapter8.vue</h1>
    <div>{{ state.message }}</div>
    <div><input type="text" v-model="state.message"></div>
</template>

<style scoped>

</style>