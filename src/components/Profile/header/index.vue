<template>  
<div class='profileHeader'>
  <div class='headerImages'>
    <div class='mainProfileImage'><img  class='mainProfileImage' :src='images[0]'></img></div>
    <div class='secondaryImages'>
      <div class='secondaryProfileImage'><img class='secondaryProfileImage' :src='images[1]'></img></div>
      <div class='secondaryProfileImage'><img class='secondaryProfileImage' :src='images[2]'></img></div>
      <div class='secondaryProfileImage'><img class='secondaryProfileImage' :src='images[3]'></img></div>
    </div>
  </div>
  <div class='headerInfo'>
    <span class='profileName'>{{name}}</span>
    <span class='profileAge'>{{age}}</span>
    <div>
      <span class='profileLocation'>{{location}}</span>
    </div>
  </div>
</div>
</template>
<script>
  export default {
    data() {
      return {
        images: [
          'https://s-media-cache-ak0.pinimg.com/564x/29/fa/14/29fa1441f2a0446e9aa45cee74495a83.jpg',
          'http://cdn2-www.dogtime.com/assets/uploads/gallery/30-impossibly-cute-puppies/impossibly-cute-puppy-8.jpg',
          'http://cdn1-www.dogtime.com/assets/uploads/gallery/30-impossibly-cute-puppies/impossibly-cute-puppy-2.jpg',
          'http://cdn3-www.dogtime.com/assets/uploads/gallery/30-impossibly-cute-puppies/impossibly-cute-puppy-21.jpg',
        ],
        name: 'Tabitha',
        age: 24,
        location: 'San Francisco, CA',
      };
    },
    computed: {
      isCurrentUser() {
        return this.$route.params.userId === this.userId;
      },
    },
    props: [
      'isCurrentUser',
    ],
  };
</script>
<style> 
  .profileHeader {
    display: flex;
  }
  .mainProfileImage {
    flex: 5;
    height: 300px;
    width: 300px;
  }
  .secondaryImages {
    flex: 3;
    flex-direction: collumn;
  }
  .secondaryProfileImage {
    flex: 1;
    height: 100px;
    width: 100px;
  }
  .headerImages {
    flex: 5;
    display: flex;
  }
  .headerInfo {
    flex: 5;
    display: flex;
  }
</style>