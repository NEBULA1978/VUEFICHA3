<!-- comunicamos el padre con el hijo con props -->
<template>
  <!-- <h1>Padre</h1> -->
  <div>
    <div v-for="(cosa,index) in cosas" :key="index">
      <FichaVue :cosa="cosa" :index="index"/>
    </div>
  </div>

    
</template>
  
<script setup>
  // import HelloWorld from './components/HelloWorld.vue'
  import FichaVue from './components/Ficha.vue'
    import cosas from "./assets/datos"
</script>

<style scoped></style>
