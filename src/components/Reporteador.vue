<template>
  <div class="table-responsive">
    <table class="order-table table">
      <tr>
        <th>Fecha de Minuta</th>
        <th>Área</th>
        <th>Oferta</th>
        <th>Módulo</th>
        <th>Maestro</th>
        <th>Aula</th>
        <th>Día</th>
        <th>Horario Curso</th>
        <th>Periodo</th>
      </tr>
      <tr>
        <td>14/05/2022</td>
        <td>Escuela Técnica</td>
        <td>Mecatrónica</td>
        <td>1 Matemáticas</td>
        <td>Alejandra Pérez Robles</td>
        <td>2300</td>
        <td>Sábados</td>
        <td>09:00 - 14:00 hrs</td>
        <td>388</td>
      </tr>
      <tr>
      </tr>
    </table>
  </div>
</template>

<script>
  export default {
    name: 'App',
    components: {},
    data() {
      return {};
    },
    methods: {},
  };
</script>

<style>
  table {
    font-family: arial, sans-serif;
    border-collapse: collapse;
    width: 100%;
  }

  td, th {
    border: 1px solid #dddddd;
    text-align: left;
    padding: 8px;
  }

  tr:nth-child(even) {
    background-color: #dddddd;
  }
  .editar{
    

  }
</style>