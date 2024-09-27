<template>
  <div class="min-h-screen bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500 text-white">
    <!-- Hero Section -->
    <div class="flex flex-col justify-center items-center h-screen px-4 text-center">
      <h1 class="text-5xl md:text-7xl font-extrabold mb-4">Welcome to My Portfolio</h1>
      <p class="text-lg md:text-2xl font-light mb-8">AI Enthusiast | Software Developer | Tech Explorer</p>
      <div class="space-x-4">
        <!-- Learn More About Me Button -->
        <a href="/about" class="bg-white text-indigo-500 font-bold py-2 px-6 rounded-full hover:bg-gray-200 transition duration-300">
          Learn More About Me
        </a>
        <!-- View My Projects Button -->
        <a href="/projects" class="bg-white text-indigo-500 font-bold py-2 px-6 rounded-full hover:bg-gray-200 transition duration-300">
          View My Projects
        </a>
        <!-- Contact Me Button -->
        <a href="/contact" class="bg-white text-indigo-500 font-bold py-2 px-6 rounded-full hover:bg-gray-200 transition duration-300">
          Contact Me
        </a>
      </div>
    </div>

    <!-- Skills Preview Section -->
    <section class="bg-white text-gray-800 py-16">
      <div class="max-w-6xl mx-auto text-center">
        <h2 class="text-4xl font-extrabold mb-6">What I’m Good At</h2>
        <p class="mb-10 text-lg">Here’s a quick snapshot of my skills.</p>
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
          <div class="p-6 bg-indigo-500 text-white rounded-lg shadow-lg transform hover:scale-105 transition duration-300">
            <h3 class="font-bold text-2xl">AI/ML</h3>
            <p>Machine Learning, TensorFlow, PyTorch</p>
          </div>
          <div class="p-6 bg-purple-500 text-white rounded-lg shadow-lg transform hover:scale-105 transition duration-300">
            <h3 class="font-bold text-2xl">Web Dev</h3>
            <p>HTML, CSS, JavaScript, Vue.js</p>
          </div>
          <div class="p-6 bg-pink-500 text-white rounded-lg shadow-lg transform hover:scale-105 transition duration-300">
            <h3 class="font-bold text-2xl">Programming</h3>
            <p>Python, C++, JavaScript</p>
          </div>a
          <div class="p-6 bg-indigo-500 text-white rounded-lg shadow-lg transform hover:scale-105 transition duration-300">
            <h3 class="font-bold text-2xl">Data Science</h3>
            <p>Data Analysis, Visualization</p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Welcome - Varun Gadi'
    }
  }
}
</script>

<style scoped>
h1 {
  animation: fadeInDown 1s ease-out;
}

@keyframes fadeInDown {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
