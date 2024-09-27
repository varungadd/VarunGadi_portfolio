<template>
    <div class="min-h-screen bg-gradient-to-r from-green-200 via-blue-200 to-green-300 flex flex-col justify-center items-center px-4">
      <div class="max-w-4xl bg-white shadow-2xl rounded-lg p-10 md:p-20 transform transition hover:scale-105 hover:shadow-2xl duration-500">
        <h1 class="text-6xl font-extrabold text-gray-800 text-center mb-6 leading-tight">About Me</h1>
        <p class="text-2xl mt-6 text-blue-600 text-center font-semibold leading-relaxed">AI Enthusiast & Software Developer</p>
        <p class="mt-4 text-gray-700 text-center text-xl leading-relaxed">I’m Varun Gadi, an AI enthusiast passionate about solving complex real-world problems with cutting-edge technologies.</p>
        
        <div class="mt-8 text-center">
          <!-- Updated Resume Link -->
          <a href="/mnt/data/Varun%20Gadi%20(1)%20(1).pdf" download class="bg-blue-600 hover:bg-blue-800 text-white font-bold py-3 px-8 rounded-full shadow-lg hover:shadow-xl transition duration-300 ease-in-out">Download Resume</a>
        </div>
  
        <!-- Timeline Section -->
        <div class="mt-16">
          <h2 class="text-4xl font-extrabold text-gray-800 text-center mb-10 leading-tight">My Journey</h2>
          <div class="timeline-container space-y-8">
            <div v-for="event in timeline" :key="event.year" class="timeline-item bg-gray-100 p-6 rounded-lg shadow-lg hover:shadow-2xl transition duration-300 ease-in-out">
              <div class="timeline-year text-blue-600 text-2xl font-semibold mb-2">{{ event.year }}</div>
              <div class="timeline-content">
                <h3 class="text-xl font-bold text-gray-800 mb-2">{{ event.title }}</h3>
                <p class="text-gray-700 leading-relaxed">{{ event.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        timeline: [
          { year: "2024", title: "Internship at CodSoft", description: "Worked on AI projects at CodSoft." },
          { year: "2023", title: "AI Chatbot Project", description: "Developed an AI chatbot using NLP and ML." },
          { year: "2022", title: "Started AI Journey", description: "Took AI courses and deepened my skills." },
          { year: "2023", title: "NIT Trichy Project", description: "Worked on a research project at NIT Trichy focusing on AI and deep learning algorithms." },
          { year: "2023", title: "DRDO Project", description: "Collaborated with DRDO on a project involving AI for defense applications." }
        ]
      };
    }
  }
  </script>
  
  <style scoped>
  /* General Styling for Typography and Layout */
  h1 {
    font-family: 'Poppins', sans-serif;
  }
  
  p {
    line-height: 1.75;
  }
  
  /* Timeline Styles */
  .timeline-container {
    margin: 50px 0;
  }
  
  .timeline-item {
    background-color: #f7fafc;
    padding: 20px;
    border-left: 5px solid #6366f1; /* Adding a nice colored border for each item */
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
  }
  
  .timeline-item:hover {
    transform: scale(1.03);
  }
  
  .timeline-year {
    font-weight: bold;
    color: #4c51bf;
    font-size: 1.75rem;
  }
  
  .timeline-content h3 {
    font-size: 1.5rem;
    font-weight: 700;
    color: #2d3748;
  }
  
  .timeline-content p {
    color: #4a5568;
    font-size: 1.125rem;
    line-height: 1.8;
  }
  
  /* Button Enhancements */
  a {
    transition: all 0.3s ease;
  }
  
  a:hover {
    transform: translateY(-2px);
  }
  </style>
  
  <!-- Include Poppins font for more elegant typography -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
  