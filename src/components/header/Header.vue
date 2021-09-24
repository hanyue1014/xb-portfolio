<template>
  <div class="header">
    <h1 class="logo">Hy</h1>
    <LinkNav />
    <Profile />
  </div>
</template>

<script>
import LinkNav from './links/LinkNav.vue'
import Profile from '../header/Profile.vue'

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
  position: absolute;
  margin: 10px 0px;
  justify-content: space-between;
}

.logo {
  margin-left: 15px;
}
</style>