<template>
  <b-navbar toggleable="md" type="dark">
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
    <div class="mx-2">
      <b-navbar-brand href="#inicio">NavBar</b-navbar-brand>
      <b-collapse is-nav id="nav_collapse">
        <!-- Right aligned nav items -->
        <b-navbar-nav v-b-scrollspy:nav-scroller class="ml-auto">
          <b-nav-item v-for="item in navItems" :key="item.name" :href="item.link">{{ item.name | capitalize }}</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </div>
  </b-navbar>
</template>

<script>
export default {
  data () {
    return {
      navItems: [
        {name: 'início', link: '#inicio', icon: ''},
        {name: 'sobre', link: '#sobre', icon: ''},
        {name: 'carros', link: '#carros', icon: ''},
        {name: 'galeria', link: '#galeria', icon: ''},
        {name: 'contato', link: '#contato', icon: ''}
      ]
    }
  },
  filters: {
    capitalize: function (value) {
      return value.toUpperCase()
    }
  }
}
</script>

<style>

</style>
