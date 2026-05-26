# 📋 Instrucciones para subir tu portafolio a GitHub

## Opción 1: Crear repositorio en GitHub desde la web

1. Abre GitHub: https://github.com/new
2. Completa los datos:
   - **Repository name**: `superdb-portfolio`
   - **Description**: "Modern portfolio with Vue 3, Vite & Tailwind CSS"
   - **Public** (para que sea visible)
   - Sin inicializar con README (ya lo tenemos)

3. Copia el comando HTTPS o SSH que te ofrece GitHub

## Opción 2: Comando automático (si tienes GitHub CLI)

```bash
cd c:\Users\champ\Downloads\portfolio-nuxt
gh repo create superdb-portfolio --public --source=. --remote=origin --push
```

## Opción 3: Comando manual con Git

Después de crear el repositorio en GitHub, copia esta URL de tu repositorio y ejecuta:

```bash
cd c:\Users\champ\Downloads\portfolio-nuxt

# Renombrar rama a main
git branch -M main

# Agregar origin (REEMPLAZA TU_USUARIO con tu usuario de GitHub)
git remote add origin https://github.com/TU_USUARIO/superdb-portfolio.git

# Enviar al repositorio
git push -u origin main
```

## 🚀 Desplegar con GitHub Pages

Una vez subido, puedes desplegarlo gratis con GitHub Pages:

1. Ve a **Settings** del repositorio
2. En la sección **Pages**, selecciona:
   - **Source**: Deploy from a branch
   - **Branch**: main
   - **Folder**: / (root)
3. Modifica tu `vite.config.js`:

```javascript
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'

export default defineConfig({
  plugins: [vue()],
  base: '/superdb-portfolio/' // Reemplaza con tu nombre de repositorio
})
```

4. Ejecuta:
```bash
npm run build
```

5. El proyecto estará en: `https://TU_USUARIO.github.io/superdb-portfolio/`

## 📝 Cambios Necesarios Antes de Subir

Para que tu portafolio sea completamente personalizado:

1. **Actualizar README.md** - Reemplaza los datos con los tuyos
2. **Actualizar Hero.vue** - Modifica nombre, email, redes sociales
3. **Actualizar Projects.vue** - Agrega tus proyectos reales
4. **Actualizar Skills.vue** - Tus skills y herramientas
5. **Actualizar Contact.vue** - Tus datos de contacto

Después de cada cambio:
```bash
git add .
git commit -m "Descripción del cambio"
git push
```

## ✅ Checklist antes de publicar

- [ ] Nombres y datos personales actualizados
- [ ] Enlaces de GitHub, LinkedIn, Twitter correctos
- [ ] Descripción personal en Hero
- [ ] Al menos 3-4 proyectos reales
- [ ] Skills reales y precisos
- [ ] Email de contacto funcional
- [ ] Probado en mobile/tablet
- [ ] Repositorio público en GitHub

---

¡Tu portafolio está listo! 🎉
