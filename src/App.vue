<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">KELLY</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <router-link to="/" class="nav-link pb-0" exact-active-class="active">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/about" class="nav-link pb-0" exact-active-class="active">About</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/resume" class="nav-link pb-0" exact-active-class="active">Resume</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/service" class="nav-link pb-0" exact-active-class="active">Services</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/portfolio" class="nav-link pb-0" exact-active-class="active">Portfolio</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/contact" class="nav-link pb-0" exact-active-class="active">Contact</router-link>
          </li>
        </ul>
        <ul class="navbar-nav social-links">
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="fab fa-twitter"></i></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="fab fa-facebook"></i></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="fab fa-instagram"></i></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#"><i class="fab fa-linkedin"></i></a>
          </li>
        </ul>
      </div>
    </nav>
    <router-view/>
    <copyright/>
  </div>
</template>

<script>
import copyright from './components/CopyrightPage.vue';

export default {
  name: 'App',
  components: {
    copyright
  }
};
</script>
