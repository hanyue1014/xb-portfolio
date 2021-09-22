<template>
  <ul>
    <HeaderLink 
      link="#about" 
      :haveFocus="active == 'abouts'"
      @mouseover="tempChangeActiveState('abouts')"
      @mouseleave="revertActive"
    >
      About
    </HeaderLink>
    <HeaderLink 
      link="#projects" 
      :haveFocus="active == 'projects'"
      @mouseover="tempChangeActiveState('projects')"
      @mouseleave="revertActive"
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
      active: '',
      tempActive: ''
    }
  },
  methods: {
    changeActiveState(focusedNav) {
      // for now I just have two links, so not gonna worry about the reusability
      this.active = focusedNav
    },
    tempChangeActiveState(focusedNav) {
      this.tempActive = this.active
      this.changeActiveState(focusedNav)
    },
    revertActive() {
      if (this.tempActive) {
        this.changeActiveState(this.tempActive)
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