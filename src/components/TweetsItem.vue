<template>
    <li>
        <img style="width:30px; height:30px;" :src="item.avatar" alt="">
        <p>{{item.body}}</p>
        <p>{{item.date}}</p>
    </li>
</template>
<script>
export default {
    props: {
        item: {
            type: Object,
            required: true,
        }
    }
}
</script>