<script setup>
  const skills = [
    { name: 'HTML', point: '90%' },
    { name: 'CSS', point: '80%' },
    { name: 'JAVASCRIPT', point: '50%' },
    { name: 'VUE', point: '75%' },
  ]
</script>

<template>
  <section id="About" class="container">
    <h1>About</h1>
    <div class="row gx-5">
      <figure class="col-md-6">
        <img src="/images/profile.jpg" alt="">
        <figcaption>About Me</figcaption>
      </figure>
      <p class="col-md-6">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus accusantium aspernatur atque consectetur distinctio eaque est eum eveniet inventore iure, maxime, natus neque non nulla quia recusandae sed sequi sint.</p>
    </div>
    <article class="row mt-5">
      <h2 class="mb-3">Skills</h2>
      <dl>
        <div v-for="skill in skills" :key="skill.name">
          <dt class="lead">{{ skill.name }}</dt>
          <dd>
            <div class="progress" role="progressbar">
              <div class="progress-bar" :style="{ width: skill.point }"></div>
            </div>
          </dd>
        </div>
      </dl>
    </article>
  </section>

</template>

<style scoped lang="scss">
  #About {
    img{
      width: 100%;
    }
  }
</style>