<template>
  <br />
  <h4>Asistencias</h4>
  <br />
  <!-- Input para ingresar la cantidad de prácticas -->
  <div class="A text-start">
   <div class="B">Cantidad de Alumnos:</div>
    <div class="B B-input">
      <div class="input-group input-group-sm mb-3">
        <input
          type="number"
          class="form-control"
          aria-label="Sizing example input"
          max="50"
          aria-describedby="inputGroup-sizing-sm"
          v-model="cantidad2"
        />
      </div>
    </div>
    <div class="B">Cantidad de clases:</div>
    <div class="B B-input">
      <div class="input-group input-group-sm mb-3">
        <input
          name="myInput_DRS"
          onkeypress="return isNumeric(event)"
          oninput="maxLengthCheck(this)"
          type = "number"
          placeholder="Numero"
          min = "1"
          max = "4"
          class="form-control"
          aria-label="Sizing example input"
          
          aria-describedby="inputGroup-sizing-sm"
          v-model="cantidad"
          v-on:click.capture="isNumeric"
          v-on:click.capture="maxLengthCheck"
        />
      </div>
    </div>
  </div>

  <!-- Campo para la descripción -->
  <div class="descripcion" v-for="item in cantidad">
  <label>Describa la Clase {{ item }} :</label>
    <textarea class="form-control" aria-label="With textarea"></textarea>
    
  </div>
  <br />
  <!-- Campos por alumnos -->
  <div class="contenedor">
    <div v-for="alumnos in cantidad2">
      <div class="text-start">Nombre del alumno {{ alumnos }}</div>

      <div class="" v-for="item in cantidad">
        <div class="input-group mb-3">
          Clase {{ item }} : &thinsp;
          <select class="form-select" id="inputGroupSelect02">
            <option value="0"></option>
            <option value="1">Asistencia</option>
            <option value="2">Falta</option>
            <option value="3">Retardo</option>
            <option value="4">Justificante</option>
          </select>
        </div>
      </div>
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
 methods: {
   // Codigo para definir un maximo de clases.
   maxLengthCheck(object) {
    if (object.value.length > object.max.length)
      object.value = object.value.slice(0, object.max.length)
  },
    
  isNumeric(evt) {
    var theEvent = evt || window.event;
    var key = theEvent.keyCode || theEvent.which;
    key = String.fromCharCode (key);
    var regex = /[0-9]|\./;
    if ( !regex.test(key) ) {
      theEvent.returnValue = false;
      if(theEvent.preventDefault) theEvent.preventDefault();
    }
  }
 },
 
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