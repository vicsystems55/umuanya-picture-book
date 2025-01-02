<template>
    <div class="registration-completed d-flex justify-content-center align-items-center vh-100">
      <div class="text-center">
        <!-- Lottie animation container -->
        <div class="lottie-container mx-auto mb-4" style="width: 150px; height: 150px;">
          <lottie-player
            src="https://assets2.lottiefiles.com/packages/lf20_u4yrau.json" 
            background="transparent" 
            speed="1" 
            style="width: 100%; height: 100%;" 
            loop 
            autoplay>
          </lottie-player>
        </div>
        <!-- Text -->
        <h2 class="mb-2">Registration Completed!</h2>
        <p class="text-muted">Thank you for registering. You’re all set to get started.</p>
        <div class="py-5">
          <router-link to="/">
          <button  class="btn btn-warning">Back Home</button>
          </router-link>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "RegistrationCompleted",
  };
  </script>
  
  
  
  <style scoped>
  /* Ensure full height for the parent container */
  .registration-completed {
    min-height: 100vh;
    background-color: #f8f9fa; /* Light gray background for contrast */
  }
  </style>
  