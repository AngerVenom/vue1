<template>
<div class="todo">
<!-- Input de usuario e input de contraseña -->
    <span v-if="accedio==true">
      <h1> Educación Continua y CAADI</h1>
      <br >
      <div class="estilos">
        <form action class="form">
          <label>Usuario</label>
          <input type="text" class="form-control" v-model="user">
          <br >
          <label >Contraseña</label>
          <input type="text" class="form-control" v-model="pass">
        </form>
        <br >
      <!-- Botón de acceder -->
      <button type="button" class="btn btn-primary" v-on:click="acceder()">Acceder</button>
    </span>
<!-- Visualizar vista de maestro (lista de minutas) -->
      <span v-if="lista==true">
        <MinutasMaestros />
      </span>
    </div>
</div>
</template>
<!-- No hay funciones dentro de Login -->
<script>
import MinutasMaestros from './MinutasMaestros.vue'
  export default {
    components:{
      MinutasMaestros
    },
    data(){
      return{
        user: "",
        pass: "",
        accedio: true,
        lista: false
        }
      },
    methods:{
    /* Función de login: deshabilita el login (accedio) y habilita el contenido del maestro (lista) */
      acceder(){
        if (this.user == "user1" && this.pass==123){
          this.accedio = false;
          this.lista = true;
        }
      }
    }
  }
</script>

<style>
  .todo{
    margin-top:100px;
  }
  .estilos{
    width: 200px;       
          height: 200px;
          margin: 0 auto;
  }
</style>