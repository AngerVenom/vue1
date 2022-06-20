<template>
  <h5>Agregar Usuario</h5>
  <br />
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control campos"
      placeholder="Usuario..."
      aria-label="Recipient's username"
      aria-describedby="basic-addon2"
    />
    <div class="input-group-append"></div>
  </div>
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control campos"
      placeholder="Contraseña..."
      aria-label="Recipient's username"
      aria-describedby="basic-addon2"
    />
    <div class="input-group-append"></div>
  </div>
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control campos"
      placeholder="Rol..."
      aria-label="Modalidad"
      aria-describedby="basic-addon2"
    />
    <div class="input-group-append"></div>
  </div>
  <button type="button" class="btn btn-success agregar">Agregar</button>
  <br /><br />
  <br />
  <!--Tabla de información-->
  <div class="table-responsive">
    <table class="table table-bordered">
      <tr class="green">
        <th scope="col">#</th>
        <th scope="col">Usuario</th>
        <th scope="col">Contraseña</th>
        <th scope="col">Rol</th>
      </tr>
      <tr class="greenli">
        <td scope="col">1</td>
        <td scope="col">user1</td>
        <td scope="col">123</td>
        <td scope="col">Maestro</td>
      </tr>
      <tr class="greenli">
        <td scope="col">2</td>
        <td scope="col">admin</td>
        <td scope="col">123</td>
        <td scope="col">Administrador</td>
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
