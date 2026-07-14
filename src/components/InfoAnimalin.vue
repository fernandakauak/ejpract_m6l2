<script setup>
    import { ref } from 'vue';
    let animalin = {
	    nombre: "Memi",
	    tipo: "Gata",
	    edad: 6,
	    vacunado: true,
	    foto: "/src/assets/memi.jpg",
	    caracteristicas: ["Con manchitas", "Tamaño mediano", " Ojitos grandes"],
        curiosidad: "Baila cuando pongo flamenco"
    };

</script>

<template>
    <article>
        <h1>Les presento a <br>
            {{ animalin.nombre }}</h1>
        <img v-bind:src="animalin.foto" alt="animalin.nombre">
        <h2>Es una {{ animalin.tipo }} de {{ animalin.edad }} años.</h2>
        <h3>¿Tiene sus vacunas? 
            <span v-if="vacunado = true">¡Sí, tiene sus vacunas!</span>
            <span v-else>No voy a decir que no las tiene porque nunca haría eso -_-</span>
        </h3>
        <h3>Características:</h3>
        <ul v-for="item in animalin.caracteristicas" :key="item">
            <li>{{ item }}</li>
        </ul>
        <h4>Dato curioso: {{ animalin.curiosidad }}</h4>
    </article>
</template>

<style scoped>
    article {
        width: 80%;
        margin: 5% auto;
        border-radius: 20px;
        background-color: palevioletred;
        color: #5d0f0f;
    }

    img {
        width: 40%;
        border-radius: 250px;
    }
    
    h1 {
        font-weight: bold;
        line-height: 120%;
    }

    h4 {
        font-style: italic;
    }

    ul {
        width: 30%;
        margin: auto;
    }
</style>