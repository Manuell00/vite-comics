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
            <li class="header-item"><a href="#">CHARACTERS</a>
                <div class="blue"></div>
            </li>
            <li class="header-item"><a href="#">COMICS</a>
                <div class="blue"></div>
            </li>
            <li class="header-item"><a href="#">MOVIES</a>
                <div class="blue"></div>
            </li>
            <li class="header-item"><a href="#">TV</a>
                <div class="blue"></div>
            </li>
            <li class="header-item"><a href="#">GAMES</a>
                <div class="blue"></div>
            </li>
            <li class="header-item"><a href="#">COLLECTIBLES</a>
                <div class="blue"></div>
            </li>
            <li class="header-item"><a href="#">VIDEOS</a>
                <div class="blue"></div>
            </li>
            <li class="header-item"><a href="#">FANS</a>
                <div class="blue"></div>
            </li>
            <li class="header-item"><a href="#">NEWS</a>
                <div class="blue"></div>
            </li>
            <li class="header-item"><a href="#">SHOP</a>
                <div class="blue"></div>
            </li>
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
        height: 100%;


        .header-item {
            height: 100%;
            display: flex;
            align-items: center;
            position: relative;

            .blue {
                background-color: $primary;
                position: absolute;
                height: 8px;
                width: 100%;
                bottom: 0;
                opacity: 0;
                transition: opacity 0.5s ease-in-out;
            }

            a {
                font-weight: 700;
                color: black;
            }

            &:hover .blue {
                opacity: 1;

            }
        }
    }
}
</style>
