<template>
    <ul>
        <TweetsItem v-for="item in items" :key="item.id" :item="item"/>
    </ul>
</template>

<script>
import TweetsItem from '@/components/TweetsItem.vue'

export default {
    components: {TweetsItem},
    props: {
        items: {
            type: Array,
            required: true,
        }
    }
}
</script>
