<template>
  <nav
    :class="[
      'flex fixed top-0 z-50 lg:px-16  w-full justify-between items-center p-5 shadow-md transition-colors duration-300',
      theme === 'dark' ? 'bg-gray-800 text-white' : 'bg-white text-gray-800'
    ]"
  >
    <div class="text-2xl font-bold">
      David Akintola
    </div>
    <!-- Desktop Navigation -->
    <ul class="hidden md:flex space-x-5">
      <li>
        <a href="#hero" class="hover:underline">Home</a>
      </li>
      <li>
        <a href="#about" class="hover:underline" @click.prevent="scrollTo('about')">About</a>
      </li>
      <li>
        <a href="#skills" class="hover:underline" @click.prevent="scrollTo('skills')">Skills</a>
      </li>
      <li>
        <a href="#contact" class="hover:underline" @click.prevent="scrollTo('contact')">Contact</a>
      </li>
      <button
        @click="$emit('toggle-theme')"
        :class="[
          'transition-colors duration-300',
          theme === 'dark' ? 'text-white' : 'text-gray-800'
        ]"
      >
        <i v-if="theme === 'dark'" class="ri-sun-fill text-lg"></i>
        <i v-else class="ri-moon-fill text-lg"></i>
      </button>
      <li>
        <a 
          href="/david.pdf" 
          download 
          class="hover:underline rounded-lg p-2"
          :class="[
            'transition-colors duration-300',
            theme === 'dark' ? 'bg-gray-100 text-gray-800' : 'bg-gray-800 text-gray-100'
          ]"
        >
          Download CV
        </a>
      </li>
    </ul>

    <!-- Mobile Menu Toggle -->
    <button
      class="md:hidden text-2xl"
      @click="toggleSidebar"
    >
      <i :class="theme === 'dark' ? 'ri-menu-line text-white' : 'ri-menu-line text-gray-800'"></i>
    </button>

    <!-- Sidebar -->
    <div
      v-if="isSidebarOpen"
      class="fixed inset-0 bg-black bg-opacity-50 z-40"
      @click="closeSidebar"
    ></div>
    <div
      :class="[
        'fixed top-0 right-0 h-full z-50 w-1/2 bg-gray-100 shadow-lg transition-transform duration-300',
        isSidebarOpen ? 'translate-x-0' : 'translate-x-full',
        theme === 'dark' ? 'bg-gray-800 text-white' : 'bg-white text-gray-800'
      ]"
    >
      <div class="flex justify-between items-center p-5">
        <div class="text-xl font-bold">Menu</div>
        <button @click="toggleSidebar" class="text-2xl">
          <i :class="theme === 'dark' ? 'ri-close-line text-white' : 'ri-close-line text-gray-800'"></i>
        </button>
      </div>
      <ul class="space-y-4 p-5">
        <li>
          <a href="#hero" class="hover:underline" @click.prevent="closeSidebarAndScroll('hero')">Home</a>
        </li>
        <li>
          <a href="#about" class="hover:underline" @click.prevent="closeSidebarAndScroll('about')">About</a>
        </li>
        <li>
          <a href="#skills" class="hover:underline" @click.prevent="closeSidebarAndScroll('skills')">Skills</a>
        </li>
        <li>
          <a href="#contact" class="hover:underline" @click.prevent="closeSidebarAndScroll('contact')">Contact</a>
        </li>
        <li>
          <a 
            href="/david.pdf" 
            download 
            class="hover:underline rounded-lg p-2"
            :class="[
              'transition-colors duration-300',
              theme === 'dark' ? 'bg-gray-100 text-gray-800' : 'bg-gray-800 text-gray-100'
            ]"
          >
            Download CV
          </a>
        </li>
        <button
          @click="$emit('toggle-theme')"
          :class="[
            'transition-colors underline-offset-0 duration-300 w-full text-left',
            theme === 'dark' ? 'text-white' : 'text-gray-800'
          ]"
        >
          <i v-if="theme === 'dark'" class="ri-sun-fill text-lg mr-2"></i>
          <i v-else class="ri-moon-fill text-lg mr-2"></i>
          Toggle Theme
        </button>
      </ul>
    </div>
  </nav>
</template>


<script>
export default {
  name: 'Navbar',
  props: {
    theme: {
      type: String,
      required: true, // Parent must pass the current theme (light or dark)
    },
  },
  data() {
    return {
      isSidebarOpen: false,
    };
  },
  methods: {
    scrollTo(sectionId) {
      const section = document.getElementById(sectionId);
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
      }
    },
    toggleSidebar() {
      this.isSidebarOpen = !this.isSidebarOpen;
    },
    closeSidebar() {
      this.isSidebarOpen = false;
    },
    closeSidebarAndScroll(sectionId) {
      this.closeSidebar();
      this.scrollTo(sectionId);
    },
  },
};
</script>
