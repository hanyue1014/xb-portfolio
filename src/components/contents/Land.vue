<template>
  <!-- the landing component (first component they sees) -->
  <div class="component">
    <div class="container">
      <h1>
        Hello!!! I am 
      </h1>
      <span>Xuan Bin</span>
      <h3>A student developer in Penang, Malaysia</h3>
      <button class="learn-btn">Learn More</button>
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

h3 {
  font-size: 2vw;
}

span {
  font-size: 6vw;
  font-weight: bold;
  color: var(--emphasis);
}

.learn-btn {
  /* width: 6vw; */
  /* height: 4vh; */
  padding: 10px;
  margin-top: 10px;
  font-size: 125%;
  text-align: center;
  color: var(--primary);
  background-color: var(--emphasis);
  border: 2px solid var(--primary);
  border-radius: 5px;
  cursor: pointer;
  transition: .5s;
}

.learn-btn:hover {
  background-color: white;
}

</style>