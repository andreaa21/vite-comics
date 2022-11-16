<script>

import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import ComponenteAggiuntivo from './components/ComponenteAggiuntivo.vue'
import AppJumbo from './components/AppJumbo.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    ComponenteAggiuntivo,
    AppJumbo
  }
}
</script>

<template>
  <AppHeader />
  <AppJumbo />
  <AppMain />
  <Componente-Aggiuntivo />
  <AppFooter />
</template>



<style lang="scss">
  @use './styles/general.scss';
</style>