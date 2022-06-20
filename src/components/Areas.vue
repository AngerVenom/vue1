<template>
  <!--<div class="agregar">
    <input
      class="form-control col-md-3 light-table-filter cuadro"
      data-table="order-table"
      type="text"
    />
    <button class="btn btn-success me-md-2 boton" type="button" v-on:click="">
      Agregar
    </button>
  </div>-->

  <br />
  <ul class="list-group">
    <li class="list-group-item list-group-item-success campos">
      Escuela Técnica
    </li>
    <li class="list-group-item list-group-item-success campos">
      Educación Especializada
    </li>
    <li class="list-group-item list-group-item-success campos">CAADI</li>
  </ul>
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
  display: flex;
  padding-left: 1rem;
}
.cuadro {
  width: 50%;
}
.boton {
  right: 80px;
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
  max-width: 500px;
}
</style>
