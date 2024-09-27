<template>
    <div class="bg-gradient-to-b from-purple-100 via-white to-purple-300 min-h-screen pt-12 md:pt-20 pb-6 px-2 md:px-0">
      <header class="max-w-lg mx-auto">
        <h1 class="text-5xl font-extrabold text-center text-gray-800">My Projects</h1>
        <p class="text-lg text-center text-gray-600 mt-2">A showcase of my work, focusing on innovative solutions and technical advancements.</p>
      </header>
  
      <!-- Filter Buttons -->
      <div class="text-center my-6">
        <button @click="filterProjects('All')" class="py-2 px-4 rounded bg-gray-500 text-white mx-2 hover:bg-gray-600 transition">Show All</button>
        <button @click="filterProjects('AI')" class="py-2 px-4 rounded bg-indigo-500 text-white mx-2 hover:bg-indigo-600 transition">AI Projects</button>
        <button @click="filterProjects('Web Development')" class="py-2 px-4 rounded bg-purple-500 text-white mx-2 hover:bg-purple-600 transition">Web Development</button>
        <button @click="filterProjects('Other')" class="py-2 px-4 rounded bg-pink-500 text-white mx-2 hover:bg-pink-600 transition">Other Projects</button>
      </div>
  
      <!-- Project Cards -->
      <main class="mt-12 mx-auto max-w-7xl px-4 sm:mt-16">
        <div class="grid gap-12 grid-cols-1 md:grid-cols-2 xl:grid-cols-3">
          <div v-for="project in filteredProjects" :key="project.name" class="relative bg-white p-6 rounded-lg shadow-lg transform transition hover:scale-105 hover:shadow-2xl duration-500">
            <div v-if="project.new" class="absolute -top-4 -right-4 bg-green-400 text-white text-sm font-semibold px-2 py-1 rounded-full">New</div>
            <h2 class="text-xl font-bold text-gray-800">{{ project.name }}</h2>
            <p class="text-gray-600 mt-2">{{ project.description }}</p>
            <a :href="project.link" class="mt-3 text-blue-500 hover:text-blue-700 font-semibold">View on GitHub →</a>
          </div>
        </div>
      </main>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        projects: [
          { name: "AI Chatbot", category: "AI", description: "Developed an AI-powered chatbot using NLP and machine learning techniques.", link: "https://github.com/varungadd/ai-chatbot", new: true },
          { name: "Stock Simulator", category: "Web Development", description: "Built a stock market simulator that allows users to simulate buying and selling stocks with real-time data.", link: "https://github.com/varungadd/StockSimulator", new: true },
          { name: "Health Meals", category: "Web Development", description: "Developed a healthy meal recommender using Flask and integrated it with an external API.", link: "https://github.com/varungadd/Health-Meals" },
          { name: "Data Structures and Algorithms in C++", category: "Other", description: "Focused on solving complex problems by developing and optimizing data structures and algorithms in C++.", link: "https://github.com/varungadd/dsa-projects" },
          { name: "Monitoring Motor Skills in Infants", category: "AI", description: "Created a system to monitor motor skill development in infants using computer vision techniques.", link: "https://github.com/varungadd/Monitoring-Motar-Skills-in-Infants" },
          { name: "Machine Learning Model for Disease Prediction", category: "AI", description: "Built a machine learning model to predict diseases based on patient data.", link: "https://github.com/varungadd/disease-prediction" },
          { name: "E-commerce Website Development", category: "Web Development", description: "Developed a fully functional e-commerce website using Vue.js and Node.js.", link: "https://github.com/varungadd/ecommerce-site" }
        ],
        filter: 'All'
      };
    },
    computed: {
      filteredProjects() {
        if (this.filter === 'All') return this.projects;
        return this.projects.filter(project => project.category === this.filter);
      }
    },
    methods: {
      filterProjects(category) {
        this.filter = category;
      }
    }
  }
  </script>
  
  <style scoped>
  a:hover {
    text-decoration: underline;
  }
  </style>
  