<template>
    <div>
        <!-- 子传父 -->
        <inp @addItem="emitsAddItem" />
        <!-- 父传子 -->
        <list :msg2="this.msg2" />
    </div>
</template>
<script>
import inp from './inp.vue';
import list from './list.vue';
export default {
    name: 'index',
    components: {
        inp,
        list
    },
    data() {
        return {
            //传至index
            msg2: ['zhangSan', 'liSi', 'wangWu', 'maZi', 'liLiu']
        }
    },
    methods: {
        emitsAddItem() {
            console.log(this.name)
            this.msg2.push(this.name)
        },
        delItem() {
            this.msg2.pop(this.name)
        }
    }
}



</script>