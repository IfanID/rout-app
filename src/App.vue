<template>
  <HeaderNavbar :isDarkMode="isDarkMode" :toggleDarkMode="toggleDarkMode" />
  <main class="main-content">
    <router-view />
  </main>
  <FooterNavbar />
</template>

<script>
import HeaderNavbar from './components/navbar/header/index.vue';
import FooterNavbar from './components/navbar/footer/index.vue';

export default {
  components: {
    HeaderNavbar,
    FooterNavbar,
  },
  data() {
    return {
      isDarkMode: localStorage.getItem('theme') === 'dark', // Baca dari localStorage
    };
  },
  methods: {
    toggleDarkMode() {
      this.isDarkMode = !this.isDarkMode;
      localStorage.setItem('theme', this.isDarkMode ? 'dark' : 'light'); // Simpan ke localStorage
    },
  },
  watch: {
    isDarkMode(newVal) {
      if (newVal) {
        document.documentElement.classList.add('dark-mode');
      } else {
        document.documentElement.classList.remove('dark-mode');
      }
    },
  },
};
</script>