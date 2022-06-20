<template>
  <!--Logos-->
  <div class="todo">
  <div class="estilocabecera">
    <span v-if="cabecera == true">
      <img src="https://www.uanl.mx/wp-content/uploads/2020/08/Escudo-UANL-color.png" class="uanl">
      <img src="https://pngimage.net/wp-content/uploads/2018/06/fime-logo-png-1.png" class="fime">
    </span>
  </div>    
  <!-- Datos del maestro de la lista de minutas -->
  <div class="ajuste">
    <span v-if="listado==true">
      <div class="datos">
        Nombre del Maestro: {{nombre_ma}}<br >
        Teléfono: {{telefono_ma}}<br >
        Correo: {{correo_ma}}<br >
      </div>
      <br >
      <br >
    <!-- Listado de minutas disponibles (vista al maestro) -->
      
      <br>
      <br>
      <div class="list-group listado">
        <h1 class="text-start">Minutas activas</h1>

        <a href="#" class="list-group-item list-group-item-action" aria-current="true">
          <div class="d-flex w-100 justify-content-between">
            <h5 class="mb-1">Módulo 1: Matemáticas</h5>
            <button type="button" class="btn btn-success editar" v-on:click="abrir()">Editar</button>
          </div>
          <p class="mb-1">Técnico en Mecatrónica</p>
          <small>Domingos de 09:00 a 14:00 hrs</small>
        </a>

        <a href="#" class="list-group-item list-group-item-action">
          <div class="d-flex w-100 justify-content-between">
            <h5 class="mb-1">Módulo 9: Excel II</h5>
            <button type="button" class="btn btn-success editar" v-on:click="abrir()">Editar</button>
          </div>
          <p class="mb-1">Técnico en Informática Computacional</p>
          <small class="text-muted">Sábados de 09:00 a 14:00 hrs</small>
        </a>

          <a href="#" class="list-group-item list-group-item-action">
            <div class="d-flex w-100 justify-content-between">
              <h5 class="mb-1">Módulo 8: Interfaces Gráficas</h5>
              <button type="button" class="btn btn-success editar" v-on:click="abrir()">Editar</button>
            </div>
            <p class="mb-1">Técnico en Mecatrónica</p>
            <small class="text-muted">Sábados de 14:30 a 19:30 hrs</small>
          </a>
      </div>
      <br >
      <button type="button" class="btn btn-success" v-on:click="salir()">Salir</button>
  </div>
      
  </span>
  <!-- Datos generales de una minuta -->
  <div v-if="datosMinuta==true" class="ajuste">
    <DatosMinuta />
    <!-- Botones para regresar -->
      <div class="d-grid gap-2 d-md-flex justify-content-md-end">
        <button class="btn btn-danger" type="button" v-on:click="regresarListado()">Regresar</button>
        <button class="btn btn-success me-md-2" type="button" v-on:click="capasis()">Aceptar</button>

      </div>
  </div>
  <!-- Complemento de asistencia -->
  <div class="ajuste">
    <span v-if="capturar == true">
      <br >
      <div class="d-grid gap-2 d-md-flex justify-content-md-start">
      <button type="button" class="btn btn-danger" v-on:click="cancelar()">Cancelar</button>
      <button type="button" class="btn btn-success" v-on:click="continuarpra()">Continuar</button>
      </div>
      <Asistencia />
    </span>
  </div>
  <!-- Complemento de Prácticas -->
  <div class="ajuste">
    <span v-if="capturarpra == true">
      <br >
      <div class="d-grid gap-2 d-md-flex justify-content-md-start">
      <button type="button" class="btn btn-danger" v-on:click="regresarpra()">Regresar</button>
      <button type="button" class="btn btn-success" v-on:click="continuartar()">Continuar</button>
      </div>
      <Practicas />
    </span>
  </div>
  <!-- Complemento de Tareas -->
  <div class="ajuste">
    <span v-if="capturartar == true">
      <br >
      <div class="d-grid gap-2 d-md-flex justify-content-md-start">
      <button type="button" class="btn btn-danger" v-on:click="regresartar()">Regresar</button>
      <button type="button" class="btn btn-success" v-on:click="continuar4ses()">Continuar</button>
      </div>
      <Tareas />
    </span>
  </div>
  <!-- Complemento de la cuarta sesión -->
  <div class="ajuste">
    <span v-if="cuartases == true">
      <br >
      <div class="d-grid gap-2 d-md-flex justify-content-md-start">
      <button type="button" class="btn btn-danger" v-on:click="regresar4ses()">Regresar</button>
      <button type="button" class="btn btn-success"  v-on:click="continuarresf()">Continuar</button>
      </div>
      <Cuartasesion />
    </span>
  </div>
  <!-- Complemento de resultados finales -->
  <div class="ajuste">
    <span v-if="resultf == true">
      <br >
     <div class="d-grid gap-2 d-md-flex justify-content-md-start">
      <button type="button" class="btn btn-danger" v-on:click="regresarresf()">Regresar</button>
      <button type="button" class="btn btn-success" v-on:click="finalizar()">Finalizar</button>
      </div>
      <ResultadosFinales />
    </span>
  </div>
  </div>
</template>

<script>
/* Importación de componentes (datosMinuta) */
import DatosMinuta from "./DatosMinuta.vue"
import Asistencia from "./Asistencia.vue"
import Practicas from "./Practicas.vue"
import Tareas from "./Tareas.vue"
import Cuartasesion from "./Cuartasesion.vue"
import ResultadosFinales from "./ResultadosFinales.vue"
  export default {
    name: 'App',
    components:{
      DatosMinuta,
      Asistencia,
      Practicas,
      Tareas,
      Cuartasesion,
      ResultadosFinales
    },
    /* Variables */
      data(){
        return{
          listado: true,
          datosMinuta: false,
          capturar: false,
          cancelarpra: false,
          cabecera: false,
          capturartar: false,
          cuartases: false,
          resultf: false
        }
     },
  /* Funciones */
    methods:{
    /* abre los datos de la minuta */
      abrir(){
        this.listado = false;
        this.datosMinuta = true;
        this.cabecera = true;
      },
    /* Salir del sistema */
      salir(){
        window.location.reload();
      },
    /* Botón de regresar a la lista estando en los datos de una minuta */
      regresarListado(){
        this.datosMinuta = false;
        this.listado = true;
        this.cabecera = false;
      },
    /* Acceso a la captura de asistencia */
      capasis(){
        this.capturar = true;
        this.listado = false;
        this.datosMinuta = false;
        this.cabecera = true;
      },
    /* Regresa a los datos generales de la minuta */
      cancelar(){
        this.capturar = false;
        this.listado = false;
        this.datosMinuta = true;
        this.cabecera = true;
      },
    /* Continuar con la captura de prácticas */
      continuarpra(){
        this.capturar = false;
        this.capturarpra = true;
        this.cabecera = true;
      },
    /* Regresa a la captura de asistencia */
      regresarpra(){
        this.capturar = true;
        this.capturarpra = false;
        this.cabecera = true;
      },
    /* Capturar califiaciones de tareas */
      continuartar(){
          this.capturartar = true;
          this.capturarpra = false;
          this.cabecera = true;
      },
    /* Regresamos a las prácticas */
      regresartar(){
        this.capturartar = false;
        this.capturarpra = true;
        this.cabecera = true;
      },
    /* Capturar la cuarta sesión */
      continuar4ses(){
        this.capturartar = false;
        this.cuartases = true;
        this.cabecera = true;
      },
    /* Regresar a la captura de tareas */
      regresar4ses(){
        this.capturartar = true;
        this.cuartases = false;
        this.cabecera = true;
      },
    /* Continuar con los resultados finales */
      continuarresf(){
        this.cuartases = false;
        this.resultf = true;
        this.cabecera = true;
      },
    /* Regresar a la cuarta sesión */
      regresarresf(){
        this.resultf = false;
        this.cuartases = true;
        this.cabecera = true;
      },
    /* Terminar de capturar minuta */
      finalizar(){
        this.resultf = false;
        this.listado = true;
        this.cabecera = false;
      }
    }
  }
</script>

<!-- Estilos CSS -->
<style>
  .todo{
    margin-top: 100px;
  }
  .datos{
      background: #1c7947;
      color: #ffF;
      text-align:left;
      width: 70%;
      max-width: 400px;       
      height: 100px;
      position: absolute;
      top:20%;
      right: 0px;
      margin-top: -100px;
      padding-left:20px;
      padding-top:10px;
  }
  .listado{
        width: 80%;       
        margin: 0 auto;
  }
  .est_salir{
        width: 200px;       
        height: 100px;
        
        top:20%;        
        margin-top: -100px;
  }
  .editar{
      width: 70px;       
      height: 40px;
  }
  .estilocabecera{
    max-width: 400px;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .ajuste{
    max-width: 400px;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
</style>
