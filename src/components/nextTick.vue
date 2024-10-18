<template>
    <div>
        <ul>
            <li v-for="(item, index) in fruits" :key="index">{{ item }}</li>
        </ul>
        <button @click="addList">添加</button>
    </div>
</template>
<script>
export default {
    name: 'nextTick',
    data() {
        return {
            fruits: ['apple', 'origin', 'banana']
        }
    },
    methods: {
        addList() {
            const li = document.createElement('li')
            li.innerHTML = 'pear'
            const ul = document.querySelector('ul')
            ul.appendChild(li)
            console.log('??');

        }
    }
}
</script>