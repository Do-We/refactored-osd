<template>  
<div >
  <button v-on:click='sendMessage'>Message Her</button>
  <h3>Bio</h3>
  <div class='profileBio'>{{bio}}</div>
</div>
</template>
<script>
  export default {
    data() {
      return {
        bio: 'this is why im awesome this is why im awesome this is why im awesome this is why im awesome this is why im awesome this is why im awesome this is why im awesome this is why im awesome',
      };
    },
    computed: {

    },
    props: [

    ],
    methods: {
      sendMessage() {
        console.log(`i want to open the message dropdownn and send ${this.$route.params.userId} a message`);
      },
    },
  };
</script>
<style> 

</style>