# 🧭 Encuesta Quito - Septiembre - 2025

Panel de supervisión de campo para la encuesta de Quito de septiembre de 2025, con una meta de **1.200 encuestas**. Se conecta a **KoboToolbox** y utiliza **MapLibre GL JS** para la visualización geoespacial.

---

## 🚀 Características Principales

- **🗺️ Motor WebGL Nativo (GPU):**
  - Renderizado fluido a 60 FPS sin glitches ni parpadeos.
  - Cero dependencias de API keys externas con mosaicos cartográficos de alta velocidad.
  - Capas vectoriales de **42 parroquias** y **70 sectores censales de Quito**.
  - Aislamiento visual automático y auto-zoom cinemático por sector con enlace directo a **Google Maps Navigation**.

- **📊 Tablero de Control y KPIs:**
  - Total de encuestas recolectadas, avance de meta y producción del día.
  - Tiempos promedio de duración por encuestador.
  - Conexión en vivo con auto-sincronización y caché inteligente.

- **🎛️ Filtros Cruzados Dinámicos:**
  - Filtrado multidimensional en una sola pasada (N)$ por **Supervisor**, **Parroquia**, **Sector Censal**, **Fecha** y **Estado de GPS**.
  - Búsqueda en vivo y panel lateral (Drawer) con desglose individual de boletas por encuestador.

- **🎨 Interfaz de Usuario Moderna:**
  - Tipografía clara de alta legibilidad (*Plus Jakarta Sans*, *Inter*, *JetBrains Mono*, *Open Sans Bold*).
  - Soporte completo para **Modo Claro** y **Modo Oscuro**.

---

## 🛠️ Requisitos Previos

- [Node.js](https://nodejs.org/) (versión 18 o superior)
- [npm](https://www.npmjs.com/)

---

## 📦 Instalación y Configuración

1. **Clonar el repositorio:**
   `ash
   git clone https://github.com/climasocialec-beep/Herramienta-de-Campo.git
   cd Herramienta-de-Campo
   `

2. **Instalar dependencias:**
   `ash
   npm install
   `

3. **Configurar variables de entorno:**
   Copia el archivo de ejemplo .env.example a .env:
   `ash
   cp .env.example .env
   `
   Configura tus credenciales de KoboToolbox en .env:
   `ini
   PORT=3001
   KOBO_API_TOKEN=tu_token_de_kobotoolbox
   KOBO_ASSET_UID=tu_asset_uid
   KOBO_SERVER_URL=https://kf.kobotoolbox.org
   `

4. **Iniciar el servidor local:**
   `ash
   npm start
   # o para desarrollo con recarga automática:
   npm run dev
   `

5. **Acceder a la aplicación:**
   Abre tu navegador en [http://localhost:3001](http://localhost:3001).

---

## 📂 Estructura del Proyecto

`
├── public/
│   ├── assets/
│   │   ├── parroquias.geojson        # Capa de parroquias cantonales
│   │   └── sectores_censales.geojson # Capa de 70 sectores censales de Quito
│   ├── fonts/                         # Glifos vectoriales PBF locales
│   ├── libs/
│   │   ├── maplibre-gl.js            # Motor WebGL MapLibre
│   │   └── maplibre-gl.css
│   ├── index.html                     # Tablero de control
│   ├── script.js                      # Lógica frontend y WebGL
│   └── style.css                      # Estilos CSS y temas
├── .env.example                       # Plantilla de variables de entorno
├── .gitignore                         # Archivos y secretos ignorados
├── package.json
├── server.js                          # Servidor Express proxy con caché
└── README.md
`

---

## 👥 Desarrollado para
**Clima Social** — Equipo Técnico de Supervisión de Campo.
