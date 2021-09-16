<template>
  <div class="header">
    <h1 class="logo">Hy</h1>
    <LinkNav />
  </div>
</template>

<script>
import LinkNav from './LinkNav.vue'

export default {
  name: 'Header',
  components: {
    LinkNav
  }
}
</script>

<style>
.header {
  display: flex;
  width: 100vw;
  justify-content: space-between;
}

.logo {
  margin-left: 10px;
}
</style>