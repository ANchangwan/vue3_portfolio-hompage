<script setup>
import Title from "./components/Title.vue";
import Portfolio from "./components/Portfolio.vue";
import About from "./components/About.vue";

</script>

<template>
  <nav class="navbar navbar-expand-lg fixed-top bg-body-tertiary" data-bs-theme="dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Dpams Tech</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
          <a class="nav-link" href="#">Portfolio</a>
        </li>
        </ul>
      </div>
    </div>
  </nav>
  <Title/>
  <Portfolio/>
  <About/>
</template>

<style scoped lang="scss">


</style>
