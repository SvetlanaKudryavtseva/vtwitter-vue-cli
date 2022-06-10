<template>
<div class="wrapper">
  <!-- header -->
  <div class="wrapper-content">
    <div class="view">
      <div class="container">
        <Form @onSubmit="handleSubmit"/>
        <TweetsList :items="items" />
      </div><!-- end container -->
    </div>
  </div><!-- end wrapper-content -->
  <!-- footer -->
</div><!-- end wrapper -->
</template>

<script>
import { ref } from 'vue'
import Form from '@/components/Form';
import TweetsList from '@/components/TweetsList';

export default {
  components: { Form, TweetsList },
  setup(){
    const items = ref([
      {
          id: 1,
          avatar: `https://avatars.dicebear.com/api/male/1.svg`,
          body: "hello vue 3",
          likes: 12,
          date: new Date(Date.now()).toLocaleString(),
      },
      {
          id: 2,
          avatar: `https://avatars.dicebear.com/api/male/2.svg`,
          body: "hello world",
          likes: 5,
          date: new Date(Date.now()).toLocaleString(),
      },
    ])

    const handleSubmit = item => items.value.push(item)

    return {
      items,
      handleSubmit
    }
  }
// export default {
//   components: { Form, TweetsList },
//   data() {
//         return {
//             items: [{
//                     id: 1,
//                     avatar: `https://avatars.dicebear.com/api/male/1.svg`,
//                     body: "hello vue 3",
//                     likes: 12,
//                     date: new Date(Date.now()).toLocaleString(),
//                 },
//                 {
//                     id: 2,
//                     avatar: `https://avatars.dicebear.com/api/male/2.svg`,
//                     body: "hello world",
//                     likes: 5,
//                     date: new Date(Date.now()).toLocaleString(),
//                 },
//             ],
//         }
//     },
//     methods: {
//         handleSubmit(item){
//           this.items.push(item)
//         }

//     }
    
}
</script>
