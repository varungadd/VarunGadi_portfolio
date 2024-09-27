<template>
    <div class="min-h-screen bg-gradient-to-r from-pink-50 via-white to-pink-100 flex flex-col justify-center items-center px-4">
      <div class="max-w-lg bg-white shadow-lg rounded-lg p-8 md:p-16 text-center transform transition hover:scale-105 hover:shadow-2xl duration-500">
        <h1 class="text-5xl font-extrabold text-gray-800">Contact Me</h1>
        <p class="mt-6 text-gray-600 text-lg">Feel free to get in touch to discuss potential opportunities, projects, or just say hi!</p>
  
        <!-- Contact Form -->
        <form @submit.prevent="submitForm" class="mt-6 space-y-4">
          <div class="text-left">
            <label for="name" class="block text-sm font-semibold text-gray-700">Your Name</label>
            <input type="text" id="name" v-model="formData.name" required class="mt-1 block w-full p-2 border border-gray-300 rounded-md focus:ring-indigo-500 focus:border-indigo-500" />
          </div>
          <div class="text-left">
            <label for="email" class="block text-sm font-semibold text-gray-700">Your Email</label>
            <input type="email" id="email" v-model="formData.email" required class="mt-1 block w-full p-2 border border-gray-300 rounded-md focus:ring-indigo-500 focus:border-indigo-500" />
          </div>
          <div class="text-left">
            <label for="message" class="block text-sm font-semibold text-gray-700">Your Message</label>
            <textarea id="message" v-model="formData.message" rows="5" required class="mt-1 block w-full p-2 border border-gray-300 rounded-md focus:ring-indigo-500 focus:border-indigo-500"></textarea>
          </div>
          <button type="submit" class="bg-indigo-600 text-white font-bold py-2 px-4 rounded-full hover:bg-indigo-800 transition duration-300">Send Message</button>
        </form>
  
        <!-- Social Media Links with Icons -->
        <div class="social-links flex justify-center mt-8">
          <a href="https://www.linkedin.com/in/varun-gadi-92b86b263/" target="_blank" class="text-blue-600 mx-2">
            <i class="fab fa-linkedin fa-2x"></i>
          </a>
          <a href="https://github.com/varungadd" target="_blank" class="text-gray-900 mx-2">
            <i class="fab fa-github fa-2x"></i>
          </a>
          <a href="https://twitter.com/varungadd" target="_blank" class="text-blue-400 mx-2">
            <i class="fab fa-twitter fa-2x"></i>
          </a>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        formData: {
          name: '',
          email: '',
          message: ''
        }
      };
    },
    methods: {
      submitForm() {
        alert(`Message Sent by ${this.formData.name}!`);
        this.formData.name = '';
        this.formData.email = '';
        this.formData.message = '';
      }
    }
  }
  </script>
  
  <style scoped>
  input, textarea {
    transition: border-color 0.3s ease;
  }
  input:focus, textarea:focus {
    border-color: #6366f1;
  }
  .social-links i {
    transition: transform 0.3s ease;
  }
  .social-links i:hover {
    transform: scale(1.2);
  }
  </style>
  
  <!-- Include Font Awesome for social media icons -->
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet">
  