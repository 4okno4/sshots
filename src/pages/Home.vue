<template>
  <div class="relative">
    <Header />
    <Hero />
    <Portfolio />
    <About />
    <Contacts /> <!-- добавили -->
  </div>
</template>

<script setup>
import Header from '../components/Header.vue'
import Hero from '../components/Hero.vue'
import Portfolio from '../components/Portfolio.vue'
import About from '../components/About.vue'
import Contacts from '../components/Contacts.vue' // импорт
</script>
