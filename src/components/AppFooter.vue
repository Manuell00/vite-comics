<script>
export default {
    name: "AppFooter",
}
</script>

<template>
    <!-- Inserisco il footer -->
    <footer>
        <div class="footer-container">

            <div class="sign-button">
                <span id="sign-up-button">SIGN-UP NOW!</span>
            </div>

            <div class="social">
                <span>FOLLOW US</span>
                <img src="../../public/img/footer-facebook.png" alt="Facebok">
                <img src="../../public/img/footer-twitter.png" alt="Twitter">
                <img src="../../public/img/footer-youtube.png" alt="YouTube">
                <img src="../../public/img/footer-pinterest.png" alt="Pinterest">
                <img src="../../public/img/footer-periscope.png" alt="Periscope">
            </div>
        </div>
    </footer>
</template>



<!-- Aggiungo lo scoped perchè lo stile ci interessa solo per il componente relativo -->
<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/variables.scss' as *;

.footer-container {
    height: 100px;
    width: 100%;
    background-color: #3f3f3f;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 15%;


    #sign-up-button {
        background-color: transparent;
        color: white;
        border: 1px solid $primary;
        padding: 10px 20px;
        cursor: pointer;
        transition: 0.7s ease-in-out;

        &:hover {
            background-color: $primary;
            padding: 15px 25px;
            cursor: pointer;
        }
    }

    .social {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 10px;


        span {
            color: $primary;
            text-transform: uppercase;
            font-weight: 800;
            font-size: 18px;
            margin-right: 10px;
        }

        img {
            height: 30px;
            width: 30px;
        }
    }
}
</style>