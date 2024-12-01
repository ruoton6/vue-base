<template>
    <div class="slot2-wrapper">
        <div class="slot2-title">
            Slot2
        </div>
        <div class="slot2-main">
            <!-- slot为插槽标签，可以将父组件传递来的模板数据渲染出来 -->
            <slot name="slot1" :data1="data1">
                <!-- 插槽默认值，若父组件没有传递任何数值过来则显示下方的模板内容 -->
                slot1 - 默认值
            </slot>
            <slot name="slot2" :data2="data2">
                slot2 - 默认值
            </slot>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            data1: "slot1",
            data2: "slot2"
        }
    }
}
</script>

<style scoped>
.slot2-wrapper {
    height: 200px;
    width: 200px;
    margin: 25px auto;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
}

.slot2-title {
    height: 50px;
    width: 100%;
    background-color: #ffa500;
    color: #ffffff;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}

.slot2-main {
    height: 150px;
    width: 200px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}
</style>