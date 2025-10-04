<template>
  <div class="home">
    <h1>Home</h1>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
};
</script>

<style scoped>
.home {
  text-align: center;
}

h1 {
  font-size: 2.5rem;
}

@media (max-width: 768px) {
  h1 {
    font-size: 2rem;
  }
}
</style>