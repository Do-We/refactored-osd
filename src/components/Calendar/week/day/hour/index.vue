<template>
  <div>
    <event-block :hour='timeSlot[1]'></event-block>
  </div>
</template>


<script>
  import EventBlock from './eventblock.vue';

  export default {
    components: {
      EventBlock
    },
    data() {
      return {

      }
    },
    created () {
    },
    props: [
      'timeSlot'
    ],
  }
</script>
