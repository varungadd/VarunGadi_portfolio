<template>
    <div class="min-h-screen bg-gradient-to-b from-green-50 via-white to-green-100 flex flex-col justify-center items-center px-4">
      <div class="max-w-4xl bg-white shadow-2xl rounded-lg p-8 md:p-16 transform transition hover:scale-105 hover:shadow-2xl duration-500">
        <h1 class="text-5xl font-extrabold text-gray-800 text-center">Skills</h1>
        <div class="mt-8 grid grid-cols-1 md:grid-cols-2 gap-6">
          <div>
            <h2 class="text-3xl font-bold text-green-600">Technical Skills</h2>
            <ul class="mt-4 list-disc list-inside text-gray-700 text-lg">
              <li>Python, JavaScript, C++</li>
              <li>Machine Learning and Deep Learning</li>
              <li>Data Analysis with Python</li>
              <li>Frameworks: TensorFlow, PyTorch</li>
              <li>Web Development: HTML, CSS, Vue.js</li>
            </ul>
          </div>
          <div>
            <h2 class="text-3xl font-bold text-green-600">Soft Skills</h2>
            <ul class="mt-4 list-disc list-inside text-gray-700 text-lg">
              <li>Problem Solving and Critical Thinking</li>
              <li>Effective Communication</li>
              <li>Teamwork and Collaboration</li>
              <li>Adaptability and Flexibility</li>
              <li>Leadership and Management</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    head() {
      return {
        title: 'Skills - Varun Gadi'
      }
    }
  }
  </script>
  
  <style scoped>
  ul {
    line-height: 2;
  }
  </style>
  