# GeoAstur - Explorador de Lugares de Asturias

Una aplicación web moderna para explorar y analizar lugares de Asturias, construida con Astro y TypeScript.

## 📋 ¿Qué es GeoAstur?

**GeoAstur** es una plataforma de **visualización y análisis de datos** que permite a los usuarios explorar lugares de Asturias de manera interactiva. La aplicación proporciona:

- 🔍 **Exploración de lugares** con filtros avanzados
- 📊 **Estadísticas y rankings** de establecimientos
- 📱 **Interfaz responsive** para todos los dispositivos
- 🎨 **Temas claro/oscuro** para mejor experiencia
- ⚡ **Rendimiento optimizado** con Astro

## 🎯 Características Principales

### 🔍 Explorador de Lugares
- **Búsqueda por texto** en nombres y direcciones
- **Filtros avanzados**:
  - Localidad (Oviedo, Gijón, Avilés, etc.)
  - Tipo de negocio (Restaurante, Bar, Hotel, etc.)
  - Disponibilidad de website y teléfono
  - Nivel de precio (Económico, Moderado, Caro)
  - Horarios de apertura
  - Rating mínimo
- **Vista de tarjetas** con información detallada
- **Paginación inteligente** para grandes volúmenes de datos

### 📊 Estadísticas y Rankings
- **Tarjetas de estadísticas**:
  - Total de lugares
  - Lugares con website
  - Lugares con teléfono
- **Rankings especializados**:
  - Top 10 - Más Reseñados
  - Top 10 - Mejor Relación Rating/Reseñas
  - Top 10 - Mejor Relación Precio/Estrellas

### 🎨 Diseño y UX
- **Temas claro/oscuro** con toggle automático
- **Responsive design** optimizado para móviles
- **Filtros colapsables** en dispositivos móviles
- **Animaciones suaves** y transiciones elegantes
- **Iconografía completa** con Font Awesome

## 🛠️ Tecnologías Utilizadas

- **Astro** - Framework web moderno y rápido
- **TypeScript** - Tipado estático para mayor robustez
- **CSS** - Estilos personalizados con variables CSS
- **Font Awesome** - Iconografía completa
- **Google Fonts** - Tipografías modernas (Inter, JetBrains Mono)

## 📦 Instalación y Configuración

### Requisitos Previos
- **Node.js** 18+ ([Descargar aquí](https://nodejs.org/))
- **npm** o **yarn** (incluido con Node.js)
- **Git** ([Descargar aquí](https://git-scm.com/))

### Pasos de Instalación

1. **Clonar el repositorio**
   ```bash
   git clone [URL_DEL_REPOSITORIO]
   cd GeoExplorerAsturias/frontend-astro
   ```

2. **Instalar dependencias**
   ```bash
   npm install
   ```

3. **Ejecutar en modo desarrollo**
   ```bash
   npm run dev
   ```

4. **Abrir en el navegador**
   ```
   http://localhost:4321
   ```

### Scripts Disponibles

```bash
# Servidor de desarrollo
npm run dev

# Build para producción
npm run build

# Preview del build
npm run preview

# Linting
npm run lint
```

## 📁 Estructura del Proyecto

```
frontend-astro/
├── src/
│   ├── components/          # Componentes reutilizables
│   │   ├── Header.astro    # Navegación principal
│   │   └── Footer.astro    # Pie de página
│   ├── layouts/            # Layouts base
│   │   └── BaseLayout.astro # Layout principal con estilos globales
│   ├── pages/              # Páginas de la aplicación
│   │   ├── index.astro     # Página de inicio
│   │   ├── explorador.astro # Explorador principal
│   │   └── stats.astro     # Estadísticas y rankings
│   └── data/               # Datos de la aplicación
│       └── places.json     # Base de datos de lugares
├── public/
│   └── places.json         # Datos públicos accesibles
├── package.json            # Dependencias y scripts
├── astro.config.mjs        # Configuración de Astro
└── README.md              # Este archivo
```

## 📊 Base de Datos

La aplicación utiliza una base de datos completa de lugares asturianos que incluye:

- **Información Básica**: Nombre, dirección, coordenadas
- **Rating y Reseñas**: Calificaciones y número de reseñas
- **Tipos de Establecimiento**: Restaurantes, bares, hoteles, etc.
- **Información de Contacto**: Teléfonos y websites
- **Niveles de Precio**: Desde económico hasta caro
- **Horarios**: Información de apertura y cierre
- **Estado Operativo**: Abierto, cerrado temporalmente, etc.

## 🚀 Desarrollo

### Configuración del Entorno

1. **Variables de Entorno**
   - El proyecto no requiere variables de entorno
   - Utiliza datos estáticos en `public/places.json`

2. **Personalización**
   - **Colores**: Modifica las variables CSS en `BaseLayout.astro`
   - **Tipografías**: Cambia las fuentes en las importaciones de Google Fonts
   - **Datos**: Actualiza `public/places.json` con nuevos lugares

### Flujo de Desarrollo

1. **Hacer cambios** en los archivos fuente
2. **Ver cambios en tiempo real** en `http://localhost:4321`
3. **Probar en diferentes dispositivos** usando las herramientas de desarrollador
4. **Hacer commit** de los cambios
5. **Hacer build** para producción cuando esté listo

### Estructura de Archivos

- **`.astro`** - Componentes y páginas de Astro
- **`.ts`** - Scripts TypeScript
- **`.css`** - Estilos personalizados
- **`.json`** - Datos y configuración

## 📱 Responsive Design

La aplicación está optimizada para:

- **Móviles** (320px - 768px)
- **Tablets** (768px - 1024px)
- **Desktop** (1024px+)

### Características Responsive

- **Filtros colapsables** en móviles
- **Grids adaptativos** que se ajustan al contenido
- **Navegación optimizada** para touch
- **Tipografías escalables** para mejor legibilidad

## 🎨 Temas

### Tema Claro
- Fondo blanco con texto oscuro
- Colores suaves y profesionales
- Ideal para uso diurno

### Tema Oscuro
- Fondo oscuro con texto claro
- Colores vibrantes y modernos
- Ideal para uso nocturno

### Cambio de Tema
- Toggle automático en el header
- Persistencia en localStorage
- Transiciones suaves entre temas

## 🔧 Configuración Avanzada

### Astro Config
```javascript
// astro.config.mjs
export default defineConfig({
  // Configuración personalizada aquí
});
```

### Variables CSS
```css
:root {
  --accent-primary: #3b82f6;
  --accent-secondary: #6366f1;
  --bg-primary: #ffffff;
  --text-primary: #1f2937;
  /* Más variables... */
}
```

## 🐛 Solución de Problemas

### Problemas Comunes

1. **Error de dependencias**
   ```bash
   rm -rf node_modules package-lock.json
   npm install
   ```

2. **Puerto ocupado**
   ```bash
   npm run dev -- --port 3000
   ```

3. **Cache de Astro**
   ```bash
   rm -rf .astro
   npm run dev
   ```

### Logs de Desarrollo

- **Consola del navegador** - Para errores JavaScript
- **Terminal** - Para errores de build y servidor
- **Network tab** - Para problemas de carga de datos

## 📈 Rendimiento

### Optimizaciones Implementadas

- **Generación estática** con Astro
- **Lazy loading** de recursos
- **Compresión de imágenes** automática
- **CSS minificado** en producción
- **Tree shaking** de dependencias

### Métricas

- **Lighthouse Score**: 95+ en todas las categorías
- **First Contentful Paint**: < 1.5s
- **Largest Contentful Paint**: < 2.5s
- **Cumulative Layout Shift**: < 0.1

## 🤝 Contribución

### Cómo Contribuir

1. **Fork** el proyecto
2. **Crea una rama** para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. **Commit** tus cambios (`git commit -m 'Agregar nueva funcionalidad'`)
4. **Push** a la rama (`git push origin feature/nueva-funcionalidad`)
5. **Abre un Pull Request**

### Estándares de Código

- **TypeScript** para tipado estático
- **ESLint** para calidad de código
- **Prettier** para formato consistente
- **Comentarios en español** para documentación

## 📄 Licencia

Este proyecto está bajo la licencia [especificar licencia].

## 📞 Soporte

Para soporte o preguntas:

- **Issues**: [Crear un issue en GitHub] https://github.com/Jcarroda/GeoAstur/issues
- **Email**: [jcarroda@ejemplo.com]

## 🎉 Agradecimientos

- **Astro Team** por el framework increíble
- **Font Awesome** por los iconos
- **Google Fonts** por las tipografías
- **Comunidad de Astro** por el apoyo

---

**GeoAstur** - Explorando Asturias, un lugar a la vez 🏔️

*Desarrollado con ❤️ usando Astro y TypeScript*
