<template>
    <div>
        <h1>Estoy en el artículo número {{ myId }}</h1>
    </div>
</template>

<script setup>
const route = useRoute()
const myId = ref(route.params.id); // Crear una variable vacía, para que tenga un valor poner entre "" dentro del paréntesis

</script>
