<template>
  <b-container>
    <app-nav></app-nav>
    <nuxt/>
  </b-container>
</template>

<script>
import NavigationComponent from '~/components/Shared/Navigation.vue'

export default {
  components: {
    'app-nav': NavigationComponent
  }
}
</script>

<style scoped>

</style>
