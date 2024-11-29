<template>
    <div class="wrap2-wrapper">
        <div class="wrap2-title">
            {{ msg }}
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            msg: "Wrap2组件"
        }
    }
}
</script>

<style scoped>
.wrap2-wrapper {
    height: 200px;
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
</style>