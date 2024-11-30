<template>
    <div class="wrap2-wrapper">
        <div class="wrap2-title">
            {{ msg }}
        </div>
        <div class="wrap2-search">
            <input type="text" maxlength="20" v-model="search">
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            msg: "Wrap2组件",
            search: ""
        }
    },
    // 使用侦听器来不断触发事件来发送自定义事件给父组件
    watch: {
        search(newValue, oldValue) {
            this.$emit("searchData", newValue);
        }
    }
}
</script>

<style scoped>
.wrap2-wrapper {
    height: 100px;
    width: 200px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    margin: 25px auto;
}

.wrap2-title {
    height: 50px;
    width: 100%;
    background-color: #ffa500;
    color: #4f4f4f;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}

.wrap2-search {
    height: 50px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.wrap2-search input {
    padding: 2px;
}
</style>