<template>
    <div class="news-wrapper">
        <div class="news-title">
            组件生命周期应用 / 新闻列表
        </div>
        <div class="news-list">
            <div class="news" v-for="(item, index) of data" :key="index">
                <div class="title">
                    {{ item.title }}
                </div>
                <div class="content">
                    {{ item.content }}
                </div>
                <div class="time">
                    {{ item.time }}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            data: []
        }
    },
    mounted() {
        // 模拟网络请求
        this.data = [
            {
                title: "标题1",
                content: "内容1",
                time: "2024年12月3日"
            },
            {
                title: "标题2",
                content: "内容2",
                time: "2024年12月3日"
            },
            {
                title: "标题3",
                content: "内容3",
                time: "2024年12月3日"
            },
            {
                title: "标题4",
                content: "内容4",
                time: "2024年12月3日"
            },
            {
                title: "标题5",
                content: "内容5",
                time: "2024年12月3日"
            }
        ];
    }
}
</script>

<style scoped>
.news-wrapper {
    width: 300px;
    margin: 10px auto;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
}

.news-title {
    height: 50px;
    width: 100%;
    background-color: #1e90ff;
    color: #ffffff;
    text-align: center;
    line-height: 50px;
    font-size: 20px;
}

.news-list {
    width: 100%;
    min-height: 50px;
    padding: 8px;
    box-sizing: border-box;
}

.news {
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
    padding: 6px;
    margin: 6px 0px;
    border: 1px solid rgba(0, 0, 0, .1);
    box-sizing: border-box;
}

.title {
    height: 30px;
    width: 100%;
    background-color: #ffa500;
    color: #4f4f4f;
    text-align: center;
    line-height: 30px;
    font-size: 20px;
}

.content {
    width: 100%;
    line-height: 22px;
    font-size: 20px;
    padding: 8px;
}

.time {
    height: 22px;
    width: 120px;
    text-align: center;
    line-height: 22px;
    background-color: #008000;
    color: #ffffff;
    font-size: 16px;
    padding: 2px;
    margin: 6px 0px;
    border-radius: 3px;
    box-shadow: 0px 1px 3px rgba(0, 0, 0, .5);
}
</style>