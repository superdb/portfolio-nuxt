<script setup>
import { ref } from 'vue'
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

const activeSection = ref('home')
</script>

<template>
  <div class="bg-dark-900 text-white">
    <Navbar :activeSection="activeSection" @navigate="activeSection = $event" />
    <Hero />
    <Projects />
    <Skills />
    <Contact />
    <Footer />
  </div>
</template>

<style scoped>
</style>
