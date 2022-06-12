<template>
    <select v-model="sortBy">
        <option value="date">Sort by date</option>
        <option value="likes">Sort by likes</option>
    </select>

    <p>{{ sortBy }}</p>
    <ul>
        <TweetsItem v-for="item in items" :key="item.id" :item="item"/>
    </ul>
</template>

<script>
import { ref}  from 'vue'
import TweetsItem from '@/components/TweetsItem.vue'

export default {
    components: {TweetsItem},
    props: {
        items: {
            type: Array,
            required: true,
        }
    },
    setup() {
        const sortBy = ref('date')
        return { sortBy }
    }
}
</script>
