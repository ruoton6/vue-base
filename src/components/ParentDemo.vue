<template>
    <div class="box-wrapper">
        <div class="box-title">
            父组件
        </div>
        <ChildDemo :msg="msg" />
    </div>
</template>

<script>
import ChildDemo from './ChildDemo.vue';

export default {
    data() {
        return {
            msg: "Parent数据"
        }
    },
    components: {
        "ChildDemo": ChildDemo
    }
}
</script>

<style scoped>
.box-wrapper {
    height: 300px;
    width: 300px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    margin: 10px auto;
}

.box-title {
    height: 50px;
    width: 100%;
    background-color: #1e90ff;
    color: #ffffff;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}
</style>