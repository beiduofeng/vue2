<template>
    <input type="checkbox" :checked="checked" @change="heddleChange">

</template>
<script>
export default {
    name: 'check',
    model: {
        prop: 'checked',
        event: 'change'
    },
    props: ['checked'],
    methods: {
        heddleChange(e) {
            this.$emit('change', e.target.checked)
        }
    }


}
</script>