<template>
  <li>
    <a href="{{ link }}" :class="classObject">
      <slot>Default</slot>
    </a>
  </li>
</template>

<script>
export default {
  name: 'HeaderLink',
  props: {
    link: String,
    haveFocus: Boolean
  },
  data() {
    return {
      classObject: {
        active: this.haveFocus
      }
    }
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
  text-decoration: none;
  color: black;
}

/* a.active::after {
  width: 50%;
  height: 5px;
  border-radius: 5000000px;
  background-color: black;
} not currently working */
</style>