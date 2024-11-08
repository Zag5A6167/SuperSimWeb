<script setup>
import { ref } from 'vue'
import RandomNumber from './components/RandomNumber.vue'
import DarkMode from './components/DarkMode.vue'

const currentPage = ref('home')

const switchPage = (page) => {
  currentPage.value = page
}


</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand hover-effect" href="#" @click="switchPage('home')">SuperSim Web</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav">
          <!-- Main Navigation -->
          <li class="nav-item">
            <a class="nav-link active" href="#" @click="switchPage('home')">Home</a>
          </li>
          
          <!-- More Navigation -->
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              More
            </a>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#" @click="switchPage('home')">Home</a></li>
              <li><a class="dropdown-item" href="#" @click="switchPage('RandomNumber')">Random Number</a></li>
            </ul>
          </li>
        </ul>
       
        <DarkMode />
      </div>
    </div>
  </nav>

  <!-- Add this section to display components -->
  <div class="container mt-3">
    <div v-if="currentPage === 'home'">
      <h1>Welcome to Home Page</h1>
    </div>
    <RandomNumber v-if="currentPage === 'RandomNumber'" />
  </div>


  

</template>


<style>
.hover-effect:hover{
  color: red;
}
</style>