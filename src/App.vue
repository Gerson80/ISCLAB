<script setup>
//import HelloWorld from './components/HelloWorld.vue'
import Titulo from './components/Titulo.vue'
import Cabecera from './components/Cabecera.vue'
import Proyectos from './components/Proyectos.vue'
import Que_hacemos from './components/Que_hacemos.vue'
import Pueden_crear from './components/Pueden_crear.vue'
import Queclase from './components/Queclase.vue'


</script>

<template>
  <body class="bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500 ">
    <Cabecera></Cabecera>

  <section >
    <Titulo></Titulo>
    <Que_hacemos></Que_hacemos>
    <Pueden_crear></Pueden_crear>
    <Queclase></Queclase>
    <Proyectos></Proyectos>
  </section>
  
  
  </body>
  
  
  
 
</template>