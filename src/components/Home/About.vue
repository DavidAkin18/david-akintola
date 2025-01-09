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
        class="object-cover w-80 h-80 rounded-lg shadow-lg"
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
      <h2 class="text-3xl font-bold mb-5">Curious about me? Here you have it:</h2>
      <p class="text-lg mb-4">
        I'm a passionate frontend developer specializing in Vue.js, React.js and creating fast, 
        responsive, and visually appealing digital experiences.
        With a keen eye for design and a focus on delivering accessible solutions, I love building 
        modern web applications that users enjoy.
      </p>
      <p class="text-lg mb-4">
        I began my journey as a developer in 2020 and have continued to grow with new technologies 
        like Vue.js, TailwindCSS, and more. When
        I'm not coding, you can find me exploring new ideas or sharing insights with the community.
      </p>
      <ul class="text-lg list-disc pl-5">
        <li>Full-time freelancer</li>
        <li>Avid learner</li>
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
