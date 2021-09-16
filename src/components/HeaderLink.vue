<template>
  <li>
    <a href="{{ link }}">
      <slot>Default</slot>
    </a>
  </li>
</template>

<script>
export default {
  name: 'HeaderLink',
  props: {
    link: String
  }
}
</script>

<style scoped>
li {
  display: inline;
}

a {
  display: inline-block;
  padding: 10px;
}
</style>