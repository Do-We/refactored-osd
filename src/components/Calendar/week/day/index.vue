<template>
  <div>
    <table class='dayTable'>
      <thead>
        <tr>
          <th>{{today}}</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for='hour in hours'>
          <td @click.prevent='bookTimeslot(today, hour)'>
            <hour :time-slot='[today, hour]' v-if='selected === JSON.stringify([today, hour])'></hour>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import hour from './hour';
  export default {
    components: {
      hour,
    },
    props: [
      'today',
      'selected'
    ],
    created() {
      let temp = [];
      for(let i = 9; i <= 23; i++) {
        temp.push(i);
      };
      this.$data.hours = temp;
    }, 
    data () {
      return {
        hours: null,
      }
    },
    methods: {
      bookTimeslot (day, hour) {
        this.$parent.$emit('selected', JSON.stringify([day, hour]));
      },
    },
  }
</script>


<style>
  table.dayTable {
    width: 10%;
    background-color: #ffffff;
    border-collapse: collapse;
    border-right: 1px solid black;
    color: #000000;
    float: left;
    text-align: center;
  }

  table.dayTable td, table.dayTable th {
    padding: 3px;
    height: 20px;
  }

  table.dayTable td:hover {
    background: #F1F1F1;
    cursor: default;
    box-shadow: 1px 2px 2px #705848;
  }

  table.dayTable th {
    cursor: default;
  }

  table.dayTable thead {
    background-color: #white;
  }
</style>


