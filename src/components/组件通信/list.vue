<template>
    <div>
        <ul>
            <li v-for="item in msg2" :key="item">{{ item }}<button @click="del">删除</button></li>
        </ul>
    </div>
</template>
<script>
import { del } from 'vue';

export default {
    name: 'list',
    data() {
        return {

        }
    },
    methods: {
        del() {
            this.msg2.pop(this.item)

        }
    },
    props: {
        msg2: {
            default: {}
        }
    }
}
</script>