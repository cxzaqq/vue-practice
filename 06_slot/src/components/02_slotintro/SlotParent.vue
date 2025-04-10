<template>
    <div class="parentContainer">
        <SlotChild>
            {{ slotData }}
        </SlotChild>
    </div>
</template>

<!-- 다른 vue 파일을 import 시 내가 원하는 이름을 쓸 수 있다(feat. export default) -->
<script setup>
import SlotChild from "./SlotChild.vue";
import { ref } from "vue";

const slotData = ref("hello data"); // slot은 일반적으로 태그 형태로 전달된다.(일반적인 상태값, 데이터는 props를 활용하는 편)
</script>

<style scoped>
.parentContainer {
    display: flex;
    align-items: center;
    flex-direction: column;
    border: 1px solid black;
}
</style>
