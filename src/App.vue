<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import Educacion from './components/EducacionComponente.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';

  </script>

<template>
  <header>
<!--BARRA DE NAVEGACION--> 
<NavBar />
<!-- Componente Datos Personales--> 
<DatosPersonales/>

  </header>
  <main>
    <!-- el estilo css de la section se encuentra en base.css -->
      <section id="educacion"><h2> Educación - Cursos</h2></section>
      <Educacion/>

      <section id="experiencia"><h2>Experiencia</h2></section>
      <ExperienciaComponente/>
      
      <section id="proyectos"><h2>Proyectos</h2></section>
      <section id="habilidades"><h2>Habilidades</h2></section>
      <section id="intereses"><h2>Intereses</h2></section>
  </main>

</template>

<style scoped>

</style>
