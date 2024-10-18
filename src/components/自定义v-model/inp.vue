<template>
    <input type="text" :value="value" @input="heddleInput">
</template>
<script>
export default {
    name: 'inp',
    props: ['value'],
    methods: {
        heddleInput(e) {
            this.$emit('input', e.target.value)
        }
    }
}
</script>