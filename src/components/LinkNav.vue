<template>
  <ul>
    <HeaderLink link="#about">About</HeaderLink>
    <HeaderLink link="#projects">Projects</HeaderLink>
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
  /* margin-right: 10px;  actually not what i wanna achieve*/
}
</style>