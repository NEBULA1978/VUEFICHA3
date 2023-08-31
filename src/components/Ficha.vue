
<template>
    <!-- <h1>Hijo</h1> -->
    <div>
        <button class="boton">
            {{ cosa.ropa }} ({{ cosa.marca }})
        </button>
        <div class="estrellas">
            <span v-for="index in cosa.nota" :key="index">
                <img src="https://www.html6.es/img/estrella.png" alt="">
            </span>
        </div>
        <button>+</button>
    </div>
</template>

<script setup>
const props = defineProps({
    cosa: String,
    index: Number
})
</script>

<style scoped></style>
