<template>
  <h5>Técnico Desarrollador Web</h5>
  <div class="table-responsive">
    <table class="table table-bordered">
      <tr class="green">
        <th scope="col">#</th>
        <th scope="col">Módulo</th>
      </tr>
      <tr class="greenli">
        <td scope="col">1</td>
        <td scope="col">Lógica Computacional</td>
      </tr>
      <tr class="greenli">
        <td scope="col">2</td>
        <td scope="col">Dev-C++</td>
      </tr>
      <tr class="greenli">
        <td scope="col">3</td>
        <td scope="col">HTML5/CSS3</td>
      </tr>
    </table>
  </div>
  <br /><br />
  <h5>Técnico Mecánica Automotriz</h5>
  <div class="table-responsive">
    <table class="table table-bordered">
      <tr class="green">
        <th scope="col">#</th>
        <th scope="col">Módulo</th>
      </tr>
      <tr class="greenli">
        <td scope="col">1</td>
        <td scope="col">Fundamentos Automotrices</td>
      </tr>
      <tr class="greenli">
        <td scope="col">2</td>
        <td scope="col">Mantenimento Preventivo</td>
      </tr>
      <tr class="greenli">
        <td scope="col">3</td>
        <td scope="col">Reparación de Motores Gasolina</td>
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
.green {
  background-color: #1c7947;
  color: #fff;
}

.greenli {
  background-color: #e4e9be;
}
</style>
