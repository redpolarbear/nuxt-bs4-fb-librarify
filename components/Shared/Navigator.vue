<template>
  <b-navbar toggleable="md" variant="faded">
    <b-nav-toggle target="nav_collapse"></b-nav-toggle>
    <b-navbar-brand href="#">Librarify</b-navbar-brand>
    <b-collapse is-nav id="nav_collapse">
      <!-- Right aligned nav items -->
      <b-nav is-nav-bar class="ml-auto">
        <b-nav-item v-for="item in menuItems" :key="item.title" :to="item.link" exact>
          <i class="fa" v-bind:class="item.icon"></i> {{ item.title }}
        </b-nav-item>
      <b-nav-form>
        <b-button size="sm" class="my-2 my-sm-0 mx-2" variant="outline">Log In</b-button>
        <b-button size="sm" class="my-2 my-sm-0 ml-2" variant="info">Sign Up</b-button>
      </b-nav-form>
      </b-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
// import { mapGetters } from 'vuex'
import LoginComponent from '~/components/User/Login'
import SignupComponent from '~/components/User/Signup'

export default {
  name: 'navigator',
  components: {
    'app-login': LoginComponent,
    'app-signup': SignupComponent
  },
  data () {
    return {
    }
  },
  computed: {
    menuItems () {
      let menuItems = [
        { icon: 'fa-home', title: 'Home', link: '/' },
        { icon: 'fa-book', title: 'Library', link: '/library' },
        { icon: 'fa-bolt', title: 'Moments', link: '/moments' },
        { icon: 'fa-envelope', title: 'Messages', link: '/messages' }
      ]
      return menuItems
    }
  }
}
</script>

<style scoped>

</style>
