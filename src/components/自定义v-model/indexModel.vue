<template>
    <div>
        v-model:
        <inp v-model="message" /><br><br>
        自定义v-model:
        <inp :value="message" @input="message = $event" /><br><br>
        message :
        {{ message }}
        <br><br><br>
        <check v-model="checked" />
        <check :checked="checked" @change="checked = $event" />{{ checked }}
    </div>
</template>
<script>
import inp from './inp.vue';
import check from './check.vue';
export default {
    name: 'indexModel',
    components: { inp, check },
    data() {
        return {
            message: 'sun',
            checked: true
        }
    }
}
</script>