<template>
    <div id="app">
        <Slot1 :url="website.url">
            {{ website.text }}
        </Slot1>
        <!-- 以便获取p标签 -->
        <p ref="r" @click="testRefs">$refs</p>
    </div>
</template>

<script>
import son from './son.vue';

export default {
    // 定义当前的组件名
    name: 'slotIndex',
    // 注册要消费的，导入的组件
    components: {
        son
    },

    data() {
        return {
            website: {
                url: 'https://www.baidu.com',
                text: "去百度"
            }
        }
    },
    methods: {
        testRefs: function () {
            console.log(this.$refs.r);    //获取p标签

        }
    }
}
</script>

<style></style>