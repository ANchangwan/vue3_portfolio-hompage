<script setup>
import TitlePage from "./components/TitlePage.vue";
import Portfolio from "./components/Portfolio.vue";
import About from "./components/About.vue";

</script>

<template>
  <nav class="navbar navbar-expand-lg fixed-top bg-body-tertiary" data-bs-theme="dark">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/">Dpams Tech</router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link active" aria-current="page" to="/title">Home</router-link>
          </li>
          <li class="nav-item">
          <router-link class="nav-link" to="/portfolio">Portfolio</router-link>
        </li>
        </ul>
      </div>
    </div>
  </nav>
 <router-view/>
</template>

<style scoped lang="scss">


</style>
