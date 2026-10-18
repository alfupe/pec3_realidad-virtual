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

## Compatibilidad y Requisitos de Navegación

El proyecto utiliza **A-Frame 1.8.0** sobre **WebGL 2.0 / WebXR** y componentes multimedia en estándares web universales (H.264 MP4 y GLTF/GLB 2.0).

### Navegadores y versiones mínimas recomendadas
* **Google Chrome:** Versión 79 o superior (soporte completo de WebXR Device API y WebGL 2.0).
* **Mozilla Firefox:** Versión 75 o superior.
* **Apple Safari (macOS / iOS):** Versión 15.4 o superior (soporte de WebGL 2.0 y WebKit WebXR).
* **Microsoft Edge:** Versión 79 o superior (Chromium).
* **Meta Quest Browser:** Compatible de forma nativa para experiencia inmersiva completa en visor VR standalone.

### Consideraciones técnicas y Cross-Browser
1. **Protocolo y ejecución en local vs. entorno seguro (HTTPS / Localhost):**  
   Tal como se indicó en las pautas de la asignatura sobre los protocolos en A-Frame, si se intenta abrir el archivo `index.html` haciendo doble clic directamente desde el explorador de archivos, el navegador utilizará el protocolo `file://`, impidiendo la correcta carga de los modelos 3D (`.glb`), texturas y vídeos debido a las restricciones de seguridad del navegador.  
   Para probar el proyecto en local es imprescindible abrirlo bajo el protocolo `http://` arrancando un servidor web local, siendo la forma más sencilla y recomendada usar la extensión **Live Server de Visual Studio Code**. Asimismo, para el uso de la API WebXR y los sensores móviles de orientación/giroscopio en dispositivos reales, se requiere una conexión segura (**HTTPS**), requisito que cubre el despliegue público en **GitHub Pages**.

2. **Permisos de sensores en `<iframe>` (Móvil / Giroscopio):**  
   Para garantizar que la vista panorámica responda a los giroscopios y acelerómetros móviles desde dentro del marco `<iframe>`, las etiquetas incorporan la política de permisos explícita:  
   `allow="autoplay; accelerometer; gyroscope; xr-spatial-tracking; fullscreen"`.  
   En dispositivos iOS (Safari), al activar el modo VR el navegador puede solicitar confirmación de acceso a los sensores de movimiento.

3. **Políticas de Autoplay de vídeo (*Autoplay Policy*):**  
   Para evitar bloqueos de seguridad en navegadores que restringen la reproducción automática no solicitada, la Escena 2 incluye el atributo `muted` en el vídeo y un botón de control (*Reproducir / Pausar*) sincronizado que garantiza el inicio inmediato bajo cualquier circunstancia o navegador.

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
* Búsqueda y localización de recursos multimedia equirrectangulares (fotografía panorámica y clip de vídeo 360º) de temática submarina con licencias libres compatibles (Creative Commons) en repositorios abiertos como Wikimedia Commons.
* Redacción formal y normalización de los textos de créditos, atribuciones de autoría y licencias Creative Commons (CC BY-SA 3.0, CC BY 3.0 y CC BY 4.0) de los recursos multimedia y modelos 3D externos.
* Estructuración jerárquica y redacción técnica de la documentación del proyecto (`README.md`) para el repositorio.
* Generación mediante script del código QR optimizado para facilitar el acceso directo a la versión desplegada en GitHub Pages desde dispositivos móviles.
* Asistencia en la lógica matemática y de temporización para el suavizado de animaciones e interacción en A-Frame (cálculo de límites de patrullaje, rotación continua de 180º en extremos y velocidad de alejamiento y retorno de los modelos 3D ante eventos del cursor).
* Auditoría técnica de compatibilidad cross-browser y estándares WebXR / WebGL 2.0, identificando restricciones de permisos en `<iframe>` (acceso a giroscopios/acelerómetros en móviles y políticas de autoplay de vídeo) y formulando las directivas necesarias para garantizar una experiencia uniforme en navegadores de escritorio y móviles.

### Instrucciones o prompts representativos
> «Ayúdame a buscar en Wikimedia Commons fotos panorámicas y vídeos submarinos 360º en proyección equirrectangular con licencias abiertas para usar en A-Frame.»

> «A partir de estos enlaces de Wikimedia y Sketchfab con licencias CC BY-SA 3.0 y CC BY 4.0, redacta el bloque de créditos formal para index.html y README.md siguiendo las buenas prácticas de atribución académica.»

> «Genera un código QR ligero en PNG que enlace a https://alfupe.github.io/pec3_realidad-virtual/ para integrarlo en la interfaz.»

> «Ayúdame a calcular la velocidad y rotación de un modelo 3D en A-Frame para que patrulle entre -1.7 y 1.7 en X y gire fluidamente 180º al llegar a los extremos sin saltos bruscos.»

> «Configura la interacción para que al enfocar la mantarraya con el cursor se aleje suavemente en el eje Z hacia el fondo marino y regrese al retirar la mirada.»

> «Revisa si tenemos alguna preocupación de compatibilidad cross-browser o versiones mínimas de navegador en WebXR/A-Frame, y qué directivas de permisos debemos configurar en los iframes para que el giroscopio y el vídeo funcionen sin bloqueos en móviles.»

### Respuestas obtenidas
La herramienta facilitó enlaces y descriptores de búsqueda en Wikimedia Commons para localizar recursos equirrectangulares libres, aportó propuestas de redacción estructurada para la documentación y los créditos, generó el recurso gráfico QR, sugirió fragmentos de código con cálculos de coordenadas y eventos (`mouseenter`, `mouseleave`) para A-Frame, y proporcionó las directivas de Permissions Policy necesarias para los `<iframe>` (sensores de orientación y reproducción automática).

### Proceso de revisión, reelaboración y edición
El uso de estas herramientas ha tenido un carácter estrictamente consultivo, instrumental y de apoyo técnico/editorial. Tanto la concepción y enfoque submarino del proyecto, como la selección final de los recursos multimedia y la comprobación directa de sus licencias originales, su recorte y transcodificación a formatos web óptimos (MP4 H.264 y JPG), la optimización manual de geometrías y texturas 3D, el diseño de la interfaz web, la comprobación empírica de compatibilidad en dispositivos y navegadores reales (escritorio y móvil) y la verificación del correcto funcionamiento en GitHub Pages son fruto de mi propio trabajo y han sido realizados, evaluados y validados íntegramente por mí.



