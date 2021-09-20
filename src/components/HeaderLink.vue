<template>
  <li>
    <a :href="link" :class="classObject">
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
  display: inline-block;
}

a {
  display: block;
  padding: 10px;
  text-decoration: none;
  color: black;
  position:relative;
}

.active::after {
  content: '';
  width: 20px;
  height: 5px;
  border-radius: 5px;
  background-color: black;
  position: absolute;
  bottom: 0;
  left: calc(50% - 10px); /* since width alrd know is 10px, this will send it to the middle */
} 
</style>