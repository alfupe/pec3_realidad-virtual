# PEC 3: Tutorial de A-FRAME 360º

**Asignatura:** Realidad virtual (Semestre 2627/1)  
**Estudiante:** Alejandro Fuentes Pérez (`alfupe@uoc.edu`)  
**Grado:** Grado de Multimedia - Universitat Oberta de Catalunya (UOC)  

---

## Descripción del Proyecto

Práctica correspondiente a la PEC3 de Realidad Virtual. Consiste en la creación de dos escenas inmersivas en 360º utilizando A-Frame:

1. **Escena 1 (Foto 360º):** Utiliza la etiqueta `<a-sky>` con una imagen panorámica equirrectangular de un arrecife de coral. Se incorpora un modelo 3D externo (`pez.glb`) con patrulla horizontal continua, giro suave de 180º en los extremos e interacción reactiva de huida mediante el cursor (`mouseenter` y `mouseleave`).
2. **Escena 2 (Vídeo 360º):** Utiliza la etiqueta `<a-videosphere>` con un clip de vídeo submarino 360º en formato MP4 compatible. Incorpora un modelo 3D de mantarraya (`mantaraya.glb`) con planeo suave en la corriente e interacción reactiva en profundidad (se sumerge alejándose en el eje Z al enfocarla con el cursor y regresa suavemente), además de control interactivo de reproducción/pausa.

Ambas escenas están incrustadas en el archivo principal `index.html` mediante etiquetas `<iframe>` siguiendo las instrucciones del [paso 7 del tutorial](https://github.com/hannibalov/mindar/wiki/aframe-7-iframe-es) de la asignatura.

---

## Acceso al Proyecto en GitHub Pages

El proyecto se puede visualizar en GitHub Pages en la siguiente dirección:

[https://alfupe.github.io/pec3_realidad-virtual/](https://alfupe.github.io/pec3_realidad-virtual/)

### Código QR de acceso

<p align="center">
  <img src="recursos/qr-github-pages.png" alt="Código QR GitHub Pages" width="200">
</p>

---

## Estructura de archivos

```text
pec3_realidad-virtual/
├── index.html              # Documento principal con selector de escenas e iframes
├── recursos/               # Carpeta de recursos del proyecto
│   ├── arrecife360.jpg     # Imagen panorámica equirrectangular 360º
│   ├── escena1.html        # Escena 1 (<a-sky> y pez 3D)
│   ├── escena2.html        # Escena 2 (<a-videosphere> y mantarraya 3D)
│   ├── mantaraya.glb       # Modelo 3D de mantarraya
│   ├── pez.glb             # Modelo 3D de pez mariposa
│   ├── qr-github-pages.png # Código QR para acceso móvil
│   ├── styles.css          # Hoja de estilos del visor
│   └── video360.mp4        # Vídeo submarino 360º en formato MP4
├── .gitignore
└── README.md
```

---

## Créditos y recursos utilizados

* **Imagen panorámica 360º (Escena 1):** [Heron Bommie SVII](https://commons.wikimedia.org/wiki/File:Heron_Bommie_SVII.jpg) por © Underwater Earth / XL Catlin Seaview Survey / Christophe Bailhache, bajo licencia [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/).
* **Modelo 3D (Escena 1):** ["Stylized Butterfly Fish | Game Ready Model"](https://skfb.ly/pMEuW) por SammyCAnimations, bajo licencia [Creative Commons Attribution (CC BY 4.0)](http://creativecommons.org/licenses/by/4.0/).
* **Vídeo 360º (Escena 2):** [Fiesa underwater 360 video vr](https://commons.wikimedia.org/wiki/File:Fiesa_underwater_360_video_vr_-insta360x4.webm) por Snicel 69, bajo licencia [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/).
* **Modelo 3D (Escena 2):** ["Stylized Rare Stingray | Game Ready Model"](https://skfb.ly/pMEuE) por SammyCAnimations, bajo licencia [Creative Commons Attribution (CC BY 4.0)](http://creativecommons.org/licenses/by/4.0/).
* **Librería WebVR:** [A-Frame 1.8.0](https://aframe.io/).

---

## Declaración de uso de Inteligencia Artificial (IA)

Siguiendo las directrices institucionales de la UOC sobre el uso ético, crítico y responsable de las herramientas de Inteligencia Artificial en las actividades de evaluación, se detalla a continuación el alcance de su empleo en la realización de esta práctica:

### Herramienta utilizada
Asistente de Inteligencia Artificial (Gemini / Antigravity).

### Objetivos perseguidos
* Redacción formal y normalización de los textos de créditos, atribuciones de autoría y licencias Creative Commons (CC BY-SA 3.0, CC BY 3.0 y CC BY 4.0) de los recursos multimedia y modelos 3D externos.
* Estructuración jerárquica y redacción técnica de la documentación del proyecto (`README.md`) para el repositorio.
* Generación mediante script del código QR optimizado para facilitar el acceso directo a la versión desplegada en GitHub Pages desde dispositivos móviles.
* Asistencia en la lógica matemática y de temporización para el suavizado de animaciones e interacción en A-Frame (cálculo de límites de patrullaje, rotación continua de 180º en extremos y velocidad de alejamiento y retorno de los modelos 3D ante eventos del cursor).

### Instrucciones o prompts representativos
> «A partir de estos enlaces de Wikimedia y Sketchfab con licencias CC BY-SA 3.0 y CC BY 4.0, redacta el bloque de créditos formal para index.html y README.md siguiendo las buenas prácticas de atribución académica.»

> «Genera un código QR ligero en PNG que enlace a https://alfupe.github.io/pec3_realidad-virtual/ para integrarlo en la interfaz.»

> «Ayúdame a calcular la velocidad y rotación de un modelo 3D en A-Frame para que patrulle entre -1.7 y 1.7 en X y gire fluidamente 180º al llegar a los extremos sin saltos bruscos.»

> «Configura la interacción para que al enfocar la mantarraya con el cursor se aleje suavemente en el eje Z hacia el fondo marino y regrese al retirar la mirada.»

### Respuestas obtenidas
La herramienta proporcionó propuestas de redacción estructurada para la documentación y los créditos, generó el recurso gráfico QR y sugirió fragmentos de código con los cálculos de coordenadas y escuchadores de eventos (`mouseenter`, `mouseleave`) para la interacción en A-Frame.

### Proceso de revisión, reelaboración y edición
El uso de la herramienta ha sido estrictamente instrumental, consultivo y de soporte técnico/editorial. La delimitación temática del entorno submarino, la búsqueda y selección de recursos gráficos según las directrices de la PEC, la optimización manual de geometrías y texturas 3D para cumplir de forma estricta la restricción de peso (< 10 MB), el diseño de la interfaz web y la verificación del correcto funcionamiento en el visor web y en GitHub Pages han sido realizados, evaluados y validados íntegramente por el estudiante.

