<script>
export default {
    name: "AppCentral",
}
</script>

<template>
    <!-- Definisco un Header -->
    <header>
        <!-- Inserisco gli header item -->
        <div class="header-item">
            <img src="../../public/img/buy-comics-digital-comics.png" alt="header-item">
            <span>Digital Comics</span>
        </div>

        <div class="header-item">
            <img src="../../public/img/buy-comics-merchandise.png" alt="header-item">
            <span>DC Merchandise</span>
        </div>

        <div class="header-item">
            <img src="../../public/img/buy-comics-subscriptions.png" alt="header-item">
            <span>Subscription</span>
        </div>

        <div class="header-item">
            <img src="../../public/img/buy-comics-shop-locator.png" alt="header-item">
            <span>Comic shop Locator</span>
        </div>

        <div class="header-item">
            <img src="../../public/img/buy-dc-power-visa.svg" alt="header-item">
            <span>DC power Visa</span>
        </div>

    </header>

    <!--Definisco il Main -->
    <main>
        <!-- Colonne testo main -->
        <div class="main-text">
            <ul class="main-text-item">
                <li>
                    <h5>DC COMICS</h5>
                </li>
                <li>Characters</li>
                <li>Comics</li>
                <li>Movies</li>
                <li>TV</li>
                <li>Games</li>
                <li>Videos</li>
                <li>News</li>

                <li>
                    <h5>SHOP</h5>
                </li>
                <li>Shop DC</li>
                <li>Shop DC Collectibles</li>
            </ul>

            <ul class="main-text-item">
                <li>
                    <h5>DC</h5>
                </li>
                <li>Terms Of Use</li>
                <li>Privacy Policy</li>
                <li>Ad Choices</li>
                <li>Advertising</li>
                <li>Jobs</li>
                <li>Subscriptions</li>
                <li>Talent Workshop</li>
                <li>CPSC Certificates</li>
                <li>Ratings</li>
                <li>Shop Help</li>
                <li>Contact Us</li>
            </ul>

            <ul class="main-text-item">
                <li>
                    <h5>SITES</h5>
                </li>
                <li>DC</li>
                <li>MAD MAgazine</li>
                <li>DC Kids</li>
                <li>DC Universe</li>
                <li>DC Power Visa</li>
            </ul>

        </div>

        <!-- Logo DC bg -->
        <div class="logo-bg">
            <img src="../../public/img/dc-logo-bg.png" alt="">
        </div>

    </main>
</template>


<!-- Aggiungo lo scoped perchè lo stile ci interessa solo per il componente relativo -->
<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables.scss' as *;

header {
    height: 150px;
    background-color: $primary;
    padding: 15px 15%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: row;
    gap: 15px;

    .header-item {
        display: flex;
        justify-content: center;
        align-items: center;

        img {
            width: 50px;
            height: 50px;
            display: inline-block;
        }

        span {
            color: white;
            padding-left: 15px;
            text-transform: uppercase;
            font-size: 13px;
        }
    }

}

main {
    height: 350px;
    width: 100%;
    background-image: url(../../public/img/footer-bg.jpg);
    padding: 15px 15%;
    display: flex;
    justify-content: space-between;

    .main-text {
        display: flex;
        flex-direction: row;
        width: auto;
        height: 100%;
        gap: 30px;

        ul {
            list-style-type: none;
            text-align: left;
        }


        h5 {
            margin: 8px 0;
            font-size: 18px;
            color: white;
            text-transform: uppercase;
        }

        li {
            color: grey;
            font-size: 12px;
        }
    }

    .logo-bg {
        height: 100%;
        width: 500px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }


}
</style>