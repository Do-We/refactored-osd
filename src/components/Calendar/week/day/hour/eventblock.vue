<template>
  <div class='tooltip'>
    <button @click='editStart(-1)'> 
      <svg width="10px" height="3px" viewBox="426 569 10 3" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
        <!-- Generator: Sketch 42 (36781) - http://www.bohemiancoding.com/sketch -->
        <desc>Created with Sketch.</desc>
        <defs></defs>
        <rect id="minus" stroke="none" fill="#666666" fill-rule="evenodd" x="426" y="569" width="10" height="3" rx="1"></rect>
      </svg>
    </button>      
      {{ start }} 
    <button @click='editStart(1)'>
      <svg width="10px" height="11px" viewBox="490 566 10 11" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
        <!-- Generator: Sketch 42 (36781) - http://www.bohemiancoding.com/sketch -->
        <desc>Created with Sketch.</desc>
        <defs></defs>
        <g id="Plus" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd" transform="translate(490.000000, 566.000000)">
            <rect id="Rectangle-17" fill="#666666" x="0" y="4" width="10" height="3" rx="1"></rect>
            <rect id="Rectangle-17" fill="#666666" transform="translate(5.000000, 5.500000) rotate(90.000000) translate(-5.000000, -5.500000) " x="0" y="4" width="10" height="3" rx="1"></rect>
        </g>
      </svg> 
    </button>
    <p> to </p>
    <button @click='editEnd(-1)'> 
      <svg width="10px" height="3px" viewBox="426 569 10 3" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
        <!-- Generator: Sketch 42 (36781) - http://www.bohemiancoding.com/sketch -->
        <desc>Created with Sketch.</desc>
        <defs></defs>
        <rect id="minus" stroke="none" fill="#666666" fill-rule="evenodd" x="426" y="569" width="10" height="3" rx="1"></rect>
      </svg>
    </button>  
       {{ end }} 
    <button @click='editEnd(+1)'>
      <svg width="10px" height="11px" viewBox="490 566 10 11" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
        <!-- Generator: Sketch 42 (36781) - http://www.bohemiancoding.com/sketch -->
        <desc>Created with Sketch.</desc>
        <defs></defs>
        <g id="Plus" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd" transform="translate(490.000000, 566.000000)">
            <rect id="Rectangle-17" fill="#666666" x="0" y="4" width="10" height="3" rx="1"></rect>
            <rect id="Rectangle-17" fill="#666666" transform="translate(5.000000, 5.500000) rotate(90.000000) translate(-5.000000, -5.500000) " x="0" y="4" width="10" height="3" rx="1"></rect>
        </g>
      </svg> 
    </button>
  </div>
</template>

<script>
  export default {
    created () {
    },
    data () {
      return {
        start: this.$props.hour,
        end: this.$props.hour + 1
      }
    },
    props: [
      'hour'
    ],
    methods: {
      editStart (time) {
        this.$data.start += time
      },
      editEnd (time) {
        this.$data.end += time
      },
    }
  }
</script>

