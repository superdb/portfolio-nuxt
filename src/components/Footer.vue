<script setup>
const currentYear = new Date().getFullYear()
</script>

<template>
  <footer class="bg-dark-800 border-t border-gray-700 py-12">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
        <!-- Branding -->
        <div>
          <h3 class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent mb-2">
            SUPERDB
          </h3>
          <p class="text-gray-400 text-sm">
            Full Stack Developer crafting digital experiences
          </p>
        </div>

        <!-- Quick Links -->
        <div>
          <h4 class="text-white font-semibold mb-4">Enlaces Rápidos</h4>
          <div class="space-y-2">
            <a href="#home" class="text-gray-400 hover:text-purple-400 text-sm transition">
              Inicio
            </a>
            <br>
            <a href="#projects" class="text-gray-400 hover:text-purple-400 text-sm transition">
              Proyectos
            </a>
            <br>
            <a href="#skills" class="text-gray-400 hover:text-purple-400 text-sm transition">
              Skills
            </a>
            <br>
            <a href="#contact" class="text-gray-400 hover:text-purple-400 text-sm transition">
              Contacto
            </a>
          </div>
        </div>

        <!-- Social Links -->
        <div>
          <h4 class="text-white font-semibold mb-4">Sígueme</h4>
          <div class="flex space-x-4">
            <a href="https://github.com/superdb" target="_blank" class="text-gray-400 hover:text-purple-400 transition">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v 3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
              </svg>
            </a>
            <a href="https://linkedin.com/in/superdb" target="_blank" class="text-gray-400 hover:text-purple-400 transition">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.475-2.236-1.986-2.236-1.081 0-1.722.721-2.004 1.426-.103.25-.129.599-.129.949v5.43h-3.554s.05-8.81 0-9.728h3.554v1.375c.428-.659 1.194-1.599 2.905-1.599 2.121 0 3.713 1.386 3.713 4.365v5.587zM5.337 9.433c-1.144 0-1.915-.762-1.915-1.715 0-.955.77-1.715 1.964-1.715 1.192 0 1.915.76 1.937 1.715 0 .953-.745 1.715-1.986 1.715zm1.582 11.019H3.656V9.724h3.263v10.728zM22.225 0H1.771C.798 0 0 .774 0 1.729v20.542C0 23.227.798 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.225 0z"/>
              </svg>
            </a>
            <a href="https://twitter.com/superdb" target="_blank" class="text-gray-400 hover:text-purple-400 transition">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2s9 5 20 5a9.5 9.5 0 00-9-5.5c4.75 2.25 10-2 10-8.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"/>
              </svg>
            </a>
          </div>
        </div>
      </div>

      <!-- Divider -->
      <div class="border-t border-gray-700 pt-8">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <p class="text-gray-500 text-sm">
            © {{ currentYear }} Christian Mauro. All rights reserved.
          </p>
          <p class="text-gray-500 text-sm mt-4 md:mt-0">
            Diseñado y desarrollado por mí con <span class="text-red-500">❤️</span>
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
</style>
