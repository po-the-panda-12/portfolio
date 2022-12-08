<script setup>
import { RouterLink, RouterView } from 'vue-router'
import navbar from './components/navbar.vue'
import 'bootstrap/dist/js/bootstrap.bundle.min.js'
import 'bootstrap/dist/css/bootstrap.min.css'

</script>

<template>
  <header>
    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->

    <!-- <div class="wrapper"> -->
      <!-- <HelloWorld msg="grgr!" /> -->

      <!-- <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav> -->

      <navbar />
    <!-- </div> -->
  </header>

  <RouterView />
</template>
