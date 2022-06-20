<template>
  <!-- Bootstrap (estilos) -->
  <link
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css"
    rel="stylesheet"
    integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3"
    crossorigin="anonymous"
  />
  <div id="app">
    <!-- Login o punto de acceso -->
    <div class="todo">
      <!-- Input de usuario e input de contraseña -->
      <span v-if="accedio == true">
        <h1 class="title_initial">Educación Continua y CAADI</h1>
        <br />
        <div class="estilos">
          <form action class="form">
            <label>Usuario</label>
            <input type="text" class="form-control" v-model="user" />
            <br />
            <label>Contraseña</label>
            <input type="password" class="form-control" v-model="pass" />
            <br />
            <!-- Botón de acceder -->
            <div class="d-grid gap-2 d-md-flex justify-content-md-center">
              <button
                type="button"
                class="btn btn-success campos"
                v-on:click="acceder()"
              >
                Acceder
              </button>
            </div>
          </form>
        </div>
      </span>
    </div>

    <!-- Visualizar vista de maestro (lista de minutas) -->
    <span v-if="lista == true">
      <MinutasMaestros />
    </span>
    <!-- Visualizar vista de administrador (Deshboard) -->
    <div class="adminp">
      <span v-if="administrador == true">
        <PrincipalAdmin />
      </span>
    </div>
  </div>
</template>

<script>
/* Importación de componentes */
import PrincipalAdmin from './components/PrincipalAdmin.vue';
import MinutasMaestros from './components/MinutasMaestros.vue';

export default {
  name: 'App',
  components: {
    PrincipalAdmin,
    MinutasMaestros,
  },
  data() {
    return {
      user: '',
      pass: '',
      accedio: true,
      lista: false,
      administrador: false,
    };
  },
  methods: {
    /* Función de login: deshabilita el login (accedio) y habilita el contenido del maestro (lista) */
    acceder() {
      if (this.user == 'user1' && this.pass == 123) {
        this.accedio = false;
        this.lista = true;
      } else if (this.user == 'admin' && this.pass == 123) {
        this.accedio = false;
        this.administrador = true;
      }
    },
  },
};
</script>

<!-- Estilos CSS -->
<style>
/* Fuente */
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap');

#app {
  font-family: Open Sans, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
}
.todo {
  margin-top: 100px;
}
.title_initial {
  text-align: center;
}
.estilos {
  width: 200px;
  height: 200px;
  margin: 0 auto;
}

.campos {
  position: absolute;
  display: flex;
  align-items: center;
}
</style>
