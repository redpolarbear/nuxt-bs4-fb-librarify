<template>
  <b-container>
    <app-nav></app-nav>
    <router-view></router-view>
  </b-container>
</template>

<script>
import Navigator from '~/components/Shared/Navigator.vue'

export default {
  components: {
    'app-nav': Navigator
  }
}
</script>

<style scoped>

</style>
