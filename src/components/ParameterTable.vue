<template>
<tr>
  <div class="form-row">
    <div class="col">
      <input class="form-control mr-sm-2" type="search" placeholder="Fillter Nama Parameter" aria-label="Search">
    </div>
    <div class="col">
      <input class="form-control mr-sm-2" type="search" placeholder="Fillter Value" aria-label="Search">
    </div>
  </div>
</tr>


<table class="table table-striped">


     <thead class="thead-light">
       <tr class="table-secondary"> 
         <th scope="col">No</th>
         <th scope="col">Nama Parameter</th>
         <th scope="col">Value</th>  
         <th scope="col">Aksi</th>
       </tr>

     </thead>
     <tbody>
   <tr v-for="(parameter, index) in parameters" :key="parameter.id"> 
     <td>{{ index + 1 }}</td>
     <td>{{ parameter.name }}</td>
     <td>{{ parameter.username }}</td>
     <td><ButtonDetail :visible="false" variant="success">email: {{ parameter.email }}</ButtonDetail></td>
   </tr>  
 </tbody>
</table>
   </template>
   
   <script>
import ButtonDetail from './ButtonDetail.vue';

export default {
  name: 'parameter-table',
  props: {
       parameters: Array,
     },
     components:{
      ButtonDetail
     }
   }
   </script>
   
   <style>
   
   </style>