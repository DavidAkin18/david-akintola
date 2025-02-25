<template>
  <section :class="[theme === 'dark' ? 'bg-gray-800 text-gray-200' : 'bg-gray-200 text-gray-900']" 
  class="  md:px-16 py-28 lg:py-28 ">
    <div class="max-w-7xl mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-8">Featured Projects</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 md:gap-4 lg:gap-8">
        <!-- Project Cards -->
        <div
          v-for="(project, index) in projects"
          :key="index"
          :class="[
            'p-6 rounded-lg shadow-lg transition-colors duration-300',
            theme === 'dark' ? 'bg-gray-900' : 'bg-gray-200'
          ]"
        >
          <img
            :src="project.image"
            :alt="project.title"
            class="w-full rounded mb-4"
          />
          <h3 class="text-lg font-bold mb-2">{{ project.title }}</h3>
          <p class="text-sm mb-4">{{ project.description }}</p>
          <div class="flex gap-2 items-center justify-between">
            <a
              :href="project.liveLink"
              target="_blank"
              :class="[
                'py-2 px-4 rounded transition-colors duration-300',
                theme === 'dark' ? 'bg-purple-600 hover:bg-purple-700 text-white' : 'bg-purple-500 hover:bg-purple-600 text-white'
              ]"
            >
              View Live
            </a>
            <a
              :href="project.repoLink"
              target="_blank"
              :class="[
                'py-2 px-4  rounded transition-colors duration-300 ',
                theme === 'dark' ? 'bg-gray-700 hover:bg-gray-600 text-white' : 'bg-gray-400 hover:bg-gray-300 text-gray-900'
              ]"
            >
              GitHub Repo
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ecommerce from '@/assets/images/ecommerce.png'
import multistep from '@/assets/images/multistep_form.png'
import restorant from '@/assets/images/restorant.png'
import socialMedia from '@/assets/images/socialmedia.png'
import rock from '@/assets/images/rock.png'
import weather from '@/assets/images/weather.png'
import tic from '@/assets/images/x&o.png'
import todo from '@/assets/images/todo.png'
import toro from '@/assets/images/toro.png'
import age from '@/assets/images/age.png'
import fraser from '@/assets/images/fraser.png'
import calculator from '@/assets/images/calculator.png'
import multiStep from '@/assets/images/multisetp.png'
export default {
  name: "FeaturedProjects",
  props: {
    theme: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      projects: [
        {
          title: "E-Commerce",
          description: "An engaging e-commerce platform built with HTML, CSS, JavaScript, and Vue.js, leveraging APIs for seamless functionality and interactivity.",
          image: ecommerce,
          liveLink: "https://shop-co-ecommerce.vercel.app/",
          repoLink: "https://github.com/DavidAkin18/shop.co-ecommerce",
        },
        {
          title: "Multi Step Form ",
          description: "A dynamic multi-step form built with Vue.js, offering a seamless user experience through interactive steps, validation, and modern design.",
          image: multistep,
          liveLink: "https://multi-step-form-livid-psi.vercel.app/",
          repoLink: "https://github.com/DavidAkin18/multi-step-form",
        },
        {
          title: "Restaurant",
          description: "A modern restaurant landing page built with Vue.js and Tailwind CSS, showcasing the menu, services, and online reservation platform.",
          image: restorant,
          liveLink: "https://afro-fusion.vercel.app/#/",
          repoLink: "https://github.com/DavidAkin18/Afro_fusion",
        },
        {
          title: "Project Title 4",
          description: "A Social media platform just like X for posting liking, this require lot of extension as well as html, tailwind, css and javascript",
          image: socialMedia,
          liveLink: "https://bezal-seven.vercel.app/#/",
          repoLink: "https://github.com/DavidAkin18/bezal",
        },
        {
          title: "To-Do List",
          description: "A modern, responsive to-do list app built with Vue.js, Tailwind CSS, and JavaScript, featuring dark/light modes for efficient task tracking and management.",
          image: todo,
          liveLink: "https://to-do-list-seven-bay.vercel.app/",
          repoLink: "https://github.com/DavidAkin18/ToDo-list",
        },
        {
          title: "Cosmetic E-Commerce",
          description: "A cosmetic e-commerce platform built with Vue.js, HTML, CSS, and Tailwind, enabling users to place orders and connect directly with the owner via WhatsApp.",
          image: toro,
          liveLink: "https://house-of-tora.vercel.app/#/",
          repoLink: "https://github.com/DavidAkin18/house_of_tora",
        },
        {
          title: "Tic Tac Toe",
          description: "I developed a responsive Tic Tac Toe game using HTML, CSS, and JavaScript, featuring dynamic gameplay, intuitive design, and seamless user experience.",
          image: tic,
          liveLink: "https://tic-tac-toe-three-henna.vercel.app/",
          repoLink: "https://github.com/DavidAkin18/tic-tac-toe",
        },
        {
          title: "Rock Paper Scissors",
          description: "I created a dynamic Rock-Paper-Scissors game using HTML, CSS, and JavaScript, featuring interactive gameplay, real-time result display, and a user-friendly interface.",
          image: rock,
          liveLink: "https://rock-paper-scissors-v35j.vercel.app/computer.html",
          repoLink: "https://github.com/DavidAkin18/rock-paper-scissors",
        },
        {
          title: "Weather Api",
          description: "I built a weather application using HTML, CSS, and JavaScript, incorporating an API to fetch real-time weather data, display conditions, and ensure user-friendly interaction.",
          image: weather,
          liveLink: "https://weather-topaz-sigma.vercel.app/",
          repoLink: "https://github.com/DavidAkin18/weather_API",
        },
        {
          title: "Age Calculator",
          description: "An interactive Age Calculator using HTML, CSS, and JavaScript, allowing users to input their birthdate and calculate age in years, months, and days.",
          image: age,
          liveLink: "https://age-calculator-giw4.vercel.app/",
          repoLink: "https://github.com/DavidAkin18/age-calculator"
        },
        {
          title: "Multi Step Form",
          description: "I created a multi-step form with HTML, CSS, and JavaScript, featuring checkboxes, radio buttons, text inputs, email fields, and a submit button for seamless user interaction.",
          image: multiStep,
          liveLink: "https://multi-step-form-livid-psi.vercel.app/",
          repoLink: "https://github.com/DavidAkin18/multi-step-form",
        },
        // {
        //   title: "Project Title 12",
        //   description: "A calculator built using HTML, CSS, and JavaScript that supports addition, subtraction, multiplication, division, and decimal calculations for accuracy.",
        //   image: calculator,
        //   liveLink: "https://calculator-as1q.vercel.app/",
        //   repoLink: "https://github.com/DavidAkin18?tab=repositories",
        // },
        {
          title: "Fraser Consulting",
          description: "Fraser Consulting offers expert solutions in international consulting, contract facilitation, project management, and more. Serving industries like Oil & Gas, Aviation, and Finance with exceptional expertise.",
          image: fraser,
          liveLink: "https://fraser-consultance.vercel.app/#/",
          repoLink: "https://github.com/DavidAkin18/fraserConsultance",
        },
      ],
    };
  },
};
</script>
