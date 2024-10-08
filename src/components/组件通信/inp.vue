<template>
    <div>
        <input type="text" v-model="name" placeholder="请输入姓名"><button @click="tj">提交</button>
    </div>
</template>
<script>
export default {
    name: 'int',
    data() {
        return {
            name: ''
        }
    },
    methods: {
        tj() {
            // 向父组件触发自定义事件 addItem，this.name 作为参数
            this.$emit('addItem', this.name);
            console.log(this.name);

        }
    }
}
</script>