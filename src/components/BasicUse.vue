<template>
    <div id="BU">
        <div>{{ msg }}</div>
        <div> flag 的值是 {{ flag ? ' 真的 ' : '假的' }} </div>
        <a :href="url">点我领取红包</a>
        <div v-html="rawHtml"></div>
        {{ rawHtml }}
        <div v-if="show">如果 show === true 就展示我</div>
    </div>
</template>
<script>
export default {
    name: 'BasicUse',
    data() {
        return {
            msg: '雄关漫道真如铁',
            flag: false,
            url: 'https://www.baidu.com',
            rawHtml: "<a href='#'>点我去看视频</a>",
            show: true,

        }
    },
}
</script>
<style scoped></style>