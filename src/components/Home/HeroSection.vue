<template>
  <section
    id="hero"
    class="p-12 px-8  md:px-16 py-28 pt-36 lg:py-28 flex flex-col md:flex-row gap-8 items-center justify-center transition-colors duration-300"
    :class="theme === 'dark' ? 'bg-gray-900 text-white' : 'bg-gray-100 text-gray-800'"
  >
    <div>
      <h1 class="text-4xl font-bold mb-5">Hi, I'm David <span class="wave">👋</span>
      </h1>
      <p class="text-lg text-left max-w-2xl mb-6">
        A frontend developer specializing in Vue.js & React.js, creating fast,
        responsive, and visually appealing digital experiences.
      </p>
      <div class="flex items-center space-x-4">
        <div class="flex items-center">
          <i class="ri-map-pin-2-line text-xl mr-2"></i>
          <span>Lagos, Nigeria</span>
        </div>
        <div class="flex items-center">
          <i class="ri-checkbox-circle-line text-green-500 text-xl mr-2"></i>
          <span>Available for new projects</span>
        </div>
      </div>
      <div class="flex items-center mt-4 space-x-4">
        <a
          href="https://github.com/DavidAkin18" title="Github" target="_blank"
          class="text-gray-400 hover:text-purple-500 text-xl md:text-2xl"
        >
          <i class="ri-github-fill"></i>
        </a>
        <a
          href="https://x.com/Davidakindosu" title="X" target="_blank"
          class="text-gray-400 hover:text-purple-500 text-xl md:text-2xl"
        >
          <i class="ri-twitter-x-line"></i>
        </a>
        <a
          href="https://www.linkedin.com/in/david-akintola-4800001b4/" title="Linkedin" target="_blank"
          class="text-gray-400 hover:text-purple-500 text-xl md:text-2xl"
        >
          <i class="ri-linkedin-fill"></i>
        </a>
        <a
          href="tel:+234 7033576458" target="_blank" title="Phone"
          class="text-gray-400 hover:text-purple-500 text-xl md:text-2xl"
        >
          <i class="ri-phone-fill"></i>
        </a>
      </div>
    </div>
    <div class="w-full lg:w-1/2 flex justify-center">
      <img
        class="object-cover w-80 h-80  rounded-3xl md:rounded-full shadow-lg"
        src="../../assets/hero.jpeg"
        alt="hero"
      />
    </div>
  </section>
</template>

<script>
export default {
  name: "HeroSection",
  props: {
    theme: {
      type: String,
      required: true, // Expecting light or dark mode prop from the parent
    },
  },
};
</script>

<style>
  @keyframes wave-animation {
    0% { transform: rotate(0deg); }
    20% { transform: rotate(20deg); }
    40% { transform: rotate(-10deg); }
    60% { transform: rotate(15deg); }
    80% { transform: rotate(-5deg); }
    100% { transform: rotate(0deg); }
  }

  /* Apply animation */
  .wave {
    display: inline-block;
    animation: wave-animation 1.5s infinite;
  }
</style>
