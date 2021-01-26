<template>
<div class="card">
    <div class="card-header">
    <div class="columns">
        <div class="column is-10">
        </div>
        <div>
        <b-button-group class="btn-group btn-group-sm mt-2">
            <b-button class="btn btn-outline-secondary" variant="white">Day</b-button>
            <b-button class="btn btn-outline-secondary text-white" variant="secondary">Week</b-button>
            <b-button class="btn btn-outline-secondary" variant="white">Mon</b-button>
            <b-button class="btn btn-outline-secondary text-white" variant="secondary">Year</b-button>
        </b-button-group>
    </div>
    </div>
    </div>
    <div class="card-content">
    <div class="content">
            <Chart v-if="ChartConfig.labels.length" 
            :line-data="ChartConfig" :chart-options="options"
            :style="{height: '290px'}"/>  
        </div>
    </div>
</div>

</template>

<script>
import Chart from '../components/Chart.js'
//import axios from 'axios'
export default {
    components: {
        Chart,
    },
    data() {
        return {
            ChartConfig: {
                labels: [],
                level: [],
                datasets: [
                    {
                    data: [], 
                    backgroundColor: 'rgba(255, 0, 0, 0.2)',
                    "fill": false,
                    
                    borderColor: 'lightpink',
                    pointBackgroundColor: 'red',
                    borderWidth: 1,
                    pointBorderColor: 'red',
                    label: "Amount "
                    },
                    {
                    data: [], 
                    backgroundColor: 'rgba(0, 0, 255, 0.2)',
                    "fill": false,
                    borderColor: 'lightblue',
                    pointBackgroundColor: 'lightblue',
                    borderWidth: 1,
                    pointBorderColor: 'lightblue',
                    label: "Level "
                   
                    },
                ]   
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                legend: {
                  position: 'bottom'
                },
                layout: {
                  padding: {
                    left: 25,
                    right: 0,
                    bottom: 0
                  }
                },
                tooltips: {
                    mode: 'index',
                    intersect: false,
                },
                hover: {
                    mode: 'nearest',
                    intersect: true,
                },
                scales: {
                    xAxes: [{
                    display: true,
                    scaleLabel: {
                        display: true,
                        labelString: 'Day'
                    }
                    }],
                    yAxes: [{
                    display: true,
                    scaleLabel: {
                        display: true,
                        labelString: 'Value per ticks'
                    }
                    }]
                }
            },
        }
    },
}
</script>

<style scoped>
  .btn-group{
    float: right;
  }
</style>