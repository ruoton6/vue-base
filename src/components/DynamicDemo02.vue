<template>
    <h3>{{ message }}</h3>
    <button @click="updateHandle">更改组件数据</button>
</template>

<script>
export default {
    data() {
        return {
            message: "组件2"
        }
    },
    methods: {
        updateHandle() {
            this.message = "组件2 - 更改后";
        }
    }
}
</script>

<style scoped>
h3 {
    font-size: 20px;
    color: blue;
    text-align: center
}
</style>