<template>
    <div :class="theme" class="transition-colors duration-300">
      <Navbar :theme="theme" @toggle-theme="toggleTheme" />
      <main class="">
        <HeroSection :theme="theme"/>
        <About :theme="theme" id="about" />
        <SkillSection :theme="theme" id="skills" />
        <FeaturedProjectsVue :theme="theme" />
        <Footer :theme="theme" id="contact" />
      </main>
    </div>
  </template>
  
  <script>
  import About from './About.vue';
  import Navbar from './Navbar.vue';
  import HeroSection from './HeroSection.vue';
  import SkillSection from './SkillSection.vue';
  import Footer from './Footer.vue';
  import FeaturedProjectsVue from './FeaturedProjects.vue';
  
  export default {
    components: {
      Navbar,
      About,
      HeroSection,
      SkillSection,
      Footer,
      FeaturedProjectsVue,
    },
    data() {
      return {
        theme: 'light', // Default theme
      };
    },
    methods: {
      toggleTheme() {
        this.theme = this.theme === 'light' ? 'dark' : 'light'; // Toggles between light and dark
      },
    },
  };
  </script>
  
  <style>
  .dark {
    @apply bg-gray-900 text-white;
  }
  .light {
    @apply bg-white text-gray-900;
  }
  </style>
  