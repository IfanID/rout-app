<template>
  <footer class="main-footer">
    <nav class="footer-nav">
      <router-link to="/" class="nav-item">
        <i class="material-icons">home</i>
        <span>Home</span>
      </router-link>
      <router-link to="/explore" class="nav-item">
        <i class="material-icons">explore</i>
        <span>Jelajah</span>
      </router-link>
      <router-link to="/features" class="nav-item">
        <i class="material-icons">star</i>
        <span>Fitur</span>
      </router-link>
    </nav>
  </footer>
</template>

<script>
export default {
  name: 'FooterNavbar',
};
</script>

<style scoped>
.main-footer {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: var(--surface-container);
  height: 55px; /* Tinggi lebih kecil untuk mobile */
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
  transition: background-color 0.3s, height 0.3s;
}

.footer-nav {
  display: flex;
  justify-content: space-around;
  width: 100%;
  max-width: 500px;
}

.nav-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-decoration: none;
  color: var(--on-surface);
  font-weight: 500;
  padding: 0 0.5rem; /* Padding horizontal lebih kecil */
  transition: color 0.3s;
  -webkit-tap-highlight-color: transparent; /* Menghilangkan highlight biru di mobile */
}

.nav-item.router-link-exact-active {
  color: var(--primary);
}

.nav-item i {
  font-size: 1.4rem; /* Ukuran ikon sedikit lebih kecil */
  margin-bottom: 0.15rem;
  color: var(--on-surface);
}

.nav-item span {
  font-size: 0.7rem; /* Ukuran teks sedikit lebih kecil */
  color: var(--on-surface);
}

/* Tablet dan layar yang lebih besar */
@media (min-width: 768px) {
  .main-footer {
    height: 60px; /* Kembali ke tinggi semula */
  }

  .nav-item {
    padding: 0 1rem; /* Kembali ke padding semula */
  }

  .nav-item i {
    font-size: 1.5rem; /* Ukuran ikon normal */
    margin-bottom: 0.25rem;
  }

  .nav-item span {
    font-size: 0.75rem; /* Ukuran teks normal */
  }
}

@media (max-width: 360px) {
  .footer-nav {
    max-width: 100%; /* Gunakan lebar penuh di layar sangat kecil */
  }
  .nav-item {
    padding: 0 0.2rem; /* Padding lebih kecil lagi */
  }
}
</style>
