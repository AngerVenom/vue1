<template>
<span v-if="listaM == true">
<!--Apartado para agregar maestros-->
<h5>Agregar Maestro</h5>
<br>
<div class="input-group mb-3">
  <input type="text" class="form-control campos" placeholder="Número de empleado" aria-label="Recipient's username" aria-describedby="basic-addon2">
  <div class="input-group-append">
    
  </div>
</div>
<div class="input-group mb-3">
  <input type="text" class="form-control campos" placeholder="Nombre" aria-label="Recipient's username" aria-describedby="basic-addon2">
  <div class="input-group-append">
    
  </div>
</div>  
</div>

<button type="button" class="btn btn-success agregar" v-on:click="agregarMinuta1()">Agregar</button>
<br>
<br>
<br>
<!--Tabla de maestros-->
<div class="table-responsive">
  <table class="table table-bordered">
     <tr class="green">
      <th scope="col">#</th>
      <th scope="col">Maestro</th>

    </tr>
     <tr class="greenli">
      <td scope="col">1001</td>
      <td scope="col">Alejandra Pérez Robles</td>
    </tr>
    <tr class="greenli">
      <td scope="col">1002</td>
      <td scope="col">Hugo Abraham Avila Navarro</td>
    </tr>
    <tr class="greenli">
      <td scope="col">1003</td>
      <td scope="col">Maestro de Prueba</td>
    </tr>
  </table>
</div>
</span>
<span v-if="agregarM == true">
  <!--Apartado para agregar una minuta-->
  <h5>Agregar Oferta</h5>
  <br >
  <div class="contenedor">
  <div class="list text-start">
    Área
  </div>
  <div class="combo">
    <div class="input-group mb-3">
      <select class="form-select" id="inputGroupSelect02">
        <option selected>Seleccionar...</option>
        <option value="1">Escuela Técnica</option>
        <option value="2">Educación Especializada</option>
        <option value="3">CAADI</option>

      </select>
    </div>
  </div>

  <div class="list text-start">
    Instructor
  </div>
  <div class="combo">
    <div class="input-group mb-3">
      <select class="form-select" id="inputGroupSelect02">
        <option selected>Seleccionar...</option>
        <option value="1">Alejandra Pérez Robles</option>
        <option value="2">Hugo Abraham Avila Navarro</option>
        <option value="3">Maestro de Prueba</option>
      </select>
    </div>
  </div>

  <div class="list text-start">
    Oferta
  </div>
  <div class="combo">
    <div class="input-group mb-3">
      <select class="form-select" id="inputGroupSelect02">
        <option selected>Seleccionar...</option>
        <option value="1">Técnico Desarrollador Web</option>
        <option value="2">Técnico Mecatrónico</option>
        <option value="3">Excel</option>
      </select>
    </div>
  </div>

  <div class="list text-start">
    Módulo
  </div>
  <div class="combo">
    <div class="input-group mb-3">
      <select class="form-select" id="inputGroupSelect02">
        <option selected>Seleccionar...</option>
        <option value="1">Módulo 1</option>
        <option value="2">Módulo 2</option>
      </select>
    </div>
  </div>

  <div class="list text-start">
    Salón
  </div>
  <div class="combo">
    <div class="input-group mb-3">
      <select class="form-select" id="inputGroupSelect02">
        <option selected>Seleccionar...</option>
        <option value="1">1-101</option>
        <option value="2">1-102</option>
        <option value="2">1-103</option>
      </select>
    </div>
  </div>

  <div class="list text-start">
    Día de Clase
  </div>
  <div class="combo">
    <div class="input-group mb-3">
      <select class="form-select" id="inputGroupSelect02">
        <option selected>Seleccionar...</option>
        <option value="1">Sábado</option>
        <option value="2">Domingo</option>
        <option value="2">Martes y Jueves</option>
        <option value="2">Lunes a Viernes</option>
      </select>
    </div>
  </div>

  <div class="list text-start">
    Horario
  </div>
  <div class="combo">
    <div class="input-group mb-3">
      <select class="form-select" id="inputGroupSelect02">
        <option selected>Seleccionar...</option>
        <option value="1">09:00 - 14:00 hrs</option>
        <option value="2">14:30 - 19:30 hrs</option>
        <option value="2">19:00 - 21:30 hrs</option>
      </select>
    </div>
  </div>

  <div class="list text-start">
    Fecha de inicio
  </div>
  <div class="combo">
        <input type="date" id="start" name="trip-start"
        value="2018-07-22"
        min="2022-01-01" max="2022-12-31">
  </div>

  <br>
  <br>

  <!-- Input para ingresar la cantidad de alumnos -->    
      <div class="A text-start cantidad">
        <div class="B">Cantidad de alumnos</div>
        <div class="B B-input">
          <div class="input-group input-group-sm mb-3">
            <input type="number" class="form-control " aria-label="Sizing example input" aria-describedby="inputGroup-sizing-sm" v-model="cantidad">
          </div>
        </div>
      </div>
  <!-- Campos por alumnos -->
    <div class="contenedor">
      <div v-for="alumnos in cantidad">
      <div class="text-start">
          Nombre del alumno {{alumnos}}
        </div>
        
        <div class="" v-for="item in 1">
          <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Alumno..." aria-label="Recipient's username" aria-describedby="basic-addon2">
            <div class="input-group-append">
          </div>
        </div>
      </div>
    </div>

  <!-- Input para ingresar la cantidad de alumnos -->    
      <div class="A text-start cantidad">
        <div class="B">Cantidad de clases</div>
        <div class="B B-input">
          <div class="input-group input-group-sm mb-3">
            <input type="number" class="form-control " aria-label="Sizing example input" aria-describedby="inputGroup-sizing-sm" v-model="clases">
          </div>
        </div>
      </div>

  <br>
  <button type="button" class="btn btn-primary ajuste" v-on:click="agregarMinuta()">Agregar</button>
  <br><br>
  
  </div>
  </div>
</span>
</template>

<script>
  export default {
    name: 'App',
    components: {},
    data() {
      return {
        listaM: true,
        agregarM: false
      };
    },
    methods: {
      agregarMinuta(){
        this.listaM = true;
        this.agregarM = false;
      },
      agregarMinuta1(){
        this.listaM = false;
        this.agregarM = true;
      }
    },
  };
</script>

<style>
.agregar{
  position: relative;
}

.campos {
  max-width: 320px;
}

.green {
  background-color: #1C7947;
  color: #fff;
}

.greenli {
  background-color: #e4e9be;
}
</style>