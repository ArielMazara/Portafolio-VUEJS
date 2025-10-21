<script setup>
import { ref } from 'vue';

// --- CAMBIO 1: Importa FondoSvg en lugar de FondoLava ---
// (Asegúrate de que la ruta a FondoSvg.vue sea correcta)
import FondoSvg from './FondoSvg.vue'; 

// Arreglo reactivo (ref) con tus intereses personalizados
const intereses = ref([
    'Tecnología y Desarrollo de Software: Profunda pasión por la programación, la resolución de problemas complejos y la exploración de nuevas tecnologías. Tengo una marcada preferencia por el ecosistema del sistema operativo Linux, valorando su estabilidad, flexibilidad y la filosofía de código abierto.',
    'Innovación Aplicada al Campo: Me motiva especialmente la intersección entre la tecnología y el sector agrícola. Busco activamente aplicar mis conocimientos en desarrollo de software para crear herramientas innovadoras que optimicen la gestión, automaticen procesos y mejoren la eficiencia en el trabajo de campo.',
    'Naturaleza y Actividades al Aire Libre: Mantengo una fuerte conexión con el entorno natural. Disfruto del trabajo de campo, lo cual me da una perspectiva práctica de los desafíos del sector y me permite mantener un equilibrio saludable entre el trabajo digital y el físico.'
]);
</script>

<template>
    <div class="intereses-contenedor">
        
        <FondoSvg class="fondo-svg-bg" /> 
        
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
</template>

<style scoped>
.intereses-contenedor {
    position: relative; 
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
    overflow: hidden; 
    border-radius: 10px; 
    box-shadow: 0 10px 30px rgba(0,0,0,0.3); 
}

.fondo-svg-bg { /* Esta clase se aplica a tu <FondoSvg /> */
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 0; /* Queda detrás */
    object-fit: cover; 
}


.contenedor-lista {
    /* --- ¡ESTA ES LA LÍNEA CLAVE QUE FALTA! --- */
    position: relative; 
    /* ----------------------------------------- */

    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    /* Tu color blanco (var o #f0f0f0) está perfecto */
    color: var(--vt-c-white-soft, #f0f0f0); 
    font-size: 1.4rem;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.8); 
    z-index: 1; /* Ahora sí, queda adelante */
}

.item {
    margin-bottom: 1rem;
}
</style>