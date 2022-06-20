<template>
  <!--Apartado para agregar maestros-->
  <h5>Agregar Salon</h5>
  <br />
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control campos"
      placeholder="Salón..."
      aria-label="Recipient's username"
      aria-describedby="basic-addon2"
    />
  </div>
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control campos"
      placeholder="Cómputo..."
      aria-label="Recipient's username"
      aria-describedby="basic-addon2"
    />
  </div>

  <button type="button" class="btn btn-success agregar">Agregar</button>
  <br />
  <br />
  <br />
  <!--Tabla de maestros-->
  <div class="table-responsive">
    <table class="table table-bordered">
      <tr class="green">
        <th scope="col">Salón</th>
        <th scope="col">Cómputo</th>
      </tr>
      <tr class="greenli">
        <td scope="col">1-001</td>
        <td scope="col">No</td>
      </tr>
      <tr class="greenli">
        <td scope="col">1-002</td>
        <td scope="col">No</td>
      </tr>
      <tr class="greenli">
        <td scope="col">1-003</td>
        <td scope="col">Sí</td>
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
