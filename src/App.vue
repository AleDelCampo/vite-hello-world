<script>
import AppTitle from './components/AppTitle.vue';
import AppHero from './components/AppHero.vue';
export default {
  components: {
    AppTitle,
    AppHero,
  },
  data() {
    return  {
      variabile: "valore"
    }
  }
}
</script>
<template>
  <AppTitle></AppTitle>
  <AppHero></AppHero>
</template>
<style>
</style>