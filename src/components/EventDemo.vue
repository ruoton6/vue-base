<template>
    <div class="count-wrapper">
        <h3>事件方法处理器</h3>
        <button v-on:click="addCount('Hello', $event)">点击增大下方数字</button>
        <div class="count">{{ count }}</div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            count: 0
        }
    },
    methods: {
        addCount(msg, e) {
            this.count++;
            console.log(msg);
            console.log(e);
        }
    }
}
</script>

<style scoped>
.count-wrapper {
    height: 150px;
    width: 300px;
    background-color: #bdd5ec;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    margin: 0px auto;
}

.count {
    margin-top: 12px;
}
</style>