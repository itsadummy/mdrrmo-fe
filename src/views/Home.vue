<template>
  <div id="home">

      <div class="container">
      <div class="row">
        <div class="col-8 mx-auto mt-5">
            <b-card class="text-center">
                <img id="logo" src="../assets/mdrrmo_logo.png"> <hr>
                    <h4>Municipal Disaster Risk Reduction Management Office</h4>
                    <p>Santa Cruz, Laguna </p>
                        <form>
                            <form-group class="mb-2">
                                <b-icon class="h4" icon="person-circle"></b-icon> &nbsp;
                                <input type="text" placeholder="Username...">
                            </form-group> <br> <br>
                            <form-group class="mb-2">
                                <b-icon class="h4" icon="lock-fill"></b-icon> &nbsp;
                                <input type="password" placeholder="Password...">
                            </form-group>
                        
                        <div class="form-group d-flex justify-content-center">
                            <button @click="loginAcc()" class="btn btn-primary my-3"> Login </button>
                            <!-- <v-btn @click="loginUser(user)">Login</v-btn>-->
                        </div>
                        <div class="form-group justify-content-center">
                            <router-link to="#">Forgot password?</router-link>
                        </div>
                    </form>
            </b-card>

            <footer class="footer text-center">
                <p>College of Computer Studies <br>
                Laguna State Polytechnic University <br>
                2020</p>
            </footer>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
    name: 'Home',
    methods:{
        loginAcc(){
            this.$router.push("/Dashboard")
        } 
    }
}
</script>

<style scope>
    #logo{
        height: 140px;
    }
    .footer{
      margin-top: 19px;
      color: darkgrey;  
    }
</style>