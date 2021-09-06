<template>
   <div>
   <NavBar/>
   <div class="container">
    <div class="row">
      <div class="col-md-12">
        
         <h4 class="mt-4 title" >Usuarios</h4>
         <NuxtLink to="/" class="btn btn-outline-primary">REGRESAR...</NuxtLink>

          
         <div class="mt-2 card" v-for="user of users" :key="user.id" style="width:350px;height:auto">
            <img :src="`${user.picture.thumbnail}`" class="card-img-top" alt="..." style="width:100%;height:auto">
            <div class="card-body">
               <h5 class="card-title"><b>{{user.name.last}} {{user.name.first}}</b></h5>
               <h5 class="card-title"><b>Celular</b>: {{user.cell}}</h5>
               <h5 class="card-title"><b>Correo</b>: {{user.email}}</h5>
               <h5 class="card-title"><b>Ciudad</b>: {{user.location.city}}</h5>
            </div>
         </div>
      </div>
    </div>
   </div> 
   </div>
</template>
<script>
import axios from 'axios';
export default {
    name:'User',
    components: {

   },
   data() {
    return {
      users:[]
    };
  },
  mounted(){
    axios.get('https://randomuser.me/api/?results=8')
     .then(response=>{
        this.users= response.data.results;
        console.log(this.users); 
     }).catch((err)=>{
        console.log(err);
     })  
  }
}
</script>
<style scoped>
 .title{
   background-color:darkblue;
   padding:30px;
   text-align:center;
   color:white;
   font-size:25px;
   font-weight:bold;
 }
 .card{
    box-shadow: 10px 10px 10px #aaa; 
 } 
</style>