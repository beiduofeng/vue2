<template>
    <div>
        <a :href="url">
            <slot>默认展示的内容</slot>
        </a>
    </div>
</template>

<script>
export default {
    name: 'son',
    props: ["url"],
    data() {
        return {}
    }
}
</script>