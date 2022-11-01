<template>
  <div id="app">
    <div class="container">
      <h2 class="mb-4" style="color:#008080;">Daftar Parameter</h2> 
      <parameter-table :parameters='parameters'/>
    </div>
  </div>
</template>

<script>
import ParameterTable from '@/components/ParameterTable.vue'


export default {
  name: "App",
  data() {
    return {
      parameters: []
    };
  },
  mounted() {
    this.getParameters();
  },
  components: {
    ParameterTable
  },
  methods: {
    async getParameters() {
      try {
        const response = await fetch(
          "https://jsonplaceholder.typicode.com/users"
        );
        const data = await response.json();
        this.parameters = data;
      } catch (error) {
        console.error(error);
      }
    }, 
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>