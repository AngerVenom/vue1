<template>
  <meta name="viewport" content="initial-scale=1">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  <!--Box Icons-->
  <link href='https://unpkg.com/boxicons@2.1.2/css/boxicons.min.css' rel='stylesheet'>

  <div class="principal">
      <!-- Sidebar -->
    <div class="sidebar">
      <div class="logo_content">
        <div class="logo">
          <i class='bx bx-cube' ></i>
          <div class="logo_name">ECC</div>
        </div>
        <i class='bx bx-menu' v-on:click="sidebarActive()" id="burguer"></i>
      </div>
      <ul class="nav_list">
        <li>
          <a class="link" href="/" v-on:click.prevent="funcion()">
            <i class='bx bxs-dashboard' ></i>
            <span class="links_name">Dashboard</span>
          </a>
          <span class="tooltip_two">Dashboard</span>
        </li> <!--Fin elemento-->
        <li>
          <a class="link" href="/" v-on:click.prevent="funcionareas()">
            <i class='bx bx-area' ></i>
            <span class="links_name">Áreas</span>
          </a>
          <span class="tooltip_two">Áreas</span>
        </li> <!--Fin elemento-->
        <li>
          <a class="link" href="/" v-on:click.prevent="funcionoferta()">
            <i class='bx bxs-offer' ></i>
            <span class="links_name">Oferta</span>
          </a>
          <span class="tooltip_two">Oferta</span>
        </li> <!--Fin elemento-->
        <li>
          <a  class="link" href="/" v-on:click.prevent="funcionmodulos()">
            <i class='bx bx-book-open'></i>
            <span class="links_name">Módulos</span>
          </a>
          <span class="tooltip_two">Módulos</span>
        </li> <!--Fin elemento-->
        <li>
          <a class="link" href="/" v-on:click.prevent="funcionmaestros()">
            <i class='bx bxs-graduation'></i>
            <span class="links_name">Maestros</span>
          </a>
          <span class="tooltip_two">Maestros</span>
        </li> <!--Fin elemento-->
        <li>
          <a  class="link" href="/" v-on:click.prevent="funcionsalones()">
            <i class='bx bx-current-location'></i>
            <span class="links_name">Salones</span>
          </a>
          <span class="tooltip_two">Salones</span>
        </li> <!--Fin elemento-->
        <li>
          <a class="link" href="/" v-on:click.prevent="funcionminutas()">
            <i class='bx bx-desktop' ></i>
            <span class="links_name">Minutas</span>
          </a>
          <span class="tooltip_two">Minutas</span>
        </li> <!--Fin elemento-->
        <li>
          <a class="link" href="/" v-on:click.prevent="funcionusuarios()">
            <i class='bx bxs-user' ></i>
            <span class="links_name">Usuarios</span>
          </a>
          <span class="tooltip_two">Usuarios</span>
        </li> <!--Fin elemento-->
      </ul>
      <!--Perfil Actual-->
      <div class="profile_content">
        <div class="profile">
          <div class="profile_detail">
            <!--<i class='bx bxs-user' ></i>-->
            <div class="name_job">
              <div class="name">Alejandra Perez</div> <!--Aqui insertar codigo php para mostrar el usuario desde la db-->
              <div class="job">Admin</div>
            </div>
          </div>
          <i class='bx bx-log-out salir' v-on:click="salir()"></i> <!--Boton de salir-->
        </div>
      </div>
    </div>
  </div>
  
  
  

  <!-- Contenido -->
  <div class="contenido">
    <!-- Cabeza -->
      <div class="cabeza">
        <h2>Gestor de Minutas Digitales</h2>
      </div>
      <!-- Contenido -->
      <div class="contenido2">

        <span v-if="panel == true">
          <h3>Dashboard</h3>
          <br >
          <Deshboard />
        </span>
        
        <span v-if="agregarareas == true">
          <h3>Áreas</h3>
          <br >
          <Areas />
        </span>

        <span v-if="ofertap == true">
          <h3>Oferta</h3>
          <br >
          <Oferta />
        </span>
        
        <span v-if="modulosp == true">
          <h3>Módulos</h3>
          <br >
          <Modulos />
        </span>

        <span v-if="maestrosp == true">
          <h3>Maestros</h3>
          <br >
          <Maestros />
        </span>
        
        <span v-if="salonesp == true">
          <h3>Salones</h3>
          <br >
          <Salones />
        </span>

        <span v-if="minutasp == true">
          <h3>Minutas</h3>
          <br >
          <Minutas />
        </span>
        
        <span v-if="usuariosp == true">
          <h3>Usuarios</h3>
          <br >
          <Usuarios />
        </span>
        
      </div>    
    </div>
  </div>
</template>

<script>
import Deshboard from './Deshboard.vue';
import Areas from './Areas.vue';
import Oferta from './Oferta.vue';
import Modulos from './Modulos.vue';
import Maestros from './Maestros.vue';
import Salones from './Salones.vue';
import Minutas from './Minutas.vue';
import Usuarios from './Usuarios.vue';
import AgregarMaestro from './AgregarMaestro.vue';

  export default {
    name: 'App',
    components: {
      Deshboard,
      Areas,
      Oferta,
      Modulos,
      Maestros,
      Salones,
      Minutas,
      Usuarios,
      AgregarMaestro
    },
    data(){
      return{
        panel: true,
        agregarareas: false,
        ofertap: false,
        modulosp: false,
        maestrosp: false,
        salonesp: false,
        minutasp: false,
        usuariosp: false
      }
    },
    methods:{
      funcion(){
        this.panel = true;
        this.agregarareas = false;
        this.ofertap = false;
        this.modulosp = false;
        this.maestrosp = false;
        this.salonesp = false;
        this.minutasp = false;
        this.usuariosp = false;
      },
      funcionareas(){
        this.panel = false;
        this.agregarareas = true;
        this.ofertap = false;
        this.modulosp = false;
        this.maestrosp = false;
        this.salonesp = false;
        this.minutasp = false;
        this.usuariosp = false;
      },
      funcionoferta(){
        this.panel = false;
        this.agregarareas = false;
        this.ofertap = true;
        this.modulosp = false;
        this.maestrosp = false;
        this.salonesp = false;
        this.minutasp = false;
        this.usuariosp = false;
      },
      funcionmodulos(){
        this.panel = false;
        this.agregarareas = false;
        this.ofertap = false;
        this.modulosp = true;
        this.maestrosp = false;
        this.salonesp = false;
        this.minutasp = false;
        this.usuariosp = false;
      },
      funcionmaestros(){
        this.panel = false;
        this.agregarareas = false;
        this.ofertap = false;
        this.modulosp = false;
        this.maestrosp = true;
        this.salonesp = false;
        this.minutasp = false;
        this.usuariosp = false;
      },
      funcionsalones(){
        this.panel = false;
        this.agregarareas = false;
        this.ofertap = false;
        this.modulosp = false;
        this.maestrosp = false;
        this.salonesp = true;
        this.minutasp = false;
        this.usuariosp = false;
      },
      funcionminutas(){
        this.panel = false;
        this.agregarareas = false;
        this.ofertap = false;
        this.modulosp = false;
        this.maestrosp = false;
        this.salonesp = false;
        this.minutasp = true;
        this.usuariosp = false;
      },
      funcionusuarios(){
        this.panel = false;
        this.agregarareas = false;
        this.ofertap = false;
        this.modulosp = false;
        this.maestrosp = false;
        this.salonesp = false;
        this.minutasp = false;
        this.usuariosp = true;
      },
      salir(){
        window.location.reload();
      },
      sidebarActive(){
        let burguer = document.querySelector("#burguer");
        let sidebar = document.querySelector(".sidebar");
        
        burguer.onclick = function(){
          sidebar.classList.toggle("active");
        }
      },
  },
};
  
</script>

<style>
  

  .contenido{
    position: absolute;
    height: 100%;
    width: calc(100% - 78px);
    left: 78px;
    transition: all 0.5s ease;
  }
  .contenido2{
    position: absolute;
    width: 90%;
  }
  
  .todo{
    display: flex;
    margin-top: 0px;
    
  }
  .active ,.contenido{ 
    width: calc(100% - 240px);
    left: 230px; 
  }
  
  
  /* Barra de navegacion */
  .bx-menu{
    cursor: pointer;
  }
  .salir{
    cursor: pointer;
  }
  ul{
    list-style-type: none;
    
  }
  .nav_list{
    padding-left: 0px;
  }
  li{
    text-align: initial;
  }
  .link{
    text-decoration: none;
    padding-left: initial;
  }
  a i{
    color: #fff;
  }
  a .links_name{
    color: #fff;
    text-decoration: none;
    padding-left: initial;
  }
  .sidebar{
    position: fixed;
    color: #fff;
    height: 100%;
    width: 78px;
    top: 0;
    left: 0;
    background: #1C7947;
    padding: 6px 14px;
    transition: all 0.5s ease;
  }
  .active{
    width: 220px;
  }
  .sidebar .logo_content .logo{
    color: #fff;
    display: flex;
    height: 50px;
    width: 100%;
    align-items: center;
    opacity: 0;
    pointer-events: none;
  }
  .active .logo_content .logo{
    opacity: 1;
    pointer-events: none;
  }
  .logo_content .logo i{
    font-size: 28px;
    margin-right: 5px;
  }
  .logo_content .logo .logo_name{
    font-size: 20px;
    font-weight: 600;
  }
  .sidebar #burguer{
    position: absolute;
    color: #fff;
    left: 50%;
    top: 6px;
    font-size: 25px;
    height: 50px;
    width: 50px;
    text-align: center;
    line-height: 50px;
    transform: translateX(-50%);
  }
  .active #burguer{
    left: 90%;
  }
  .sidebar ul{
    margin-top: 20px;
  }
  .sidebar ul li{
    position: relative;
    height: 50px;
    width: 100%;
    margin: 0 5px;
    line-height: 50px;
    
  }
  .sidebar ul li .tooltip_two{
    color: #000;
    font-weight: 400;
    position: absolute;
    left: 122px;
    top: 0;
    transform: translate(-50%, -50%);
    border-radius: 6px;
    line-height: 35px;
    text-align: center;
    height: 35px;
    width: 122px;
    background: #fff;
    box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.2);
    transition: 0s;
    opacity: 0;
    pointer-events: none;
    display: block;
  }
  .active ul li .tooltip_two{
    display: none;
  }
  .sidebar ul li:hover .tooltip_two{
    top: 50%;
    transition: all 0.5s ease;
    opacity: 1;
  }
  .sidebar ul li a{
    display: flex;
    align-items: center;
    transition: all 0.4s ease;
    border-radius: 12px;
    white-space: nowrap;
  }
  .sidebar ul li a:hover{
    background-color: #29BB89;
    color: #111o1d;
  }
  .sidebar .links_name{
    opacity: 0;
    pointer-events: none;
  }
  .active .links_name{
    opacity: 1;
    pointer-events: auto;
  }

  .sidebar ul li a i{
    height: 50px;
    min-width: 50px;
    border-radius: 12px;
    line-height: 50px;
    text-align: center;
  }
  .sidebar .profile_content{
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
  }
  .sidebar .profile_content .profile{
    position: relative;
    padding: 10px 6px;
    height: 60px;
    font-weight: 600px;
    background: #29BB89;
  }
  .profile_content .profile .profile_detail{
    display: flex;
    align-items: center;
    opacity: 0;
    pointer-events: none;
    white-space: nowrap;
  }
  .active .profile_content .profile .profile_detail{
    opacity: 1;
    pointer-events: auto;
  }
  .profile .profile_detail i{
    height: 45px;
    width: 45px;
    border-radius: 12px;
  }
  .profile .profile_detail .name_job{
    margin-left: 10px;
  }
  .profile .profile_detail .name{
    font-size: 15px;
    
  }
  .profile .profile_detail .job{
    font-size: 12px;
  }
  .profile .salir{
    position:absolute;
    left: 50%;
    bottom:5px;
    transform: translateX(-50%);
    min-width: 50px;
    line-height: 50px;
    font-size: 23px;
    border-radius: 12px;
    text-align: center;
  }
  .active .profile .salir{
    left: 88%;
  }

  .btn{
    color: black;
    position:absolute; 
    z-index:170;
    right: 0; 
    background-color: lightblue;
    border: none;
    color: white;
    padding: 1px 16px;
    font-size: 16px;
    cursor: pointer;
  }
  /* Darker background on mouse-over */
  .btn:hover {
    background-color: lightblue;
  } 
  /*Responsive */
  @media only screen and (min-width : 320px) and (max-width : 900px) {
    .contenido{
      position: absolute;
      /*text-align: left;*/
      /*margin:12px;*/
      height: 100%;
      transition: all 0.5s ease;
      width: calc(100% - 80px);
      left: 80px;
    }
    .active ,.contenido{ 
      /*margin:12px;*/
       
    }
    .sidebar ul li .tooltip_two{
      display: none;
      opacity: 0;
    }
    .active{
      display: none;
    }

    .sidebar #burguer{
      color: #1C7947;
    }
    .sidebar ul li{ 
      height: 80px;
    }

    .sidebar ul li a i{
      font-size: 24px;
    }
  }
</style>
