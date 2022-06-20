<template>
  <span v-if="datosvisibles == true">
    <!-- Datos de la minuta -->
    <br />
    <div>
      <h3>Datos de la minuta</h3>
      <div class="text-start datosM">
        <strong>Área:</strong> Escuela Técnica <br />
        <strong>Instructor:</strong> Alejandra Pérez Robles <br />
        <strong>Módulo:</strong> 9 - Excel II<br />
        <strong>Oferta:</strong> Informática Computacional <br />
        <strong>Modalidad:</strong> Presencial<br />
        <strong>Salón:</strong> 11-301<br />
      </div>
    </div>
    <!-- Tabla de criterios de Evaluación y asistencia -->
    <div class="informacion table-responsive">
      <table class="table table-bordered">
        <tr class="green">
          <td>Criterios de asistencia</td>
          <td>Criterios de Evaluación</td>
        </tr>
        <tr class="greenli">
          <td>Asistencia</td>
          <td>Excelente</td>
        </tr>
        <tr class="greenli">
          <td>Falta</td>
          <td>Cumplio</td>
        </tr>
        <tr class="greenli">
          <td>Retardo</td>
          <td>Deficiente</td>
        </tr>
        <tr class="greenli">
          <td>Justificante</td>
          <td>No cumplió</td>
        </tr>
      </table>
      <!-- Botones para continuar con la captura de asistencia o regresar -->
      <div class="d-grid gap-2 d-md-flex justify-content-md-end"></div>
    </div>
  </span>
  <!-- Lista de alumnos con combo para capturar (componente) -->
  <span v-if="asis == true">
    <Asistencia />
  </span>
  <!-- Regresar al listado -->
  <span v-if="MinMae == true">
    <MinutasMaestros />
  </span>
</template>

<script>
import Asistencia from './Asistencia.vue';
import MinutasMaestros from './MinutasMaestros.vue';
export default {
  name: 'App',
  components: {
    Asistencia,
    MinutasMaestros,
  },
  data() {
    return {
      datosvisibles: true,
      asis: false,
      MinMae: false,
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

.green {
  background-color: #1c7947;
  color: #fff;
  font-weight: 500;
}

.greenli {
  background-color: #e4e9be;
}

.red {
  background-color: #f24c4c;
}
</style>
