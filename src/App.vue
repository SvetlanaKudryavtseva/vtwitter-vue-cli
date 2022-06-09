<template>
<div class="wrapper">
  <!-- header -->
  <div class="wrapper-content">
    <div class="container">
      <TweetsList />
    </div>
  </div><!-- end wrapper-content -->
  <!-- footer -->
</div><!-- end wrapper -->

</template>
<script>
import TweetsList from '@/components/TweetsList'

export default {
  components: {TweetsList},
}
</script>
