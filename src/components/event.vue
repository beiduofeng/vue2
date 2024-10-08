<template>
    <div>
        {{ num }} <button @click="addOne">+1</button><button @click="addThree(3, $event)">+3</button>
    </div>
</template>
<script>
export default {
    name: 'event',
    data() {
        return {
            num: 1
        }
    },
    methods: {
        addOne() {
            this.num += 1
        },
        addThree(p, event) {
            this.num += 3
            console.log('p', p);
            console.log('event', event);


        }
    }
}
</script>