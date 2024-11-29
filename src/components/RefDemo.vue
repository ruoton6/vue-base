<template>
    <div class="ref-wrapper">
        <div class="ref-title">
            模板引用
        </div>
        <div class="ref-main" ref="message" @click="getTemplate">{{ msg }}</div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            msg: "点击引用当前模板"
        }
    },
    methods: {
        getTemplate() {
            console.log(this.$refs.message);
        }
    }
}
</script>

<style scoped>
.ref-wrapper {
    height: 150px;
    width: 300px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    margin: 10px auto;
}

.ref-title {
    height: 50px;
    width: 100%;
    text-align: center;
    line-height: 50px;
    background-color: #1e90ff;
    color: #ffffff;
    font-size: 22px;
}

.ref-main {
    height: 100px;
    width: 100%;
    text-align: center;
    line-height: 100px;
    font-size: 18px;
}
</style>