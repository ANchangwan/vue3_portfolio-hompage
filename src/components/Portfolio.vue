<script setup>
  import data from '../assets/portfolio';
  console.log(data[0]);
</script>

<template>
  <section id="portfolio" class="container">
    <h1>Portfolio</h1>
    <ul class="list row">
      <li class="col-md-4" v-for="item in data" :key="item.id">
        <img :src="`${item.imgUrl}`" :alt="item.imgUrl">
        <h3> {{item.title}}</h3>
        <p>{{ item.desc}}</p>
      </li>
    </ul>
  </section>
</template>

<style scoped lang="scss">
#portfolio {
  h1 { margin-bottom: 1rem; }
  .list {

    padding: 0;

    li {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin-bottom: 10vh;
      img {
        width: 100%;
        aspect-ratio: 16 / 9;
        object-fit: cover;
        object-position: top;
      }
      h4 { margin-top: 1rem; }
    }
  }
}

</style>