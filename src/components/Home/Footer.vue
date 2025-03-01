<template>
  <footer
    :class="[theme === 'dark' ? 'bg-gray-900 text-black-500' : 'bg-gray-800 text-gray-900']"
    class="p-12 px-8 md:px-16 py-28  text-center transition-colors duration-300 border-t"
  >
    <div class="max-w-7xl mx-auto px-4">
      <div class="flex justify-center space-x-6 mb-4">
        <a
          href="https://www.linkedin.com/in/david-akintola-4800001b4/" target="_blank" title="Linkedin"
          :class="[
            'text-lg md:text-2xl transition-colors duration-300',
            theme === 'dark' ? 'text-gray-400 hover:text-purple-500' : 'text-gray-50 hover:text-purple-600'
          ]"
        >
          <i class="ri-linkedin-box-line"></i>
        </a>
        <a
          href="https://wa.me/qr/R7XJHRWA4GRYC1" target="_blank" title="Whatsapp"
          :class="[
            'text-lg md:text-2xl transition-colors duration-300',
            theme === 'dark' ? 'text-gray-400 hover:text-purple-500' : 'text-gray-50 hover:text-purple-600'
          ]"
        >
          <i class="ri-whatsapp-fill"></i>
        </a>
        
        <a
          href="https://x.com/Davidakindosu" target="_blank" title="X"
          :class="[
            'text-lg md:text-2xl transition-colors duration-300',
            theme === 'dark' ? 'text-gray-400 hover:text-purple-500' : 'text-gray-50 hover:text-purple-600'
          ]"
        >
          <i class="ri-twitter-x-line"></i>
        </a>
        <a
          href="https://github.com/DavidAkin18" target="_blank" title="Github"
          :class="[
            'text-lg md:text-2xl transition-colors duration-300',
            theme === 'dark' ? 'text-gray-400 hover:text-purple-500' : 'text-gray-50 hover:text-purple-600'
          ]"
        >
          <i class="ri-github-fill"></i>
        </a>
        <a
          href="mailto:akindayodavid22@gmail.com" target="_blank" title="Email"
          :class="[
            'text-lg md:text-2xl transition-colors duration-300',
            theme === 'dark' ? 'text-gray-400 hover:text-purple-500' : 'text-gray-50 hover:text-purple-600'
          ]"
        >
          <i class="ri-mail-line"></i>
        </a>
        <a
          href="tel:+234 7033576458" target="_blank" title="Phone"
          :class="[
            'text-lg md:text-2xl transition-colors duration-300',
            theme === 'dark' ? 'text-gray-400 hover:text-purple-500' : 'text-gray-50 hover:text-purple-600'
          ]"
        >
          <i class="ri-phone-fill"></i>
        </a>
      </div>
      <p class="text-sm"
        :class="[
          'text-2xl transition-colors duration-300',
          theme === 'dark' ? 'text-gray-100 ' : 'text-gray-50 '
        ]"
      >
        © 2025 David Akindayo Akintola · Frontend Developer 
      </p>
      <p class="text-xs mt-2"
        :class="[
          'text-2xl transition-colors duration-300',
          theme === 'dark' ? 'text-gray-100 ' : 'text-gray-50 '
        ]"
      >Designed by @dayoAkin </p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
    theme: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
/* Add any additional scoped styles if needed */
</style>
