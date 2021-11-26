<template>
  <h1>Home</h1>
</template>

<script>
export default {
    name:'Home',
    data(){},
    methods:{},
    mounted(){
        let user = localStorage.getItem("user-info");
        
        if(!user){
            this.$router.push({name : 'SignUp'})
        }
    }
}
</script>

<style>

</style>