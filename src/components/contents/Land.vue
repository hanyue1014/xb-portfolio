<template>
  <!-- the landing component (first component they sees) -->
  <div class="component">
    <div class="container">
      <h1>
        Hello!!! I am 
      </h1>
      <span>Xuan Bin</span>
      <h3>A student developer in Penang, Malaysia</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Land'
}
</script>

<style scoped>
.component {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.container {
  margin-left: 40px;
}

h1 {
  font-size: 4vw;
}

span {
  font-size: 6vw;
  font-weight: bold;
}

span {
  color: rgb(0, 156, 204);
}
</style>