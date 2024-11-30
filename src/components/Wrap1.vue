<template>
    <div class="wrap1-wrapper">
        <div class="wrap1-title">
            Wrap1
        </div>
        <!-- 使用子组件传递来的自定义事件来实现数据子传父 -->
        <Wrap2 @searchData="wrap2SearchData" />
        <div class="wrap1-search">
            {{ search }}
        </div>
    </div>
</template>

<script>
// 组件局部注册，组件嵌套
import Wrap2 from "./Wrap2.vue";

export default {
    data() {
        return {
            search: ""
        }
    },
    components: {
        "Wrap2": Wrap2
    },
    methods: {
        // 参数就是子组件传递来的数据
        wrap2SearchData(data) {
            this.search = data;
        }
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

.wrap1-search {
    padding: 6px;
    width: 200px;
    height: 20px;
    margin: 10px auto;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
}
</style>