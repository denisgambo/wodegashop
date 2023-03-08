<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">    
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <a class="nav-link active" aria-current="page" href="#">
          <RouterLink to="/">Home</RouterLink>
        </a>
      </div>

      <div class="navbar-nav">
        <a class="nav-link active" aria-current="page" href="#">
          <RouterLink to="/clothes">Clothes</RouterLink>
        </a>
      </div>
    </div>
  </div>
</nav>

  <RouterView />
</template>

<style scoped>



</style>
