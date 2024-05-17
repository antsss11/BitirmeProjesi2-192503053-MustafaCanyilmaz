<template>



<div> 
      <canvas ref="chartCanvas"></canvas>
    </div>

</template>
  
  <script>
  import { Chart, registerables } from 'chart.js';
  
  export default {
    mounted() {
      this.createChart();
    },
    methods: {
      createChart() {
        Chart.register(...registerables);
  
        const ctx = this.$refs.chartCanvas.getContext('2d');
        new Chart(ctx, {
          type: 'polarArea',
          data: this.chartData,
          options: {}
        });
      }
    },
    data() {
      return {
        chartData: {
       
            labels: ['Kırmızı', 'Yesil', 'Sarı', 'Gri', 'Mavi'],
          datasets: [{
            label: 'My First Dataset',
            data: [11, 16, 7, 3, 14],
            backgroundColor: [
              'rgb(255, 99, 132)',
              'rgb(75, 192, 192)',
              'rgb(255, 205, 86)',
              'rgb(201, 203, 207)',
              'rgb(54, 162, 235)'
            ]
          }]
        }
      };
    }
  };
  
  
  </script>

<style>
.h2{
    display: grid;
    margin-left:90px;
    color: #beb6b6a4;
    margin-top:-40px;
  }

 

</style>