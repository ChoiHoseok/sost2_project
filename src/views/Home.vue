<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <BarChart v-bind="test1"></BarChart>
    <LineChart v-bind="test2"></LineChart>
    <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
  </div>
</template>

<script>
import BarChart from '@/components/BarChart.vue'
import LineChart from '@/components/LineChart.vue'

export default{
  data: function(){
    return{
      test1:{
        columns: [
              ["data1", 30, 200, 100, 170, 150, 250],
              ["data2", 130, 100, 140, 35, 110, 50]
          ]
      },
      test2:{
        columns: [
              ["data1", 30, 200, 100, 170, 150, 250],
              ["data2", 130, 100, 140, 35, 110, 50]
          ]
      },
      test3:{
        columns: [
              ["data1", 30, 200, 100, 170, 150, 250],
              ["data2", 130, 100, 140, 35, 110, 50]
          ]
      }
    }
  },
  components:{
    BarChart,
    LineChart
  }
}

</script>
