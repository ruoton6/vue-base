<template>
    <div class="life-wrapper">
        <div class="life-title">
            组件生命周期
        </div>
        <div class="life-main">
            <button @click="updateHandle">更新数据</button>
            <span>{{ message }}</span>
        </div>
    </div>
</template>

<script>
// 生命周期函数
//     创建期：beforeCreate  created
//     挂载期：beforeMounte  mounted
//     更新期：beforeUpdate  updated
//     销毁期：beforeUnmount unmounted

export default {
    data() {
        return {
            message: "数据更新前"
        }
    },
    methods: {
        updateHandle() {
            this.message = "数据更新后"
        }
    },
    beforeCreate() {
        console.log("组件创建之前");
    },
    created() {
        console.log("组件创建之后");
    },
    beforeMount() {
        console.log("组件渲染之前");
    },
    mounted() {
        console.log("组件渲染之后");
    },
    beforeUpdate() {
        console.log("组件更新之前");
    },
    updated() {
        console.log("组件更新之后");
    },
    beforeUnmount() {
        console.log("组件销毁之前");
    },
    unmounted() {
        console.log("组件销毁之后");
    }
}
</script>

<style scoped>
.life-wrapper {
    height: 300px;
    width: 300px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    margin: 10px auto;
}

.life-title {
    height: 50px;
    width: 100%;
    background-color: #1e90ff;
    color: #ffffff;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}

.life-main {
    height: 250px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.life-main button,
.life-main span {
    margin: 6px;
}
</style>