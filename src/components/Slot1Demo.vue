<template>
    <div class="slot1-wrapper">
        <div class="slot1-title">
            Slot1
        </div>
        <!-- 插槽 - 可以将模板内容完整的传递给子组件然后渲染出来 -->
        <Slot2Demo>
            <template #slot1="slotPorps">
                <div style="margin: 6px; color: red;">
                    {{ msg1 }} - {{ slotPorps.data1 }}
                </div>
            </template>
            <template #slot2="slotProps">
                <div style="margin: 6px; color: green;">
                    {{ msg2 }} - {{ slotProps.data2 }}
                </div>
            </template>
        </Slot2Demo>
    </div>
</template>

<script>
import Slot2Demo from './Slot2Demo.vue';

export default {
    data() {
        return {
            msg1: "具名插槽1",
            msg2: "具名插槽2"
        }
    },
    components: {
        Slot2Demo
    }
}
</script>

<style scoped>
.slot1-wrapper {
    height: 300px;
    width: 300px;
    margin: 10px auto;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
}

.slot1-title {
    height: 50px;
    width: 100%;
    background-color: #1e90ff;
    color: #ffffff;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}
</style>