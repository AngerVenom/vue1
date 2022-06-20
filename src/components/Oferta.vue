<template>
  <!--Apartado para agregar una oferta-->
  <h5>Agregar Oferta</h5>
  <br />
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control campos"
      placeholder="Oferta..."
      aria-label="Recipient's username"
      aria-describedby="basic-addon2"
    />
    <div class="input-group-append"></div>
  </div>
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control campos"
      placeholder="Área..."
      aria-label="Recipient's username"
      aria-describedby="basic-addon2"
    />
    <div class="input-group-append"></div>
  </div>
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control campos"
      placeholder="Modalidad..."
      aria-label="Modalidad"
      aria-describedby="basic-addon2"
    />
    <div class="input-group-append"></div>
  </div>
  <button type="button" class="btn btn-success agregar">Agregar</button>
  <br /><br /><br />
  <!--Tabla de información-->
  <div class="table-responsive">
    <table class="table table-bordered">
      <tr class="green">
        <th scope="col">#</th>
        <th scope="col">Oferta</th>
        <th scope="col">Área</th>
        <th scope="col">Modalidad</th>
      </tr>
      <tr class="greenli">
        <td scope="col">1</td>
        <td scope="col">Excel</td>
        <td scope="col">Educación Especializada</td>
        <td scope="col">En Línea</td>
      </tr>
      <tr class="greenli">
        <td scope="col">2</td>
        <td scope="col">TDW</td>
        <td scope="col">Escuela Técnica</td>
        <td scope="col">En Línea</td>
      </tr>
      <tr class="greenli">
        <td scope="col">3</td>
        <td scope="col">Inglés Intermedio</td>
        <td scope="col">CAADI</td>
        <td scope="col">Presencial</td>
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
.agregar {
  position: relative;
}
.green {
  background-color: #1c7947;
  color: #fff;
}

.greenli {
  background-color: #e4e9be;
}

.campos {
  max-width: 250px;
}
</style>
