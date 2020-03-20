<template>
  <a
    href="#responsive-header"
    class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4"
  >
    {{ item.label }}
  </a>
</template>

<script>
export default {
  name: 'navbar-menu-item',
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>
