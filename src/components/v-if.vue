<template>
    <div>
        <div v-if="type === 'a'">type===a</div>
        <div v-else-if="type === 'b'">type===b</div>
        <div v-else>type===other</div>

        <div v-show="type === 'a'">type===a</div>
        <div v-show="type === 'b'">type===b </div>
    </div>
</template>
<script>
export default {
    name: 'vIf',
    data() {
        return {
            type: 'b'
        }
    }
}
</script>