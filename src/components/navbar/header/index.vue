<template>
  <header class="main-header">
    <div class="logo">
      <img src="@/icon/logo/logo.png" alt="Logo Aplikasi" class="app-logo">
    </div>
    <div class="spacer"></div>
    <div class="theme-toggle" @click="toggleDarkMode">
      <i class="material-icons">{{ isDarkMode ? 'dark_mode' : 'light_mode' }}</i>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderNavbar',
  props: {
    isDarkMode: Boolean,
    toggleDarkMode: Function,
  },
};
</script>

<style scoped>
.main-header {
  display: flex;
  align-items: center;
  padding: 0.5rem 1rem; /* Padding lebih kecil untuk mobile */
  background-color: var(--surface-container);
  min-height: 50px; /* Gunakan min-height agar bisa menyesuaikan */
  transition: background-color 0.3s, padding 0.3s;
}

.logo {
  font-weight: bold;
  font-size: 1.25rem; /* Ukuran font logo sedikit lebih kecil di mobile */
  color: var(--on-surface);
}

.app-logo {
  height: 35px; /* Ukuran logo lebih kecil */
  width: auto;
  border-radius: 50%;
  object-fit: cover;
}

.spacer {
  flex-grow: 1;
}

.theme-toggle {
  cursor: pointer;
  font-size: 22px; /* Ukuran ikon sedikit lebih kecil */
  color: var(--on-surface);
  display: flex;
  align-items: center;
  justify-content: center;
  width: 35px;
  height: 35px;
  border-radius: 50%;
  border: 1px solid var(--on-surface);
  transition: background-color 0.3s, color 0.3s, border-color 0.3s;
  outline: none; /* Menghilangkan outline fokus */
  -webkit-tap-highlight-color: transparent; /* Menghilangkan highlight biru di mobile */
}

.theme-toggle:hover {
  background-color: var(--theme-toggle-hover-bg);
}

/* Tablet dan layar yang lebih besar */
@media (min-width: 768px) {
  .main-header {
    padding: 1rem 2rem; /* Kembali ke padding semula */
    min-height: 60px; /* Tinggi header lebih besar di desktop */
  }

  .logo {
    font-size: 1.5rem; /* Ukuran font logo normal */
  }

  .app-logo {
    height: 40px; /* Ukuran logo normal */
  }

  .theme-toggle {
    font-size: 24px; /* Ukuran ikon normal */
    width: 40px;
    height: 40px;
  }
}
</style>
