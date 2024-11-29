<template>
    <div class="classMsg">
        <div :class="classObject">
            Class绑定
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            // 对象中的键代表样式名字，值代表这个样式是否生效
            classObject: {
                "style1": true,
                "style2": true,
                "style3": true,
                "style4": false,
                "style5": false
            }
        }
    }
}
</script>

<style>
.classMsg {
    height: 100px;
    width: 300px;
    margin: 10px auto;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
}

/* 样式1 字体增大*/
.style1 {
    font-size: 22px;
}

/* 样式2 字体加粗 */
.style2 {
    font-weight: bold;
}

/* 样式3 字体变红 */
.style3 {
    color: red;
}

/* 样式4 字体加下划线 */
.style4 {
    text-decoration: underline;
}

/* 样式5 加大字体间距 */
.style5 {
    letter-spacing: 2px;
}
</style>