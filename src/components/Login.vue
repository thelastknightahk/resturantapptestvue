<template>
 <img src="../assets/optimus.jpeg"  class="logo" >
  <h1>Login</h1>
  <div class="login" >
      
      <input type="text" v-model="email" placeholder="Enter Email">
      <input type="password" v-model="password" placeholder="Enter Password">
      <button v-on:click="login()" >Login</button>
      <p>   
          <router-link to="/sign-up" >Sign Up</router-link>
      </p>
  </div>
</template>

<script>
import axios from 'axios'
export default {
 name:'Login',
 data(){
        return {
            email:'',
            password:''
        }
    },
    methods:{
       async login(){
           let loginResult = await axios.get("http://localhost:3000/users?email=aung@gmail.com&password=aungmail@");
           
             console.warn('Login  '+loginResult)
        }
    },
    mounted(){
        // let user = localStorage.getItem("user-info");
        // if(user){
        //     this.$router.push({name : 'Home'})
        // }
    }
}
</script>

<style>
.logo{
     width: 200px;
 }
  
</style>