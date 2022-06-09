<template>
<div class="wrapper">
  <!-- header -->
  <div class="wrapper-content">
    <div class="view">
      <div class="container">
        <TweetsList />
      </div><!-- end container -->
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
