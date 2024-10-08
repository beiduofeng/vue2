<template>
    <div id="box">
        <input type="text" v-model="name" placeholder="key name">
        <input type="text" v-model="info.city" placeholder="key city">
    </div>
</template>
<script>

export default {
    name: 'watch',
    data() {
        return {
            name: 'sunJnYao',
            info: {
                city: 'china'
            }
        }
    },
    watch: {
        //值类型监测
        name(oldValue, value) {
            console.log('oldValue,value', oldValue, value);
        },
        //引用类型监测
        info: {
            handler(oldValue, value) {
                const { city } = value
                console.log('oldValue,value', oldValue, value);
                console.log(city);


            },
            deep: true
        }
    }
}
</script>
<style scoped>
#box {
    border: 1px red solid;
}

input {
    display: block;
    margin: 10px auto;
}
</style>