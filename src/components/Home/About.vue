<template>
  <section
    id="about"
    :class="[
      'p-12 px-8 md:px-16 py-28 lg:py-28 flex flex-col lg:flex-row gap-8 items-center justify-center transition-colors duration-300',
      theme === 'dark' ? 'bg-gray-800 text-white' : 'bg-gray-200 text-gray-900'
    ]"
  >
    <!-- Image Section -->
    <div class="w-full lg:w-1/2 flex justify-center">
      <img
        src="../../assets/hero1.jpeg"
        alt="About Me"
        class="object-contain w-90 h-90 rounded-lg shadow-lg"
      />
    </div>

    <!-- Text Section -->
    <div class="w-full lg:w-1/2">
      <!-- Header -->
      <div class="mb-5">
        <span
          :class="[
            'px-4 py-2 rounded-full text-sm font-semibold tracking-wider uppercase',
            theme === 'dark' ? 'bg-gray-700 text-gray-300' : 'bg-gray-300 text-gray-700'
          ]"
        >
          About me
        </span>
      </div>
      <h2 class="text-3xl font-bold mb-5">Get to know me:</h2>
      <p class="text-lg mb-4">
        I’m a frontend developer with a passion for crafting dynamic, responsive, and user-friendly digital experiences. My expertise lies in modern web technologies such as Vue.js, React.js, Typescript, Github, CSS, HTML5, restful API and TailwindCSS, enabling me to build solutions that are both visually engaging and performance-driven.
      </p>
      <p class="text-lg mb-4">
        Since starting my development journey in 2020, I have continuously honed my skills, staying at the forefront of emerging tools and technologies. Beyond coding, I enjoy exploring innovative ideas and actively engaging with the tech community to share knowledge and insights.
      </p>
      <ul class="text-lg list-disc pl-5">
        <li>Dedicated full-time/freelancer</li>
        <li>Lifelong learner with a passion for growth</li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection',
  props: {
    theme: {
      type: String,
      required: true,
    },
  },
};
</script>
