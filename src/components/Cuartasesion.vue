<template>
  <br />
  <h4>Cuarta sesión</h4>
  <br />
  <!-- Input para ingresar la cantidad de prácticas -->
  <div class="A text-start">
    <div class="B">Cantidad de Alumnos:</div>
    <div class="B B-input">
      <div class="input-group input-group-sm mb-3">
        <input
          type="number"
          class="form-control"
          aria-label="Sizing example input"
          max="50"
          aria-describedby="inputGroup-sizing-sm"
          v-model="cantidad"
        />
      </div>
    </div>
  </div>
  <!-- Campo para la descripción del proyecto -->
  <div class="descripcion">
    <label>Describa en qué consiste el Proyecto:</label>
    <textarea class="form-control" aria-label="With textarea"></textarea>
  </div>
  <br />
  <!-- Campo para la descripción del Examen -->
  <div class="descripcion">
    <label>Describa qué se aplico en el Examen:</label>
    <textarea class="form-control" aria-label="With textarea"></textarea>
  </div>
  <br />
  <!-- Campos por alumnos -->
  <div class="contenedor">
    <div v-for="alumnos in cantidad">
      <div class="text-start">Nombre del alumno {{ alumnos }}</div>
      <div class="input-group mb-3">
        Proyecto: &thinsp;
        <select class="form-select" id="inputGroupSelect02">
          <option value="0"></option>
          <option value="1">Excelente</option>
          <option value="2">Cumplió</option>
          <option value="3">Deficiente</option>
          <option value="4">No Cumplió</option>
        </select>
      </div>
      <div class="input-group mb-3">
        Examen: &thinsp;
        <input
          type="number"
          class="form-control"
          min="0"
          max="100"
          aria-label="Sizing example input"
          aria-describedby="inputGroup-sizing-sm"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'App',
  components: {},
  data() {
    return {
      cantidad: '',
    };
  },
  methods: {},
};
</script>

<style>
.uanl {
  width: 30%;
  float: left;
  margin-top: -50px;
}
.fime {
  width: 30%;
  float: right;
  margin-top: -50px;
}
.datosM {
  padding: 20px;
}
.B-input {
  width: 20%;
}
.descripcion {
  margin: 0 auto;
  width: 90%;
}
.A {
  width: 90%;
}
.B {
  display: inline-block;
  margin: 5px;
}
.contenedor {
  width: 80%;
}
</style>
