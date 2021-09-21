<template>
  <ul>
    <HeaderLink 
      link="#about" 
      :haveFocus="active == 'abouts'"
      @mouseover="changeActiveState"
    >
      About
    </HeaderLink>
    <HeaderLink 
      link="#projects" 
      :haveFocus="active == 'projects'"
      @mouseover="changeActiveState"
    >
      Projects
    </HeaderLink>
  </ul>
</template>

<script>
import HeaderLink from './HeaderLink.vue'

export default {
  name: 'LinkNav',
  components: {
    HeaderLink
  },
  data() {
    return {
      active: ''
    }
  },
  methods: {
    changeActiveState() {
      // for now I just have two links, so not gonna worry about the reusability
      if (this.active == 'abouts') {
        this.active = 'projects'
      } else {
        this.active = 'abouts'
      }
    }
  }
}
</script>

<style scoped>
ul {
  list-style: none;
}
</style>