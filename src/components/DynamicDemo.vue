<template>
    <div class="dynamic-wrapper">
        <div class="dynamic-title">
            动态组件
        </div>
        <div class="dynamic-main">
            <button @click="changeComponent">更改组件</button>
            <component :is="component"></component>
        </div>
    </div>
</template>

<script>
import DynamicDemo01 from "./DynamicDemo01.vue";
import DynamicDemo02 from "./DynamicDemo02.vue";

export default {
    data() {
        return {
            component: "DynamicDemo01"
        }
    },
    methods: {
        changeComponent() {
            // 三元运算符
            this.component = this.component == "DynamicDemo01" ? "DynamicDemo02" : "DynamicDemo01";
        }
    },
    components: {
        DynamicDemo01,
        DynamicDemo02
    }
}
</script>

<style scoped>
.dynamic-wrapper {
    height: 300px;
    width: 300px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    margin: 10px auto;
}

.dynamic-title {
    height: 50px;
    width: 100%;
    background-color: #1e90ff;
    color: #ffffff;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}

.dynamic-main {
    height: 200px;
    width: 200px;
    margin: 25px auto;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    box-sizing: border-box;
    border: 8px solid #ffa500;
}
</style>