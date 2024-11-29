<template>
    <div class="watch-wrapper">
        <div class="watch-title">
            侦听器
        </div>
        <div class="watch-main">
            <button @click="updateMessage">点击修改文本内容</button>
            <div class="watch-message">
                {{ message }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            message: "Hello,World!",
            flag: true
        }
    },
    // 函数方法
    methods: {
        updateMessage() {
            if (this.flag) {
                this.message = "你好，世界！"
                this.flag = false;
            } else {
                this.message = "Hello,World!"
                this.flag = true;
            }
        }
    },
    // 侦听器
    watch: {
        // 这里的侦听器方法名称必须要和响应式数据对象的名称一样
        // 比如这里侦听的是 data 中的 message 对象
        message(newValue, oldValue) {
            console.log("新值：" + newValue);
            console.log("旧值：" + oldValue);
        }
    }
}
</script>

<style scoped>
.watch-wrapper {
    height: 150px;
    width: 300px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    margin: 10px auto;
}

.watch-title {
    height: 50px;
    width: 100%;
    background-color: #1e90ff;
    color: #ffffff;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}

.watch-main {
    height: 100px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.watch-message {
    font-size: 18px;
    font-weight: bold;
    margin-top: 8px;
}
</style>