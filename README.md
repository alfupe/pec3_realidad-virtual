# PEC 3: Tutorial de A-FRAME 360º - Inmersión Submarina

**Asignatura:** Realidad virtual (Semestre 2627/1)  
**Estudiante:** Alejandro Fuentes Pérez (`alfupe@uoc.edu`)  
**Grado:** Grado de Multimedia - Universitat Oberta de Catalunya (UOC)  

---

## 📌 Descripción del Proyecto

Este proyecto interactivo de Realidad Virtual WebXR recrea una **experiencia inmersiva submarina en 360º**, diseñada y optimizada para cumplir con los criterios de máxima calificación (Excelente) de la Rúbrica R3 de la PEC3:

1. **Escena 1 (Fondo fijo 360º con `<a-sky>`):**
   * Panorámica submarina equirrectangular de alta resolución (4096×2048 px) de un arrecife de coral.
   * **Interactividad y originalidad:** Puntos de interés (hotspots 3D) con señalización luminosa y animada. Al apuntar la mirada o el cursor (`mouseenter`), se despliegan paneles informativos interactivos sobre la biodiversidad del arrecife.
   * **Fauna marina 3D animada:** Peces geométricos estilizados nadando en órbitas concéntricas alrededor del usuario con aletas articuladas en movimiento.
   * **Efectos ambientales:** Columnas volumétricas de burbujas ascendentes.

2. **Escena 2 (Fondo de vídeo 360º con `<a-videosphere>`):**
   * Vídeo subacuático 360º en formato nativo **MP4 (H.264)**, garantizando compatibilidad universal con navegadores modernos de escritorio, móviles y visores VR.
   * **Interactividad y originalidad:** Consola HUD 3D de buceo flotante en el espacio virtual tridimensional con telemetría de inmersión y botones interactivos para alternar **Reproducir / Pausar** y activar/desactivar el sonido sin restricciones de políticas de autoplay del navegador.

3. **Incrustación en documento HTML principal:**
   * Ambas escenas están incrustadas y coordinadas en [`index.html`](index.html) a través de elementos `<iframe>` con pestañas de navegación directa, cumpliendo el apartado 7 del tutorial de A-Frame.

---

## 🌐 Acceso al Proyecto en GitHub Pages

El proyecto se encuentra publicado y accesible públicamente a través de GitHub Pages:

🔗 **[https://alfupe.github.io/pec3_realidad-virtual/](https://alfupe.github.io/pec3_realidad-virtual/)**

### 📱 Código QR de acceso directo

Apunta con la cámara de tu smartphone o tu visor VR para abrir directamente la experiencia:

<p align="center">
  <img src="recursos/qr-github-pages.png" alt="Código QR GitHub Pages PEC3" width="220">
  <br>
  <em>Escanea para acceder directamente a la experiencia WebVR</em>
</p>

---

## 📁 Estructura del Repositorio y Entrega

El proyecto sigue estrictamente las especificaciones de entrega de la UOC:

```text
pec3_realidad-virtual/
├── index.html              # Documento HTML raíz con visor de escenas, checklist y créditos
├── recursos/               # Subcarpeta con todos los recursos y escenas de la práctica
│   ├── arrecife360.jpg     # Fotografía panorámica 360º equirrectangular (1.6 MB)
│   ├── escena1.html        # Escena 1 interactiva con <a-sky>, hotspots y fauna animada
│   ├── escena2.html        # Escena 2 interactiva con <a-videosphere> y consola HUD 3D
│   ├── qr-github-pages.png # Código QR para acceso rápido desde dispositivos móviles/VR
│   ├── styles.css          # Hoja de estilos CSS del visor y la interfaz
│   └── video360.mp4        # Clip de vídeo 360º equirrectangular en MP4 H.264 (3.7 MB)
├── .gitignore              # Filtro para archivos de sistema (macOS .DS_Store), IDEs y zips
└── README.md               # Documentación completa del proyecto
```

* **Control de peso:** El conjunto total de recursos del proyecto ocupa tan solo **~5.4 MB**, cumpliendo holgadamente el límite de **10 MB** estipulado para la entrega comprimida.

---

## 📚 Propiedad Intelectual y Licencias

* **Imagen 360º Arrecife (Escena 1):** *"Heron Bommie SVII"* capturada con cámara subacuática Seaview SVII por © Underwater Earth / XL Catlin Seaview Survey / Christophe Bailhache. Licencia [Creative Commons Attribution-ShareAlike 3.0 (CC BY-SA 3.0)](https://creativecommons.org/licenses/by-sa/3.0/). Fuente: [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Heron_Bommie_SVII.jpg).
* **Vídeo 360º Inmersión (Escena 2):** *"Fiesa underwater 360 video vr #insta360x4"* grabado con cámara Insta360 X4 por Snicel 69. Licencia [Creative Commons Attribution 3.0 (CC BY 3.0)](https://creativecommons.org/licenses/by/3.0/). Fuente: [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Fiesa_underwater_360_video_vr_-insta360x4.webm).
* **Framework WebXR:** [A-Frame v1.8.0](https://aframe.io/) (Licencia MIT, Supermedium & Mozilla).
