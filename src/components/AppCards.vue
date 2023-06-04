<script>
export default {
    name: "AppCards",
    props: {
        details: Object
    }
}
</script>

<!-- TEMPLATE -->
<template>
    <!-- Blocco carta (Scopongo in componente figlio) -->
    <div class="comics-card">
        <img :src="details.thumb" :alt="details.series">
        <h5>{{ details.series }}</h5>
    </div>
</template>


<!-- Aggiungo lo scoped perchè lo stile ci interessa solo per il componente relativo -->
<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables.scss' as *;

.comics-card {
    width: 190px;
    height: 200px;
    padding: 20px;
    text-align: left;
    margin-bottom: 25px;
    position: relative;

    h5 {
        color: white;
        text-transform: uppercase;
    }

    img {
        width: 100%;
        max-height: 100%;
        object-fit: cover;
        transition: transform 0.3s ease-in-out;
    }

    &:hover img {
        transform: scale(1.2);
        filter: grayscale(100%);
        transition: filter 0.5s ease-in-out;
    }
}
</style>
