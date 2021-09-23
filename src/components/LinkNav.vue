<template>
  <ul>
    <HeaderLink 
      link="#about" 
      :haveFocus="focused('abouts')"
      @mouseover="tempChangeActiveState('abouts')"
      @mouseleave="revertActive"
      @click="setActive('abouts')"
    >
      About
    </HeaderLink>
    <HeaderLink 
      link="#projects" 
      :haveFocus="focused('projects')"
      @mouseover="tempChangeActiveState('projects')"
      @mouseleave="revertActive"
      @click="setActive('projects')"
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
      tempActive: '',
      persistActive: '' // store which was persisted
    }
  },
  methods: {
    changeActiveState(focusedNav) {
      this.active = focusedNav
    },
    tempChangeActiveState(focusedNav) {
      this.tempActive = this.active
      this.changeActiveState(focusedNav)
    },
    revertActive() {
      // if there was already something that needs to be persisted, remain it
      if (this.persistActive) {
        this.changeActiveState(this.persistActive)
      } else {
        this.changeActiveState(this.tempActive)
        this.tempActive = ''
      }
    },
    setActive(clickedNav) {
      this.persistActive = clickedNav
      this.persist = true
    },
    focused(navToCheck) {
      return this.active == navToCheck 
    }
  }
  // decided that methods does a bttr job than this
  // computed: {
  //   focused() {
  //     return this.active == ''
  //   }
  // }
}
</script>

<style scoped>
ul {
  list-style: none;
}
</style>