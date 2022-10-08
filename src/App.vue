<template>
  <div class="mb-12">
    <Header />
    <hr>
  </div>
  
  <div class="container">
    <Formulario />
  </div>
  
  
</template>

<script>
  import Header from "./components/Header.vue"
  import Formulario from "./components/Formulario.vue"
  export default{
    components:{
      Header,
      Formulario
    },

  };
</script>
