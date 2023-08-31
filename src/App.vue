<!-- comunicamos el padre con el hijo con props -->
<template>
  <!-- <h1>Padre</h1> -->
  <div>
    <div v-for="(cosa,index) in cosas" :key="index">
      <FichaVue :cosa="cosa" :index="index" @retorno="retorno"/>
    </div>
  </div>

    
</template>
  
<script setup>
  // import HelloWorld from './components/HelloWorld.vue'
  import FichaVue from './components/Ficha.vue'
  import cosas from "./assets/datos"
  // a es la nota e i el indice
  const retorno=(a,i)=>{
    if(a>=6){
      cosas.value[i].nota=1;

    }else{
      cosas.value[i].nota=a+1;
    }

  }
</script>

<style scoped></style>
