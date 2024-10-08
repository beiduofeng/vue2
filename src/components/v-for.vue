<template>
    <div>
        <ul>
            <li v-for="(item, index) in userList" :key="item.id">{{ index }} -- {{ item.name }} : {{
                item.age }}</li>
        </ul>
        <ul>
            <li v-for="( value, key, index) in todayFood" :key="key"><span>
                    {{ `${index} --${key} --${value} ` }}
                </span></li>
        </ul>
    </div>
</template>
<script>
export default {
    name: 'v-for',
    data() {
        return {
            userList: [
                { id: 1, name: 'a', age: 10 },
                { id: 2, name: 'b', age: 11 },
                { id: 3, name: 'c', age: 12 }
            ],
            todayFood: {
                breakfastFood: '包子',
                lunchFood: '地锅鸡',
                dinnerFood: '炒菜'
            }
        }
    }
}
</script>