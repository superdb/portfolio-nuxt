<script setup>
import { ref } from 'vue'

const formData = ref({
  name: '',
  email: '',
  message: ''
})

const submitted = ref(false)

const handleSubmit = (e) => {
  e.preventDefault()
  if (formData.value.name && formData.value.email && formData.value.message) {
    submitted.value = true
    console.log('Formulario enviado:', formData.value)
    setTimeout(() => {
      formData.value = { name: '', email: '', message: '' }
      submitted.value = false
    }, 3000)
  }
}

const contactInfo = ref([
  {
    icon: 'mail',
    label: 'Email',
    value: 'christian@superdb.dev',
    href: 'mailto:christian@superdb.dev'
  },
  {
    icon: 'phone',
    label: 'Teléfono',
    value: '+1 (555) 123-4567',
    href: 'tel:+15551234567'
  },
  {
    icon: 'location',
    label: 'Ubicación',
    value: 'Buenos Aires, Argentina',
    href: '#'
  }
])
</script>

<template>
  <section id="contact" class="py-20 relative">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Título sección -->
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-4 bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent">
          Hablemos
        </h2>
        <p class="text-xl text-gray-400">
          ¿Tienes un proyecto en mente? Me encantaría escucharte
        </p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
        <!-- Información de contacto -->
        <div>
          <!-- Contact Info Cards -->
          <div class="space-y-6 mb-8">
            <a
              v-for="info in contactInfo"
              :key="info.label"
              :href="info.href"
              class="flex items-start space-x-4 group"
            >
              <div class="flex-shrink-0">
                <div class="flex items-center justify-center h-12 w-12 rounded-lg bg-gradient-to-br from-purple-600 to-pink-600 text-white group-hover:shadow-lg group-hover:shadow-purple-500/50 transition">
                  <svg v-if="info.icon === 'mail'" class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                  </svg>
                  <svg v-else-if="info.icon === 'phone'" class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 00.948.684l1.498 4.493a1 1 0 00.502.756l2.73 1.365a1 1 0 001.27-1.27L13.596 9a1 1 0 00-.756-.502L9 6.77a1 1 0 00-.684-.948L5 5a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-3.28" />
                  </svg>
                  <svg v-else class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  </svg>
                </div>
              </div>
              <div>
                <p class="text-sm font-medium text-gray-500">{{ info.label }}</p>
                <p class="text-lg text-white group-hover:text-purple-400 transition">{{ info.value }}</p>
              </div>
            </a>
          </div>

          <!-- Redes sociales -->
          <div>
            <p class="text-sm font-medium text-gray-500 mb-4">Sígueme en redes</p>
            <div class="flex space-x-4">
              <a href="https://github.com/superdb" target="_blank" class="text-gray-400 hover:text-purple-400 transition transform hover:scale-110">
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v 3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                </svg>
              </a>
              <a href="https://linkedin.com/in/superdb" target="_blank" class="text-gray-400 hover:text-purple-400 transition transform hover:scale-110">
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.475-2.236-1.986-2.236-1.081 0-1.722.721-2.004 1.426-.103.25-.129.599-.129.949v5.43h-3.554s.05-8.81 0-9.728h3.554v1.375c.428-.659 1.194-1.599 2.905-1.599 2.121 0 3.713 1.386 3.713 4.365v5.587zM5.337 9.433c-1.144 0-1.915-.762-1.915-1.715 0-.955.77-1.715 1.964-1.715 1.192 0 1.915.76 1.937 1.715 0 .953-.745 1.715-1.986 1.715zm1.582 11.019H3.656V9.724h3.263v10.728zM22.225 0H1.771C.798 0 0 .774 0 1.729v20.542C0 23.227.798 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.225 0z"/>
                </svg>
              </a>
              <a href="https://twitter.com/superdb" target="_blank" class="text-gray-400 hover:text-purple-400 transition transform hover:scale-110">
                <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2s9 5 20 5a9.5 9.5 0 00-9-5.5c4.75 2.25 10-2 10-8.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"/>
                </svg>
              </a>
            </div>
          </div>
        </div>

        <!-- Formulario de contacto -->
        <div class="bg-dark-800 rounded-xl p-8 border border-gray-700">
          <form @submit="handleSubmit" class="space-y-6">
            <!-- Input Nombre -->
            <div>
              <label for="name" class="block text-sm font-medium text-gray-300 mb-2">
                Nombre
              </label>
              <input
                v-model="formData.name"
                type="text"
                id="name"
                required
                class="w-full px-4 py-3 bg-dark-900 border border-gray-700 rounded-lg text-white placeholder-gray-500 focus:border-purple-500 focus:ring-1 focus:ring-purple-500 transition outline-none"
                placeholder="Tu nombre"
              />
            </div>

            <!-- Input Email -->
            <div>
              <label for="email" class="block text-sm font-medium text-gray-300 mb-2">
                Email
              </label>
              <input
                v-model="formData.email"
                type="email"
                id="email"
                required
                class="w-full px-4 py-3 bg-dark-900 border border-gray-700 rounded-lg text-white placeholder-gray-500 focus:border-purple-500 focus:ring-1 focus:ring-purple-500 transition outline-none"
                placeholder="tu@email.com"
              />
            </div>

            <!-- Textarea Mensaje -->
            <div>
              <label for="message" class="block text-sm font-medium text-gray-300 mb-2">
                Mensaje
              </label>
              <textarea
                v-model="formData.message"
                id="message"
                required
                rows="5"
                class="w-full px-4 py-3 bg-dark-900 border border-gray-700 rounded-lg text-white placeholder-gray-500 focus:border-purple-500 focus:ring-1 focus:ring-purple-500 transition outline-none resize-none"
                placeholder="Tu mensaje..."
              ></textarea>
            </div>

            <!-- Submit Button -->
            <button
              type="submit"
              class="w-full px-6 py-3 bg-gradient-to-r from-purple-600 to-pink-600 text-white font-semibold rounded-lg hover:shadow-lg hover:shadow-purple-500/50 transition transform hover:scale-105"
            >
              {{ submitted ? '¡Mensaje enviado!' : 'Enviar Mensaje' }}
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>
