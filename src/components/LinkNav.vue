<template>
  <ul>
    <HeaderLink link="#about" :haveFocus="true">About</HeaderLink>
    <HeaderLink link="#projects" :haveFocus="false">Projects</HeaderLink>
  </ul>
</template>

<script>
import HeaderLink from './HeaderLink.vue'

export default {
  name: 'LinkNav',
  components: {
    HeaderLink
  }
}
</script>

<style scoped>
ul {
  list-style: none;
}
</style>