<script setup>
import { ref } from 'vue'

const skills = ref([
  {
    category: 'Frontend',
    items: [
      { name: 'Vue 3', level: 95 },
      { name: 'React', level: 90 },
      { name: 'Tailwind CSS', level: 95 },
      { name: 'TypeScript', level: 85 }
    ]
  },
  {
    category: 'Backend',
    items: [
      { name: 'Node.js', level: 92 },
      { name: 'Express', level: 90 },
      { name: 'Python', level: 85 },
      { name: 'FastAPI', level: 80 }
    ]
  },
  {
    category: 'Bases de Datos',
    items: [
      { name: 'PostgreSQL', level: 88 },
      { name: 'MongoDB', level: 85 },
      { name: 'Redis', level: 80 },
      { name: 'Firebase', level: 82 }
    ]
  },
  {
    category: 'DevOps & Cloud',
    items: [
      { name: 'Docker', level: 85 },
      { name: 'AWS', level: 80 },
      { name: 'Git', level: 95 },
      { name: 'CI/CD', level: 85 }
    ]
  }
])

const tools = ref([
  'VS Code', 'Git', 'Webpack', 'Vite', 'Jest', 'Docker', 'AWS', 
  'Postman', 'Figma', 'Linux', 'GitHub', 'GitLab'
])
</script>

<template>
  <section id="skills" class="py-20 bg-dark-800/50 relative">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Título sección -->
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-4 bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent">
          Skills & Expertise
        </h2>
        <p class="text-xl text-gray-400">
          Tecnologías y herramientas que domino
        </p>
      </div>

      <!-- Skills Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-16">
        <div
          v-for="skillGroup in skills"
          :key="skillGroup.category"
          class="bg-dark-900 rounded-xl p-6 border border-gray-700 hover:border-purple-500 transition-all"
        >
          <h3 class="text-lg font-bold text-purple-400 mb-6">
            {{ skillGroup.category }}
          </h3>

          <div class="space-y-4">
            <div v-for="skill in skillGroup.items" :key="skill.name" class="space-y-2">
              <div class="flex justify-between items-center">
                <span class="text-sm font-medium text-gray-300">{{ skill.name }}</span>
                <span class="text-xs text-gray-500">{{ skill.level }}%</span>
              </div>
              <div class="w-full bg-dark-700 rounded-full h-2 overflow-hidden">
                <div
                  class="h-full bg-gradient-to-r from-purple-600 to-pink-600 rounded-full transition-all duration-1000"
                  :style="{ width: skill.level + '%' }"
                ></div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Tools & Technologies -->
      <div class="bg-dark-900 rounded-xl p-8 border border-gray-700">
        <h3 class="text-2xl font-bold text-purple-400 mb-8">
          Herramientas & Tecnologías
        </h3>

        <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-4">
          <div
            v-for="tool in tools"
            :key="tool"
            class="bg-dark-800 rounded-lg p-4 text-center border border-gray-700 hover:border-purple-500 hover:bg-dark-700 transition-all group cursor-default"
          >
            <span class="text-sm font-medium text-gray-300 group-hover:text-purple-400 transition">
              {{ tool }}
            </span>
          </div>
        </div>
      </div>

      <!-- Stats -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-16">
        <div class="bg-gradient-to-br from-purple-600/10 to-pink-600/10 rounded-xl p-8 border border-purple-500/30 text-center">
          <div class="text-4xl font-bold text-purple-400 mb-2">5+</div>
          <div class="text-gray-400">Años de Experiencia</div>
        </div>

        <div class="bg-gradient-to-br from-blue-600/10 to-cyan-600/10 rounded-xl p-8 border border-blue-500/30 text-center">
          <div class="text-4xl font-bold text-blue-400 mb-2">50+</div>
          <div class="text-gray-400">Proyectos Completados</div>
        </div>

        <div class="bg-gradient-to-br from-green-600/10 to-emerald-600/10 rounded-xl p-8 border border-green-500/30 text-center">
          <div class="text-4xl font-bold text-green-400 mb-2">100%</div>
          <div class="text-gray-400">Satisfacción del Cliente</div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>
