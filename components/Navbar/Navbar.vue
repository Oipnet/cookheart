<template>
  <nav class="flex items-center justify-between flex-wrap bg-teal-500 p-6">
    <navbar-logo />
    <navbar-toggler @toggle-navbar="handleToggle" />
    <navbar-menu />
  </nav>
</template>

<script>
import NavbarLogo from '~/components/Navbar/NavbarLogo'
import NavbarToggler from '~/components/Navbar/NavbarToggler'
import NavbarMenu from '~/components/Navbar/NavbarMenu'

export default {
  name: 'navbar',
  components: {
    NavbarLogo,
    NavbarToggler,
    NavbarMenu
  },
  data() {
    return {
      open: false
    }
  },
  methods: {
    handleToggle() {
      this.open = !this.open
    }
  }
}
</script>
