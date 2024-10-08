<template>
    <div class="boxx">
        <div :class="{ blue: isBlue, bigger: isBigger }">111</div>
        <div :class="['red', 'bigger']">222</div>
        <div :style="testObj">333</div>
    </div>
</template>
<script>
export default {
    name: 'classUse',
    data() {
        return {
            isBlue: true,
            isBigger: true,
            red: 'isRed',
            testObj: {
                fontSize: '50px',
                color: "green",
            }
        }
    }
}
</script>
<style scoped>
.blue {
    color: blue;

}

.bigger {
    font-size: 40px;
}

.red {
    color: red;
}
</style>
