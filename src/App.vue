
<script>
  import { local } from '../src/functions';

  import { RouterLink, RouterView } from 'vue-router';
  export default{
    data(){
    return{
      
    };
  },
      methods: {
        routeChanged(to){
  
  if(!local.isset('user_token')){
    this.$router.replace('/login');
  }else if(to == '/login'){
    this.$router.replace('/dashboard');
  }
      }
  },
  
  watch:{
  $route (to){
  this.routeChanged(to.path);
  }
  },
  
  created(){
  this.routeChanged(this.$route.path);
  }
    }
  </script>

<template>
  <RouterView />
</template>

<style>
  body{
    background: #d6d6d6 !important;
  }
</style>
