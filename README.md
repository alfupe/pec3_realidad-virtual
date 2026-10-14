# PEC 3: Tutorial de A-FRAME 360º

**Asignatura:** Realidad virtual (Semestre 2627/1)  
**Estudiante:** Alejandro Fuentes Pérez (`alfupe@uoc.edu`)  
**Grado:** Grado de Multimedia - Universitat Oberta de Catalunya (UOC)  

---

## 📌 Descripción del Proyecto

Este proyecto corresponde a la **PEC3** de la asignatura de *Realidad Virtual*. El objetivo es la creación de dos escenas inmersivas de realidad virtual con fondo panorámico de 360º usando el framework **A-Frame**:

1. **Escena 1**: Fondo panorámico 360º estático basado en imagen equirrectangular mediante la etiqueta `<a-sky>`.
2. **Escena 2**: Fondo panorámico 360º dinámico basado en vídeo equirrectangular mediante la etiqueta `<a-videosphere>`.

Ambas escenas están incrustadas dentro de un documento principal (`index.html`) mediante elementos `<iframe>`, permitiendo alternar y visualizar cada una de ellas de forma interactiva y responsiva.

---

## 🌐 Acceso al Proyecto en GitHub Pages

El proyecto se encuentra publicado y accesible públicamente a través de GitHub Pages en el siguiente enlace:

🔗 **[https://alfupe.github.io/pec3_realidad-virtual/](https://alfupe.github.io/pec3_realidad-virtual/)**

### 📱 Código QR de acceso directo

Para probar la experiencia directamente desde un dispositivo móvil o visor VR sin necesidad de escribir la URL en el navegador:

<p align="center">
  <img src="recursos/qr-github-pages.png" alt="Código QR GitHub Pages PEC3" width="220">
  <br>
  <em>Escanea con la cámara de tu smartphone o visor VR para abrir la experiencia WebVR</em>
</p>

---

## 📁 Estructura del Repositorio

Siguiendo las pautas de entrega establecidas en el enunciado:

```text
pec3_realidad-virtual/
├── index.html              # Documento HTML principal con visor e interfaz
├── recursos/               # Subcarpeta con todos los recursos y escenas
│   ├── escena1.html        # Escena 1: Panorámica 360º con <a-sky>
│   ├── escena2.html        # Escena 2: Vídeo 360º con <a-videosphere>
│   ├── styles.css          # Estilos CSS de la interfaz contenedora
│   └── qr-github-pages.png # Código QR para acceso rápido desde móviles/visores
└── README.md               # Documentación y descripción del proyecto
```

---

## 🛠️ Tecnologías Utilizadas

* **A-Frame** (WebXR / Three.js framework)
* **HTML5** & **CSS3**
* **Git** & **GitHub Pages**
