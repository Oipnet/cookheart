<template>
  <div
    :class="open ? 'block' : 'hidden'"
    class="w-full block flex-grow lg:flex lg:items-center lg:w-auto"
  >
    <div class="text-sm lg:flex-grow">
      <navbar-menu-item
        v-for="(item, index) in items"
        :key="index"
        :item="item"
      />
    </div>
    <div>
      <a
        href="#"
        class="inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-teal-500 hover:bg-white mt-4 lg:mt-0"
        >Download</a
      >
    </div>
  </div>
</template>

<script>
import jsonMenu from '~/components/Navbar/menu.json'
import NavbarMenuItem from '~/components/Navbar/NavbarMenuItem'

export default {
  name: 'navbar-menu',
  components: { NavbarMenuItem },
  data() {
    return { items: [] }
  },
  mounted() {
    this.items = jsonMenu
  }
}
</script>
