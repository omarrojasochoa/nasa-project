# 📘 NASA Trivias Educativas del Cuy

Proyecto educativo sobre agricultura peruana con trivias interactivas y visualización de contenido Markdown.

## 🚀 Despliegue en Vercel

### Opción 1: Despliegue Automático (Recomendado)

1. **Sube tu proyecto a GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: NASA Trivias Educativas"
   git branch -M main
   git remote add origin https://github.com/tu-usuario/nasa-trivias-educativas.git
   git push -u origin main
   ```

2. **Conecta con Vercel:**
   - Ve a [vercel.com](https://vercel.com)
   - Haz clic en "New Project"
   - Importa tu repositorio de GitHub
   - Vercel detectará automáticamente la configuración

### Opción 2: Despliegue con Vercel CLI

1. **Instala Vercel CLI:**
   ```bash
   npm i -g vercel
   ```

2. **Despliega desde la carpeta del proyecto:**
   ```bash
   cd c:\Users\OROJASO\Downloads\nasa
   vercel
   ```

3. **Sigue las instrucciones:**
   - Confirma el directorio del proyecto
   - Selecciona tu cuenta/equipo
   - Confirma la configuración

## 📁 Estructura del Proyecto

```
nasa/
├── a-preview.html          # Página principal de preview
├── assets/                 # Imágenes del proyecto
│   ├── 01-presentacion.png
│   ├── 02-juego-accion.png
│   ├── 03-trivia-v1.png
│   └── 04-trivia-v2.png
├── presentacion.md         # Presentación del proyecto
├── read.md                 # Documentación de lectura
├── storyboard.md          # Guión del proyecto
├── trivias.md             # Trivias en formato Markdown
├── vercel.json            # Configuración de Vercel
├── package.json           # Configuración del proyecto
└── README.md              # Este archivo
```

## 🌐 URLs de Acceso

Una vez desplegado, tu proyecto estará disponible en:
- **URL principal:** `https://tu-proyecto.vercel.app`
- **Preview directo:** `https://tu-proyecto.vercel.app/preview`

## 🎯 Características

- ✅ **Preview de Markdown:** Visualiza archivos .md con formato
- ✅ **Navegación por botones:** Acceso directo a cada archivo
- ✅ **Soporte de imágenes:** Carpeta assets optimizada
- ✅ **Responsive:** Funciona en móviles y desktop
- ✅ **Cache optimizado:** Configuración de Vercel para mejor rendimiento

## 🛠 Desarrollo Local

```bash
# Instalar dependencias
npm install

# Ejecutar servidor local
npm run dev

# El proyecto estará en http://localhost:3000
```

## 📝 Archivos de Contenido

- **storyboard.md:** Guión y narrativa del proyecto
- **presentacion.md:** Presentación del proyecto NASA
- **read.md:** Documentación adicional
- **trivias.md:** Preguntas educativas sobre agricultura peruana

## 🔧 Configuración de Vercel

El archivo `vercel.json` incluye:
- Redirecciones automáticas a la página principal
- Cache optimizado para assets estáticos
- Configuración de memoria para funciones

## 📞 Soporte

Si tienes problemas con el despliegue:
1. Verifica que todos los archivos estén en el repositorio
2. Revisa los logs de Vercel en el dashboard
3. Asegúrate de que `a-preview.html` esté en la raíz del proyecto

---

**¡Tu proyecto NASA está listo para el mundo! 🚀**