<template>
  <span v-if="listademinutas == true">
    <div class="activas">
      <div class="buscador">
        <input
          class="form-control col-md-3 light-table-filter buscador"
          data-table="order-table"
          type="text"
          placeholder="Search.."
        />
        <br />
        <button
          type="button"
          class="btn btn-success agregar"
          v-on:click="agregar()"
        >
          <!--*Poner funcion de buscar-->
          Buscar
        </button>
        <br />
        <br />
      </div>
      <div class="table-responsive">
        <table class="table table-bordered">
          <tr class="green">
            <th>#</th>
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
            <td>1</td>
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
          <tr class="greenli">
            <td>2</td>
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
          <tr class="greenli">
            <td>3</td>
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
          <tr class="greenli">
            <td>4</td>
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
    <br />
    <br />
  </span>
  <span v-if="agregarm == true">
    <br />
    <h3>Agregar Minuta</h3>

    <div>
      <div class="contenedor">
        <div class="list text-start">Área</div>
        <div class="combo">
          <div class="input-group mb-3">
            <select class="form-select" id="inputGroupSelect02">
              <option selected>Seleccionar...</option>
              <option value="1">Escuela Técnica</option>
              <option value="2">Especializada</option>
              <option value="3">CAADI</option>
            </select>
          </div>
        </div>

        <div class="list text-start">Instructor</div>
        <div class="combo">
          <div class="input-group mb-3">
            <select class="form-select" id="inputGroupSelect02">
              <option selected>Seleccionar...</option>
              <option value="1">Alejandra Pérez Robles</option>
              <option value="2">Hugo Abraham Avila Navarro</option>
              <option value="3">Maestro de Prueba</option>
            </select>
          </div>
        </div>

        <div class="list text-start">Oferta</div>
        <div class="combo">
          <div class="input-group mb-3">
            <select class="form-select" id="inputGroupSelect02">
              <option selected>Seleccionar...</option>
              <option value="1">Desarrollador Web</option>
              <option value="2">Mecánica Automotriz</option>
              <option value="3">Excel</option>
            </select>
          </div>
        </div>

        <div class="list text-start">Módulo</div>
        <div class="combo">
          <div class="input-group mb-3">
            <select class="form-select" id="inputGroupSelect02">
              <option selected>Seleccionar...</option>
              <option value="1">Módulo 1</option>
              <option value="2">Módulo 2</option>
              <option value="3">Módulo 3</option>
            </select>
          </div>
        </div>

        <div class="list text-start">Modalidad</div>
        <div class="combo">
          <div class="input-group mb-3">
            <select class="form-select" id="inputGroupSelect02">
              <option selected>Seleccionar...</option>
              <option value="1">Presencial</option>
              <option value="2">En línea</option>
              <option value="3">Híbrido</option>
            </select>
          </div>
        </div>

        <div class="list text-start">Salón</div>
        <div class="combo">
          <div class="input-group mb-3">
            <select class="form-select" id="inputGroupSelect02">
              <option selected>Seleccionar...</option>
              <option value="1">1-101</option>
              <option value="2">1-102</option>
              <option value="3">1-103</option>
            </select>
          </div>
        </div>

        <div class="list text-start">Día</div>
        <div class="combo">
          <div class="input-group mb-3">
            <select class="form-select" id="inputGroupSelect02">
              <option selected>Seleccionar...</option>
              <option value="1">Sábado</option>
              <option value="2">Domingo</option>
              <option value="3">Martes y jueves</option>
              <option value="3">Lunes a Viernes</option>
            </select>
          </div>
        </div>

        <div class="list text-start">Horario</div>
        <div class="combo">
          <div class="input-group mb-3">
            <select class="form-select" id="inputGroupSelect02">
              <option selected>Seleccionar...</option>
              <option value="1">09:00 a 14:00 hrs</option>
              <option value="2">14:30 a 17:30 hrs</option>
              <option value="3">19:00 a 21:30 hrs</option>
              <option value="3">15:00 a 17:00 hrs</option>
            </select>
          </div>
        </div>

        <div class="list text-start">Fecha de inicio</div>
        <div class="combo">
          <input type="date" />
        </div>

        <div class="list text-start">Fecha de término</div>
        <div class="combo">
          <input type="date" />
        </div>
      </div>
      <br /><br /><br />
      <br /><br /><br />
      <br /><br /><br />
      <br /><br /><br />
      <br /><br /><br />
      <br /><br /><br />
      <br /><br /><br />
      <br /><br />
      <div class="doble">
        <div class="ajustecontrol">
          <div class="B">Cantidad de Clases</div>
          <div class="B">
            <input
              type="number"
              class="form-control"
              aria-label="Sizing example input"
              aria-describedby="inputGroup-sizing-sm"
            />
          </div>

          <div class="B">Cantidad de alumnos</div>
          <div class="B">
            <input
              type="number"
              class="form-control"
              aria-label="Sizing example input"
              aria-describedby="inputGroup-sizing-sm"
              v-model="cantidad"
            />
          </div>
        </div>

        <div class="" v-for="item in cantidad">
          <div class="input-group mb-3">
            Nombre del alumno {{ item }} &thinsp;
            <div class="input-group mb-3">
              <input
                type="text"
                class="form-control"
                placeholder="Nombre completo..."
                aria-label="Recipient's username"
                aria-describedby="basic-addon2"
              />
              <div class="input-group-append"></div>
            </div>
          </div>
        </div>
      </div>
      <button
        type="button"
        class="btn btn-primary volver"
        v-on:click="volver()"
      >
        Agregar
      </button>
    </div>
  </span>
</template>

<script>
export default {
  name: 'App',
  components: {},
  data() {
    return {
      agregarm: false,
      listademinutas: true,
      cantidad: '',
    };
  },
  methods: {
    agregar() {
      this.agregarm = true;
      this.listademinutas = false;
    },
    volver() {
      this.agregarm = false;
      this.listademinutas = true;
    },
  },
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

tr:nth-child(even) {
  background-color: #dddddd;
}
.activas,
.cerradas {
  width: 95%;
  margin: 0 auto;
}
.buscador {
  width: 200px;
}
.volver {
  top: 167px;
  right: 190px;
}
.contenedor,
.doble {
  margin: 0 auto;
  height: 200px;
  width: 75%;
}
.A {
  width: 90%;
}
.B {
  margin: 5px;
}
.contenedor {
  width: 80%;
}
.ajustecontrol {
  width: 200px;
  aling: left;
}
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
</style>
