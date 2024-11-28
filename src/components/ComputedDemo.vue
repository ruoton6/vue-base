<template>
    <div class="computed-wrapper">
        <div class="computed-title">
            计算属性
        </div>
        <div class="computed-main">
            <button v-on:click="computedShow">合并两个数组</button>
            <div class="computed">
                <ul v-show="flag">
                    <li v-for="(item, index) of names1" v-bind:key="index"><span>{{ index }}</span> / {{ item }}</li>
                </ul>
                <ul v-show="flag">
                    <li v-for="(item, index) of names2" v-bind:key="index"><span>{{ index }}</span> / {{ item }}</li>
                </ul>
                <ul v-show="!flag">
                    <li v-for="(item, index) of concatNames" v-bind:key="index"><span>{{ index }}</span> / {{ item }}
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            names1: ["80岁杀人如麻", "90岁初露锋芒", "100岁战争之王"],
            names2: ["粉红兔兔", "水果软糖", "爱吃冰激凌"],
            flag: true
        }
    },
    // 计算属性
    computed: {
        concatNames() {
            return this.names1.concat(this.names2);
        }
    },
    // 方法
    methods: {
        computedShow(e) {
            var flag = this.flag;
            if (flag) {
                this.flag = false;
                e.target.innerHTML = "拆分当前数组";
            } else {
                this.flag = true;
                e.target.innerHTML = "合并两个数组";
            }
        }
    }
}
</script>

<style>
.computed-wrapper {
    height: 300px;
    width: 300px;
    margin: 10px auto;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    border-radius: 2px;
}

.computed-title {
    height: 50px;
    width: 100%;
    background-color: #1e90ff;
    color: #ffffff;
    text-align: center;
    line-height: 50px;
    font-size: 22px;
}

.computed-main {
    height: 200px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
    margin: 0px auto;
}

.computed-main button {
    margin-top: 16px;
}

.computed-main ul {
    list-style: none;
    width: 200px;
    display: flex;
    justify-content: content;
    align-items: center;
    flex-direction: column;
    background-color: rgba(0, 0, 0, .1);
    padding: 8px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
}

.computed-main ul li {
    width: 100%;
    text-align: center;
}

.computed-main ul li span {
    color: red;
}
</style>