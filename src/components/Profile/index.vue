<template>  
<div>
  <profile-header :is-current-user='isCurrentUser'></profile-header>
  <profile-body></profile-body>
</div>
</template>
<script>
  import ProfileHeader from './header';
  import ProfileBody from './body';

  export default {
    data() {
      return {
        userId: 'asdf',
      };
    },
    computed: {
      isCurrentUser() {
        return this.$route.params.userId === this.userId;
      },
    },
    components: {
      ProfileHeader,
      ProfileBody,
    },
  };
</script>
<style> 
</style>