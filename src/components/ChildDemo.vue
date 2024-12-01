<template>
    <div class="box2-wrapper">
        <div class="box2-title">
            子组件
        </div>
        <div class="box2-content">
            {{ msg }}
            {{ msgFn("props子传父数据") }}
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {

        }
    },
    // 获取父组件传递的数据并且校验数据的类型和设置默认值
    props: {
        msg: {
            type: String,
            default: "Parent没有传递数据"
        },
        msgFn: Function
    }
}
</script>

<style scoped>
.box2-wrapper {
    height: 200px;
    width: 200px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    margin: 25px auto;
}

.box2-title {
    height: 50px;
    width: 100%;
    background-color: #ffa500;
    color: #4f4f4f;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}

.box2-content {
    text-align: center;
    padding: 16px;
}
</style>