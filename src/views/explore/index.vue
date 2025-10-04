<template>
  <div class="explore">
    <h1>Explore</h1>
    <p>Konten di bawah ini ditambahkan untuk tujuan pengujian scroll.</p>
    <div class="content-list">
      <div v-for="n in 50" :key="n" class="list-item">
        Item #{{ n }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ExploreView',
};
</script>

<style scoped>
.explore {
  text-align: center;
  padding: 1rem;
  width: 100%;
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

p {
  margin-bottom: 2rem;
}

.content-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.list-item {
  background-color: var(--surface-container);
  color: var(--on-surface);
  padding: 2rem 1rem;
  border-radius: 8px;
  border: 1px solid var(--outline);
}

@media (max-width: 768px) {
  h1 {
    font-size: 2rem;
  }
}
</style>
