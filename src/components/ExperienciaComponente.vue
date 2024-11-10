<script setup>
import icono1 from '/src/assets/ventas.svg';
import icono2 from '/src/assets/ecomerce.svg';
import icono3 from '/src/assets/configuracion.svg';
import icono4 from '/src/assets/uiux.svg';
import icono5 from '/src/assets/watch.svg';

import { ref } from 'vue';
const titulo = 'Desarrollador Web NearTech';
const fecha = 'Desde Enero 2023 / Julio 2024';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'En Neartech desarrollo de paginas web con WordPress para Bodega Labiano donde se implemento un nuevo plugin creado de forma personal para manejar el sistema contable de la empresa.' },
    { id: 2, src: icono2, parrafo: 'Se realizo el la produccion del plugin implementando Tango Gestion en Wordpress.' },
    { id: 3, src: icono3, parrafo: 'Se realizo creacion de plantilla desde 0 para una produccion mas a detalle con el cliente.' },
    { id: 4, src: icono4, parrafo: 'Colabore con el desarrollador FullStack de Neartech para la produccion total del sistema contable.' },
    { id: 5, src: icono5, parrafo: 'Automaticé procesos de tareas diarias gestiones monotonas para reducir la carga horaria laboral un 15%.' },
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experencia in experiencias" :key="experencia.id">
                <img class="imagen-svg" :src="experencia.src" width="45rem" :alt="experencia.parrafo">
                <p>{{ experencia.parrafo }}</p>
            </li>

            <!-- <li class="item"><img class="imagen-svg" src="/src/assets/ventas.svg" width="45rem" alt="">
                <p>En Neartech desarrollo de paginas web con WordPress para Bodega Labiano donde se implemento un nuevo plugin creado de forma personal para manejar el sistema contable de la empresa.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/ecomerce.svg" width="45rem" alt="">
                <p>Se realizo el la produccion del plugin implementando Tango Gestion en Wordpress.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/configuracion.svg" width="45rem" alt="">
                <p>Se realizo creacion de plantilla desde 0 para una produccion mas a detalle con el cliente.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/uiux.svg" width="45rem" alt="">
                <p>Colabore con el desarrollador FullStack de Neartech para la produccion total del sistema contable.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/watch.svg" width="45rem" alt="">
                <p>Automaticé procesos de tareas diarias gestiones monotonas para reducir la carga horaria laboral un 15%.</p>
            </li> -->
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: coral;
}

.fecha {
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>