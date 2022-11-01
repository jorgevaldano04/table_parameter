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
     <td><button type="button" class="btn btn-warning">Detail</button></td>
   </tr>  
 </tbody>
   </table>
   <nav aria-label="Page navigation example">
  <ul class="pagination justify-content-end">
    <li class="page-item disabled">
      <a class="page-link" href="#" tabindex="-1">Sebelumnya</a>
      
    </li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item">
      <a class="page-link" href="#">Selanjutnya</a>
    </li>
  </ul>
</nav>


  
   </template>
   
   <script>
      export default {
     name: 'parameter-table',
     props: {
       parameters: Array,
     },
     
   }
   </script>
   
   <style>
   
   </style>