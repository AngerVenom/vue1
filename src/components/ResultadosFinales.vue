<template>
  <br />
  <h4>Resultados Finales</h4>
  <br />
  <!-- Campos por alumnos -->
  <br />
  <div class="contenedor">
    <table class="table">
      <thead>
        <tr>
          <th scope="col">Matrícula</th>
          <th scope="col">Nombre</th>
          <th scope="col">Calif.</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">1</th>
          <td>Mark</td>
          <td>90</td>
        </tr>
        <tr>
          <th scope="row">2</th>
          <td>Jacob</td>
          <td>80</td>
        </tr>
        <tr>
          <th scope="row">3</th>
          <td>Larry</td>
          <td>N/A</td>
        </tr>
      </tbody>
    </table>

    <div class="form-check">
      <input
        class="form-check-input"
        type="checkbox"
        value=""
        id="defaultCheck1"
      />
      <p class="text-start" for="defaultCheck1">
        Los resultados están correctos
      </p>
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
