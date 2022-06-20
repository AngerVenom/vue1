<template>
  <div class="activas">
    <div class="buscador">
      <input
        class="form-control col-md-3 light-table-filter buscador"
        data-table="order-table"
        type="text"
        placeholder="Search.."
      />
      <br />
    </div>
    <h4>Minutas Activas</h4>
    <div class="table-responsive">
      <table class="table table-bordered">
        <tr class="green">
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
        <tr class="greenli">
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
      </table>
    </div>
  </div>
  <br />
  <br />
  <br />
  <div class="cerradas">
    <div class="buscador">
      <input
        class="form-control col-md-3 light-table-filter"
        data-table="order-table"
        type="text"
        placeholder="Search.."
      />
    </div>
    <br />
    <h4>Minutas Cerradas</h4>
    <div class="table-responsive">
      <table class="table table-bordered">
        <tr class="green">
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
        <tr class="greenli">
          <td>15/05/2022</td>
          <td>Especializada</td>
          <td>Excel</td>
          <td>Básico</td>
          <td>Hugo Abraham Avila Navarro</td>
          <td>11-303</td>
          <td>Domingo</td>
          <td>09:00 - 14:00 hrs</td>
          <td>388</td>
        </tr>
      </table>
    </div>
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

td,
th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}

.activas,
.cerradas {
  width: 95%;
  margin: 0 auto;
}
.buscador {
  width: 200px;
}

.green {
  background-color: #1c7947;
  color: #fff;
}

.greenli {
  background-color: #e4e9be;
}
</style>
