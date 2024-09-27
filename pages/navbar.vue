<template>
    <nav class="bg-gray-800 text-white p-4">
      <div class="container mx-auto flex justify-between items-center">
        <h1 class="text-lg font-bold">Varun's Portfolio</h1>
        <ul class="flex space-x-4">
          <li><nuxt-link to="/" exact>Home</nuxt-link></li>
          <li><nuxt-link to="/about">About</nuxt-link></li>
          <li><nuxt-link to="/skills">Skills</nuxt-link></li>
          <li><nuxt-link to="/projects">Projects</nuxt-link></li>
          <li><nuxt-link to="/contact">Contact</nuxt-link></li>
        </ul>
      </div>
    </nav>
  </template>
  
  <script>
  export default {};
  </script>
  
  <style scoped>
  nav li a {
    transition: color 0.3s ease;
  }
  
  nav li a:hover {
    color: #f59e0b; /* Tailwind orange-500 */
  }
  </style>
  