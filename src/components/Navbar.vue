<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

defineProps({
  activeSection: String
})

defineEmits(['navigate'])

const scrollToSection = (section) => {
  isOpen.value = false
  const element = document.getElementById(section)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<template>
  <nav class="fixed w-full bg-dark-900/95 backdrop-blur-md z-50 border-b border-gray-800">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <!-- Logo -->
        <div class="flex-shrink-0">
          <a href="#home" class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent hover:opacity-80 transition">
            SUPERDB
          </a>
        </div>

        <!-- Desktop Menu -->
        <div class="hidden md:block">
          <div class="ml-10 flex items-baseline space-x-4">
            <button
              @click="scrollToSection('home')"
              class="px-3 py-2 rounded-md text-sm font-medium hover:text-purple-400 transition"
            >
              Inicio
            </button>
            <button
              @click="scrollToSection('projects')"
              class="px-3 py-2 rounded-md text-sm font-medium hover:text-purple-400 transition"
            >
              Proyectos
            </button>
            <button
              @click="scrollToSection('skills')"
              class="px-3 py-2 rounded-md text-sm font-medium hover:text-purple-400 transition"
            >
              Skills
            </button>
            <button
              @click="scrollToSection('contact')"
              class="px-3 py-2 rounded-md text-sm font-medium hover:text-purple-400 transition"
            >
              Contacto
            </button>
          </div>
        </div>

        <!-- Mobile menu button -->
        <div class="md:hidden">
          <button
            @click="isOpen = !isOpen"
            class="inline-flex items-center justify-center p-2 rounded-md hover:text-purple-400 transition"
          >
            <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Menu -->
      <div v-if="isOpen" class="md:hidden">
        <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
          <button
            @click="scrollToSection('home')"
            class="block w-full text-left px-3 py-2 rounded-md text-base font-medium hover:text-purple-400 transition"
          >
            Inicio
          </button>
          <button
            @click="scrollToSection('projects')"
            class="block w-full text-left px-3 py-2 rounded-md text-base font-medium hover:text-purple-400 transition"
          >
            Proyectos
          </button>
          <button
            @click="scrollToSection('skills')"
            class="block w-full text-left px-3 py-2 rounded-md text-base font-medium hover:text-purple-400 transition"
          >
            Skills
          </button>
          <button
            @click="scrollToSection('contact')"
            class="block w-full text-left px-3 py-2 rounded-md text-base font-medium hover:text-purple-400 transition"
          >
            Contacto
          </button>
        </div>
      </div>
    </div>
  </nav>
</template>
