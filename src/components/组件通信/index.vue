<template>
    <div>
        <!-- 子传父 -->
        <inp @addItem="this.AddItem" />
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
            msg2: {
                a: 1,
                b: 2,
                c: 3
            }
        }
    },
    methods: {
        fun() {
            console.log(this.AddItem, '111')
        }
    }
}



</script>