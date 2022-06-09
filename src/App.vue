<template>
<div class="wrapper">
  <!-- header -->
  <div class="wrapper-content">
    <div class="view">
      <div class="container">
        <TweetsList :items="items" />
      </div><!-- end container -->
    </div>
  </div><!-- end wrapper-content -->
  <!-- footer -->
</div><!-- end wrapper -->
</template>

<script>
import TweetsList from '@/components/TweetsList.vue'
export default {
  components: {TweetsList},
  data() {
        return {
            items: [{
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
            ],
        }
    },
    methods: {
        onSubmit() {
            this.items.push({
                id: Math.round(Math.random() * 30),
                avatar: `https://avatars.dicebear.com/api/male/${Date.now()}.svg`,
                body: this.item,
                date: new Date(Date.now()).toLocaleString(),
            });
            // reset
            this.item = "";

        }
    },
}
</script>
