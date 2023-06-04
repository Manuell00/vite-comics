<script>
// Importo i componenti
import AppCards from './AppCards.vue'

export default {
    name: "AppJumbotron",

    components: {
        AppCards
    },


    // Inserisco i dati
    data() {
        return {
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    }
}
</script>

<template>
    <!-- Definisco il Jumbotron -->
    <div id="jumbotron">
        <div class="bg-container">
            <img src="../../public/img/jumbotron.jpg" alt="">
            <span id="current-series">CURRENT SERIES</span>
        </div>

        <!-- Definisco il contenitore delle cards -->
        <div class="cards-container">

            <!-- Inserisco le carte prendendole dal componente AppCards -->
            <AppCards v-for="(card, index) in comics" :key="index" :details="card" />

            <!-- Definisco la linea per il button LOAD MORE -->
            <div id="load">
                <span id="load-button">LOAD MORE</span>
            </div>
        </div>
    </div>
</template>


<!-- Aggiungo lo scoped perchè lo stile ci interessa solo per il componente relativo -->
<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables.scss' as *;

#jumbotron {
    width: 100%;
    height: auto;


    .bg-container {
        height: 400px;
        width: 100%;
        position: relative;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }

        #current-series {
            padding: 10px;
            color: white;
            background-color: $primary;
            font-size: 28px;
            font-weight: 800;
            position: absolute;
            bottom: -20px;
            left: 15%;
        }
    }

    .cards-container {
        padding: 20px 15%;
        background-color: black;
        height: auto;
        width: 100%;
        display: flex;
        align-items: flex-start;
        justify-content: space-between;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 20px;

        #load {
            height: auto;
            width: 100%;
            text-align: center;
            margin-top: 50px;

            #load-button {
                color: white;
                background-color: $primary;
                padding: 5px 45px;
            }
        }
    }
}
</style>