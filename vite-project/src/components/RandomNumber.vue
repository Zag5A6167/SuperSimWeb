<script setup>
import { ref } from 'vue'

const randomNumber = ref(0)

const generateRandomNumber = () =>{
  randomNumber.value = Math.floor(Math.random() * 1000) + 1
  
}
</script>

<template>
  <div>
    <h1>Hi how are you?</h1>
    <h1>Are you ready? for random number</h1>
    <div class="display-number">{{ randomNumber }}</div>
  </div>
  <button class="btn btn-primary" @click="generateRandomNumber">Generate Random Number</button>
</template>


<style>
.display-number{
  font-size: 10rem;
  font-weight: bold;
}
</style>
