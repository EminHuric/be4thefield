<script setup>
import Menu from './components/menu.vue'
import Intro from './components/intro.vue'
</script>

<template>
  <Menu />
  <Intro />

  <div class="content">
    <h2 style="margin-top: 200px;">Ovo je deo ispod Intro-a</h2>
    <p>Ovde možeš slagati dalje sekcije...</p>
  </div>
</template>

<style scoped>
.content {
  text-align: center;
  padding: 2rem;
}

h2 {
  font-size: 2rem;
  color: #fff;
}

p {
  font-size: 1.2rem;
  color: #ccc;
}
</style>