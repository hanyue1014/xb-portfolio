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
  computed: {
    classObject() {
      return {
        active: this.haveFocus
      }
    }
  }
  // data() {
  //   return {
  //     classObject: {
  //       active: this.haveFocus
  //     }
  //   }
  // }
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

a::after {
  content: '';
  width: 0px;
  height: 5px;
  border-radius: 5px;
  background-color: black;
  position: absolute;
  bottom: 0;
  left: calc(50% - 10px); /* send it to middle */
  transition: .1s;
}

.active::after {
  width: 20px; 
} 
</style>