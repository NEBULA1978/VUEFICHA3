
<template>
    <!-- <h1>Hijo</h1> -->
    <div class="display">
        <button class="boton">
            {{ cosa.ropa }} ({{ cosa.marca }})
        </button>
        <div class="estrellas">
            <span v-for="index in cosa.nota" :key="index">
                <img src="https://www.html6.es/img/estrella.png" alt="">
            </span>
        </div>
        <!-- para modificar el padre valores de datos.js -->
        <button @click="incrementarNota(cosa.nota,index)">+</button>
    </div>
</template>

<script setup>
const emito=defineEmits('[retorno]')
const incrementarNota =(a,i)=>{
    // comunicamos con el padre
    // viene del boton +
    emito('retorno',a,i)
}
const props = defineProps({
    cosa: String,
    index: Number
})
</script>

<style scoped>
/* En la misma fila centrados */
.display {
    display: flex;
    align-items: center;
}

.display img {
    width: 15px;
    margin: 1px;
}

.diplay button {
    margin-right: 20px;
}

.boton {
    width: 165px;
}

.estrellas {
    width: 125;
    height: 22px;
}
</style>
