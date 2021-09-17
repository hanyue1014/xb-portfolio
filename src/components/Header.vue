<template>
  <div class="header">
    <h1 class="logo">Hy</h1>
    <LinkNav />
    <Profile />
  </div>
</template>

<script>
import LinkNav from './LinkNav.vue'
import Profile from './Profile.vue'

export default {
  name: 'Header',
  components: {
    LinkNav,
    Profile
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