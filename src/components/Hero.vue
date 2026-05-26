<script setup>
</script>

<template>
  <section id="home" class="min-h-screen flex items-center justify-center relative overflow-hidden pt-16">
    <!-- Fondo con efecto gradiente -->
    <div class="absolute inset-0 -z-10">
      <div class="absolute top-20 left-10 w-72 h-72 bg-purple-600 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-blob"></div>
      <div class="absolute top-40 right-10 w-72 h-72 bg-pink-600 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-blob animation-delay-2000"></div>
      <div class="absolute -bottom-8 left-1/2 w-72 h-72 bg-blue-600 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-blob animation-delay-4000"></div>
    </div>

    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
      <div class="text-center">
        <!-- Avatar -->
        <div class="mb-8 flex justify-center">
          <div class="relative">
            <div class="absolute inset-0 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full blur opacity-75 animate-pulse"></div>
            <div class="relative w-32 h-32 bg-dark-800 rounded-full flex items-center justify-center text-5xl font-bold bg-gradient-to-r from-purple-400 to-pink-600 bg-clip-text text-transparent">
              CR
            </div>
          </div>
        </div>

        <!-- Título principal -->
        <h1 class="text-5xl md:text-7xl font-bold mb-6 bg-gradient-to-r from-purple-400 via-pink-500 to-red-500 bg-clip-text text-transparent">
          Christian Mauro
        </h1>

        <!-- Subtítulo -->
        <p class="text-2xl md:text-3xl text-gray-300 mb-8">
          Full Stack Developer & Creative Mind
        </p>

        <!-- Descripción -->
        <p class="text-lg text-gray-400 max-w-2xl mx-auto mb-12 leading-relaxed">
          Apasionado por crear experiencias digitales innovadoras. Especializado en 
          <span class="text-purple-400 font-semibold">Vue.js, React, Node.js y Cloud</span>. 
          Transformo ideas en soluciones escalables y de alto rendimiento.
        </p>

        <!-- Botones CTA -->
        <div class="flex flex-col sm:flex-row gap-4 justify-center mb-8">
          <a
            href="#projects"
            class="px-8 py-3 bg-gradient-to-r from-purple-600 to-pink-600 text-white font-semibold rounded-lg hover:shadow-lg hover:shadow-purple-500/50 transition transform hover:scale-105"
          >
            Ver Proyectos
          </a>
          <a
            href="#contact"
            class="px-8 py-3 border-2 border-purple-500 text-purple-400 font-semibold rounded-lg hover:bg-purple-500/10 transition"
          >
            Contactarme
          </a>
        </div>

        <!-- Redes sociales -->
        <div class="flex justify-center gap-6">
          <a
            href="https://github.com/superdb"
            target="_blank"
            class="text-gray-400 hover:text-purple-400 transition transform hover:scale-110"
            aria-label="GitHub"
          >
            <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v 3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
            </svg>
          </a>
          <a
            href="https://linkedin.com/in/superdb"
            target="_blank"
            class="text-gray-400 hover:text-purple-400 transition transform hover:scale-110"
            aria-label="LinkedIn"
          >
            <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
              <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.475-2.236-1.986-2.236-1.081 0-1.722.721-2.004 1.426-.103.25-.129.599-.129.949v5.43h-3.554s.05-8.81 0-9.728h3.554v1.375c.428-.659 1.194-1.599 2.905-1.599 2.121 0 3.713 1.386 3.713 4.365v5.587zM5.337 9.433c-1.144 0-1.915-.762-1.915-1.715 0-.955.77-1.715 1.964-1.715 1.192 0 1.915.76 1.937 1.715 0 .953-.745 1.715-1.986 1.715zm1.582 11.019H3.656V9.724h3.263v10.728zM22.225 0H1.771C.798 0 0 .774 0 1.729v20.542C0 23.227.798 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.225 0z"/>
            </svg>
          </a>
          <a
            href="https://twitter.com/superdb"
            target="_blank"
            class="text-gray-400 hover:text-purple-400 transition transform hover:scale-110"
            aria-label="Twitter"
          >
            <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24">
              <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2s9 5 20 5a9.5 9.5 0 00-9-5.5c4.75 2.25 10-2 10-8.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"/>
            </svg>
          </a>
        </div>
      </div>
    </div>

    <!-- Scroll indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
      <svg class="w-6 h-6 text-purple-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
      </svg>
    </div>
  </section>
</template>

<style scoped>
@keyframes blob {
  0%, 100% {
    transform: translate(0, 0) scale(1);
  }
  33% {
    transform: translate(30px, -50px) scale(1.1);
  }
  66% {
    transform: translate(-20px, 20px) scale(0.9);
  }
}

.animate-blob {
  animation: blob 7s infinite;
}

.animation-delay-2000 {
  animation-delay: 2s;
}

.animation-delay-4000 {
  animation-delay: 4s;
}
</style>
