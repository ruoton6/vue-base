<template>
    <div class="model-wrapper">
        <div class="model-title">
            表单输入绑定
        </div>
        <div class="model-main">
            <form action="#">
                <!-- 主要用到 v-model -->
                <input type="text" v-model="message" maxlength="20" placeholder="在这输入内容">
                <div class="model-message">
                    {{ message }}
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            message: ""
        }
    }
}
</script>

<style>
.model-wrapper {
    height: 200px;
    width: 300px;
    margin: 10px auto;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
}

.model-title {
    height: 50px;
    width: 100%;
    text-align: center;
    line-height: 50px;
    background-color: #1e90ff;
    font-size: 22px;
    color: #ffffff;
}

.model-main {
    height: 150px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.model-main form {
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.model-main input {
    padding: 2px;
}

.model-message {
    height: 20px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    margin-top: 8px;
    line-height: 20px;
    text-align: center;
    font-size: 18px;
    padding: 6px;
}
</style>