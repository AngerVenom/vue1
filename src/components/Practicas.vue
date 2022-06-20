<template>
  <br />
  <h4>Prácticas</h4>
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
          v-model="cantidad2"
        />
      </div>
    </div>
    <div class="B">Cantidad de Prácticas:</div>
    <div class="B B-input">
      <div class="input-group input-group-sm mb-3">
        <input
          type="number"
          class="form-control"
          aria-label="Sizing example input"
          max="15"
          aria-describedby="inputGroup-sizing-sm"
          v-model="cantidad"
        />
      </div>
    </div>
  </div>

  <!-- Campo para la descripción -->
  <div class="descripcion" v-for="item in cantidad">
   <label>Describa la Práctica {{ item }} :</label>
    <textarea class="form-control" aria-label="With textarea"></textarea>
   
  </div>
  <br />
  <!-- Campos por alumnos -->
  <div class="contenedor">
    <div v-for="alumnos in cantidad2">
      <div class="text-start">Nombre del alumno {{ alumnos }}</div>

      <div class="" v-for="item in cantidad">
        <div class="input-group mb-3">
          Práctica {{ item }} : &thinsp;
          <select class="form-select" id="inputGroupSelect02">
            <option value="0"></option>
            <option value="1">Excelente</option>
            <option value="2">Cumplió</option>
            <option value="3">Deficiente</option>
            <option value="4">No cumplió</option>
          </select>
        </div>
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
