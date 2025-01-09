<template>
  <section
    id="skills"
    :class="[
      'p-12 px-8 w-full md:px-16 py-28 lg:py-28 transition-colors duration-300',
      theme === 'dark' ? 'bg-gray-900 text-white' : 'bg-gray-100 text-gray-900'
    ]"
  >
    <!-- Section Header -->
    
    <h2 class="text-xl font-bold text-gray-700 mb-8 text-center"
      :class="theme=== 'dark' ? 'text-white' : 'text-gray-900'"  
    >
      The skills, tools and technologies i am really good at:
    </h2>

    <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-5 gap-6 place-items-center">
      <!-- Skills with Icons -->
      <div
        v-for="skill in skills"
        :key="skill.name"
        :class="[
          'flex flex-col items-center gap-2 p-5 rounded shadow transition-colors duration-300',
          theme === 'dark' ? 'bg-gray-700 text-white' : 'bg-gray-100 text-gray-900'
        ]"
      >
        <img
          :src="skill.icon"
          :alt="skill.name"
          class="w-12 h-12 object-contain"
        />
        <p class="text-center text-sm font-medium">{{ skill.name }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SkillsSection',
  props: {
    theme: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      skills: [
        { name: 'JavaScript', icon: require('@/assets/icons/javascript.svg') },
        { name: 'TypeScript', icon: require('@/assets/icons/typescript.svg') },
        { name: 'HTML5', icon: require('@/assets/icons/html.svg') },
        { name: 'Vue.js', icon: require('@/assets/icons/vue.svg') },
        { name: 'React.js', icon: require('@/assets/icons/react.svg') },
        { name: 'Figma', icon: require('@/assets/icons/figma.svg') },
        { name: 'TailwindCSS', icon: require('@/assets/icons/tailwind.svg') },
        { name: 'CSS', icon: require('@/assets/icons/css.svg') },
        { name: 'Git', icon: require('@/assets/icons/git.svg') },
        { name: 'Bootstrap', icon: require('@/assets/icons/bootstrap.svg') },
        
      ],
    };
  },
};
</script>

<style scoped>
/* Ensures the icons and grid are responsive and well-spaced */
.grid {
  align-items: center;
}
</style>
