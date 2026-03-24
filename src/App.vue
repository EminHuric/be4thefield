<script setup>
import Menu from './components/menu.vue'
import Intro from './components/intro.vue'
import About from './components/about.vue';
import Products from './components/products.vue';
import End from './components/end.vue';
import Contact from './components/contact.vue';
import Footer from './components/footer.vue';
</script>

<template>
  <Menu />
  <Intro />
  <About />
  <Products />
  <End />
  <Contact />
  <Footer />
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