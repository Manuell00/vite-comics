<!-- SCRIPT -->
<script>

// Importo i componenti
import AppHeader from './components/AppHeader.vue'
import AppJumbotron from './components/AppJumbotron.vue'
import AppCentral from './components/AppCentral.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  components: {
    AppHeader,
    AppJumbotron,
    AppCentral,
    AppFooter
  },
}
</script>


<!-- TEMPLATE -->
<template>
  <!-- Inserisco il componente dell'header -->
  <AppHeader />

  <main>
    <!-- Inserisco il componente del jumbotron -->
    <AppJumbotron />

    <!-- Inserisco il componente Centrale del main -->
    <AppCentral />

  </main>

  <footer>
    <!-- Inserisco il componente del footer -->
    <AppFooter />
  </footer>
</template>



<!-- STYLE -->
<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;


h1,
h2,
h3,
h4,
h5,
h6 {
  color: $primary;
}
</style>
