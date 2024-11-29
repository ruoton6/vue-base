<template>
    <div class="wrap1-wrapper">
        <div class="wrap1-title">
            Wrap1组件
        </div>
        <Wrap2 />
    </div>
</template>

<script>
// 组件局部注册，组件嵌套
import Wrap2 from "./Wrap2.vue";

export default {
    components: {
        "Wrap2": Wrap2
    }
}
</script>

<style scoped>
.wrap1-wrapper {
    height: 300px;
    width: 300px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    margin: 10px auto;
}

.wrap1-title {
    height: 50px;
    width: 100%;
    background-color: #1e90ff;
    color: #ffffff;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}
</style>