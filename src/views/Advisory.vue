<template>
  <div class="advisory">
    <Nav/>
        <section class="main-content columns is-fullheight">
            <Sidebar/>

            <div class="container column is-10">
<div class="section has-text-centered">

  <div class="card is-hidden1">
    <div class="card-header"><p class="card-header-title">SMS Distribute</p></div>
    <div class="card-content"><div class="content"><button class="button is-danger">    Perform Task    </button></div></div>
    <hr>
    <h4>SMS LOGS</h4>
    <div class="card-content">
        <div class="content">
            
            <table class="table table-striped table-sm table-light table-hover mt-1"> 
            <thead id="thead">
                <tr>
                    <th >Type</th>
                    <th >Status</th>
                    <th >Measurement</th>
                </tr>
                </thead>
                <tbody>
                <tr v-for="rainfall in rainfallsData" v-bind:key="rainfall" :style="{height: '20px'}">
                    <td :style="{width: '250px'}">{{rainfall.level}}</td>
                    <td :style="{width: '250px'}">{{rainfall.amount}}</td>
                    <td :style="{width: '500px'}"> {{rainfall.timestamp}}</td>
                </tr>
                </tbody>
            </table> 
        </div>
    </div>
  </div>
  <br />  


  <nav class="pagination is-centered" role="navigation" aria-label="pagination">
    <a class="pagination-previous" @click="prevPage">Previous</a>
    <a class="pagination-next" @click="nextPage">Next page</a>
  </nav>

  
</div>
</div>
        </section>
  </div>
</template>

<script>
import Nav from '../components/Nav'
import Sidebar from '../components/Sidebar'
export default {
    name: "Advisory",
    components: {
        Nav,
        Sidebar
    },

    data() {
        return {
            rainfalls:[],
            currentPage: 1,
            pageSize: 4,
            totalRows: 0
        }
    },
    created:function() {
        //fetch('http://127.0.0.1:8000/api/appapi/') api sa backend koto
        fetch('https://mdrrmo-scl.herokuapp.com/api/v1/rainfal')
        .then(res => res.json())
        .then(res => {
        this.rainfalls = res;
        })
  },
    methods:{
    
        nextPage:function() {
            if((this.currentPage*this.pageSize) != this.rainfalls.length) this.currentPage++;
        },
        prevPage:function() {
            if(this.currentPage > 1) this.currentPage--;
        }
    },
    
  computed:{
    rainfallsData:function() {
      return this.rainfalls.filter((row, index) => {
        let start = (this.currentPage-1)*this.pageSize;
        let end = this.currentPage*this.pageSize;
        if(index >= start && index < end) return true;
      });
    }
  }
}
</script>

<style scoped>


</style>