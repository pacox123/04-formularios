<script>
  export default{
    data: () =>({
      proyecto: "",
      tipo: "",
      urgente: false,
      proyectos: [],
    }),
    methods:{
      registrarProyecto(){
        const proyecto = {
          proyecto: this.proyecto,
          tipo: this.tipo,
          urgente: this.urgente,
        };
        this.proyectos.push(proyecto);


        this.proyecto = "";
        this.tipo = "";
        this.urgente = false;

      },
    },
  };
</script>
<template>
    <form @submit.prevent="registrarProyecto">
        <div class="mb-3">
          <label class="form-label">Proyecto</label>
          <input v-model.trim="proyecto" type="text" class="form-control" required />
        </div>

        <div class="mb-3">
          <label class="form-label">Actividad</label>
          <select v-model.trim="tipo" required class="form-select">
            <option disabled  selected value= "">Selecciona un tipo de actividad</option>
            <option >Aplicacion Web con Vue.js</option>
            <option  >BackendServices con Node.js</option>
            <option  >App móvil con React Native</option>
          </select>
        </div>

        <div class="mb-3">
          <label  for="exampleInputPassword1" class="form-check-lable">Urgente</label>
          <input v-model="urgente" type="checkbox" class="form-ccheck-input" />
        </div>
        
        <button type="submit" class="btn btn-primary">Guardar</button>
      </form>
      <hr>

      <div class="table reponsive">
        <table class="table table-dark">
          <thead>
            <tr>
              <th>#</th>
              <th>Proyecto</th>
              <th>Tipo</th>
              <th>Urgente</th>
            </tr>
          </thead>

          <tbody>
            <tr>
              <td>1</td>
              <td>Laravel app</td>
              <td>Laravel</td>
              <td class="bg-danger">true</td>
            </tr>
          </tbody>
        </table>
      </div>
     
</template>