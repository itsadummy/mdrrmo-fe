<template>
  <div class="dashboard">
    <Nav/>
        <section class="main-content columns is-fullheight">
            <Sidebar/>
           
           <div class="container column is-7 mt-4">
              
              <Graph/>

              <Dailyforecast class="mt-3"/>

              <Hourlyforecast class="mt-3"/>

           </div>

            <div class="container column is-3">
              <Lists/>
            </div>
        </section>
  </div>
</template>

<script>
import Nav from '../components/Nav'
import Sidebar from '../components/Sidebar'
import Graph from '../components/Graph'
import Dailyforecast from '../components/Dailyforecast'
import Hourlyforecast from '../components/Hourlyforecast'
import Lists from '../components/Lists'
export default {
    name: "Dashboard",
    components: {
        Nav,
        Sidebar,
        Graph,
        Dailyforecast,
        Hourlyforecast,
        Lists
        }
}
</script>

<style scoped>


</style>