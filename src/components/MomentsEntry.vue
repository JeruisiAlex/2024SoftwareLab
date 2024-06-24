<template>
    <div :style="{ width: width }" class="momentEntryMainContainer">
        <div class="iconContainer">
            <img :src="data.icon" style="width: 60px;height: 60px; border-radius: 5px;">
        </div>
        <div class="mainContainer">
            <div class="nameContainer">
                {{ data.name }}
            </div>
            <div class="contentContainer">
                <el-text class="textConcent">
                    {{ data.textContent }}
                </el-text>
                <div class="picContainer">
                    <span v-for="(pic, index) in data.picList" :key="index" class="picItemContainer">
                        <img :src="pic" class="picImage">
                    </span>
                </div>
                <div class="bottomContainer">
                    <span class="timeContainer">
                        {{ formattedTime }}
                    </span>
                    <span></span>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
import moment from 'moment';
export default {
    name: 'MomentEntry',
    props: {
        width: {
            type: String,
            default: '300px'
        },
        data: {
            type: Object,
            default: () => ({
                icon: require("@/test_resource/icon.jpg"),
                name: "pluto",
                textContent: "1111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111",
                picList: [require("@/test_resource/icon.jpg"), require("@/test_resource/icon.jpg"), require("@/test_resource/icon.jpg"), require("@/test_resource/icon.jpg"), require("@/test_resource/icon.jpg"), require("@/test_resource/icon.jpg"), require("@/test_resource/icon.jpg")],
                time: "2024-6-25"
            })
        }
    },
    computed: {
        formattedTime() {
            const now = moment();
            const time = moment(this.data.time);
            const diffInMinutes = now.diff(time, 'minutes');
            const diffInHours = now.diff(time, 'hours');
            const diffInDays = now.diff(time, 'days');
            const diffInYears = now.diff(time, 'years');

            if (diffInMinutes < 60) {
                return `${diffInMinutes}分钟前`;
            } else if (diffInHours < 24) {
                return `${diffInHours}小时前`;
            } else if (diffInDays < 365) {
                return time.format('MM月DD日');
            } else {
                return time.format('YYYY年MM月DD日');
            }
        }
    }
}
</script>

<style scoped>
.bottomContainer{
    width: 100%;
    /* background-color: red; */
    display: flex;
}
.timeContainer{
    margin-left: 15px;
    color: #b1b3b8;
}
.momentEntryMainContainer {
    height: auto;
    border: 1px solid #ccc;
    background-color: #f9f9f9;
    display: flex;
}

.mainContainer {
    display: flex;
    flex-direction: column;
    margin-left: 20px;
    margin-top: 15px;
    width: 100%;
    align-items: flex-start;
}

.iconContainer {
    margin-top: 15px;
    margin-left: 15px;
    height: 60px;
    /* 固定图标高度 */
    width: 60px;
    display: flex;
}

.nameContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    font-size: larger;
    color: #337ecc;
}

.contentContainer {
    height: auto;
    width: 100%;
    margin-top: 15px;
    margin-left: -5px;
    align-items: flex-start;
}

.textConcent {
    display: flex;
    text-align: left;
    word-wrap: break-word;
    word-break: break-all;
    white-space: normal;
}

.picContainer {
    display: flex;
    flex-wrap: wrap;
    /* 允许换行 */
    margin-top: 10px;
}

.picItemContainer {
    width: calc(33.33% - 10px);
    /* 每行3个图片，并减去左右边距 */
    margin-left: 5px;
    margin-right: 5px;
    margin-bottom: 10px;
    /* 保证图片之间有间隔 */
    aspect-ratio: 1;
    /* 保持宽高比 */
    position: relative;
}

.picImage {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>
