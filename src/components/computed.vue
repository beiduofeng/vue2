<template>
    <div id="box">
        <p>num:{{ num }}</p>
        <p>doubleNum:{{ doubleNum }}</p>
        <!-- 此处有错误，input框中应显示200 -->
        <input v-model="doubleNumberTwoWay" />
    </div>

</template>
<script>

export default {
    name: 'computed',
    data() {
        return {
            num: 100
        }
    },
    computed: {
        doubleNum() {
            return this.num * 2
        },
        doubleNumberTwoWay: {
            get: function () {
                return this.number * 2
            },
            set(val) {
                this.number = val / 2
            }
        }
    }
}
</script>
