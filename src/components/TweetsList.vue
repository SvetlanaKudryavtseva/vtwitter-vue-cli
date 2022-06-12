<template>
    <select v-model="sortBy">
        <option value="date">Sort by date</option>
        <option value="likes">Sort by likes</option>
    </select>

    <!-- <p>{{ sortBy }}</p> -->
    <ul>
        <TweetsItem v-for="item in sortedItems" :key="item.id" :item="item"></TweetsItem>
    </ul>
</template>

<script>
import { ref, computed}  from 'vue'
import TweetsItem from '@/components/TweetsItem.vue'

export default {
    components: {TweetsItem},
    props: {
        items: {
            type: Array,
            required: true,
        }
    },
    setup( {items} ) {
        const sortBy = ref('date')

        const sortedItems = computed (() => {
            return items.sort((a, b ) => {
                if (a[sortBy.value] > b[sortBy.value]) return -1
                if (a[sortBy.value] < b[sortBy.value]) return 1
        })
        })
        return { sortBy, sortedItems }
    }
}
</script>
