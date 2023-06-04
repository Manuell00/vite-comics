<script>
export default {
    name: "AppHeader",
}
</script>

<!-- TEMPLATE -->
<template>
    <header>
        <div class="header-image-container"><img src="../../public/img/dc-logo.png" alt=""></div>
        <ul class="header-menu">
            <li class="header-item"><a href="#">CHARACTERS</a></li>
            <li class="header-item"><a href="#">COMICS</a></li>
            <li class="header-item"><a href="#">MOVIES</a></li>
            <li class="header-item"><a href="#">TV</a></li>
            <li class="header-item"><a href="#">GAMES</a></li>
            <li class="header-item"><a href="#">COLLECTIBLES</a></li>
            <li class="header-item"><a href="#">VIDEOS</a></li>
            <li class="header-item"><a href="#">FANS</a></li>
            <li class="header-item"><a href="#">NEWS</a></li>
            <li class="header-item"><a href="#">SHOP</a></li>
        </ul>
    </header>
</template>


<!-- Aggiungo lo scoped perchè lo stile ci interessa solo per il componente relativo -->
<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables.scss' as *;

header {
    width: 100%;
    height: 120px;
    background-color: white;
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-direction: row;

    .header-image-container {
        width: 80px;
        height: 80px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }

    .header-menu {
        font-size: 14px;
        display: flex;
        align-items: center;
        justify-content: flex-start;
        flex-direction: row;
        gap: 25px;
        list-style-type: none;


        .header-item {

            a {
                font-weight: 700;
                color: black;
            }

            // Da modificare
            &:hover {
                transition: 0.5s;
                padding-bottom: calc(20px);
                border-bottom: 4px solid $primary;
            }
        }
    }
}
</style>
