<script setup>
import { ref } from 'vue'

const projects = ref([
  {
    id: 1,
    title: 'SaaS Dashboard',
    description: 'Plataforma completa de gestión empresarial con autenticación y análisis en tiempo real.',
    tags: ['Vue 3', 'Node.js', 'PostgreSQL', 'Tailwind'],
    link: 'https://github.com/superdb/saas-dashboard',
    color: 'from-purple-600 to-pink-600'
  },
  {
    id: 2,
    title: 'E-Commerce API',
    description: 'API REST escalable con microservicios, pagos integrados y gestión de inventario.',
    tags: ['Express', 'MongoDB', 'AWS', 'Docker'],
    link: 'https://github.com/superdb/ecommerce-api',
    color: 'from-blue-600 to-cyan-600'
  },
  {
    id: 3,
    title: 'React Native App',
    description: 'Aplicación móvil multiplataforma para gestión de tareas con sincronización en la nube.',
    tags: ['React Native', 'Firebase', 'Redux', 'Expo'],
    link: 'https://github.com/superdb/mobile-app',
    color: 'from-green-600 to-emerald-600'
  },
  {
    id: 4,
    title: 'Real-time Chat',
    description: 'Sistema de mensajería en tiempo real con notificaciones y encriptación end-to-end.',
    tags: ['Socket.io', 'Vue.js', 'WebRTC', 'Redis'],
    link: 'https://github.com/superdb/realtime-chat',
    color: 'from-orange-600 to-red-600'
  },
  {
    id: 5,
    title: 'ML Pipeline',
    description: 'Pipeline de machine learning para análisis de datos con visualización interactiva.',
    tags: ['Python', 'TensorFlow', 'Flask', 'D3.js'],
    link: 'https://github.com/superdb/ml-pipeline',
    color: 'from-indigo-600 to-purple-600'
  },
  {
    id: 6,
    title: 'Blockchain Wallet',
    description: 'Billetera criptográfica segura con interfaz web moderna y gestión de criptomonedas.',
    tags: ['Solidity', 'Web3.js', 'React', 'Hardhat'],
    link: 'https://github.com/superdb/crypto-wallet',
    color: 'from-yellow-600 to-orange-600'
  }
])
</script>

<template>
  <section id="projects" class="py-20 relative">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Título sección -->
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-4 bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent">
          Proyectos Destacados
        </h2>
        <p class="text-xl text-gray-400">
          Algunos de mis mejores trabajos
        </p>
      </div>

      <!-- Grid de proyectos -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <a
          v-for="project in projects"
          :key="project.id"
          :href="project.link"
          target="_blank"
          class="group relative overflow-hidden rounded-xl bg-dark-800 border border-gray-700 hover:border-purple-500 transition-all duration-300 transform hover:scale-105 hover:-translate-y-2"
        >
          <!-- Fondo gradiente -->
          <div :class="`absolute inset-0 bg-gradient-to-br ${project.color} opacity-0 group-hover:opacity-10 transition-opacity duration-300`"></div>

          <!-- Contenido -->
          <div class="relative p-6 h-full flex flex-col">
            <!-- Icono -->
            <div class="mb-4 w-12 h-12 bg-dark-700 rounded-lg flex items-center justify-center group-hover:bg-gradient-to-br group-hover:from-purple-600 group-hover:to-pink-600 transition-all">
              <svg class="w-6 h-6 text-purple-400 group-hover:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
              </svg>
            </div>

            <!-- Título -->
            <h3 class="text-xl font-bold mb-2 group-hover:text-transparent group-hover:bg-gradient-to-r group-hover:from-purple-400 group-hover:to-pink-600 group-hover:bg-clip-text transition-all">
              {{ project.title }}
            </h3>

            <!-- Descripción -->
            <p class="text-gray-400 text-sm mb-4 flex-grow">
              {{ project.description }}
            </p>

            <!-- Tags -->
            <div class="flex flex-wrap gap-2">
              <span
                v-for="tag in project.tags"
                :key="tag"
                class="px-3 py-1 bg-dark-700 text-purple-300 text-xs rounded-full group-hover:bg-purple-900/30 transition"
              >
                {{ tag }}
              </span>
            </div>

            <!-- Hover effect border -->
            <div class="absolute inset-0 border-2 border-transparent group-hover:border-purple-500 rounded-xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </div>
        </a>
      </div>

      <!-- CTA Button -->
      <div class="text-center mt-16">
        <a
          href="https://github.com/superdb"
          target="_blank"
          class="inline-block px-8 py-3 bg-gradient-to-r from-purple-600 to-pink-600 text-white font-semibold rounded-lg hover:shadow-lg hover:shadow-purple-500/50 transition transform hover:scale-105"
        >
          Ver todos en GitHub
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>
