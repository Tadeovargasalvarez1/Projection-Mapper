# 🎥 Projection Mapper

> **Mapeo de proyección en tiempo real directamente desde tu navegador.**  
> Un solo archivo HTML, cero dependencias locales, cero configuración.

Un software de **Projection Mapping / Video Mapping** minimalista y ultra potente construido con **Three.js** y **WebGL**. Diseñado bajo la filosofía de *"doble clic y proyectar"*: ábrelo en Google Chrome o Edge, conecta tu proyector como pantalla extendida y calibra tus visuales en vivo sobre paredes, objetos y estructuras.

---

## ✨ Características Principales

* ⚡ **Zero-Install (Single File):** Toda la aplicación (HTML, CSS y JS modular) reside en un único archivo autónomo de menos de 45 KB.
* 🖥️ **Salida Limpia para Proyector:** Utiliza la API nativa `canvas.captureStream(60)` para emitir video a 60 FPS sin latencia a una ventana secundaria sin UI, sin bordes y sin cursor del mouse visible.
* 📐 **Deformación en Perspectiva (Corner-Pin Warp):** Malla cuádruple interactiva de 4 esquinas para ajustar la proyección milimétricamente al ángulo del espacio físico.
* 🎨 **Soporte Multimedia Total:**
  * Colores sólidos personalizables.
  * Degradados lineales procedurales.
  * Carga y renderizado de imágenes (`PNG`, `JPG`, `WebP`).
  * Reproducción fluida de videos en bucle (`MP4`, `WebM`).
* ⭕ **Máscaras y Formas Flexibles:** Rectángulos, círculos perfectos por shader alpha, polígonos regulares y herramienta de dibujo libre (trazado a mano alzada).
* 📑 **Gestor de Capas:** Panel lateral estilo editor profesional con selección rápida, duplicación, opacidad independiente y reordenamiento.
* 🧠 **Sistema de Auto-Monitoreo y Optimización:**
  * Medidor de FPS continuo.
  * Ajuste dinámico de resolución (`pixelRatio`) para mantener fluidez en equipos de bajos recursos.
  * Alertas preventivas al detectar escenas muy cargadas (>12 superficies o >3 videos).
* 💾 **Persistencia Automática:** Auto-guardado en segundo plano en `localStorage` cada 30 segundos; tus cambios sobreviven a recargas accidentales.

---

## 🚀 Inicio Rápido

1. **Descarga** el archivo `projection-mapper.html`.
2. **Ábrelo** con doble clic en cualquier navegador moderno (Chrome, Edge o Firefox recomendados).
3. ¡Listo! Ya estás en el lienzo de mapeo.

---

## 📽️ Cómo usar con un Proyector

1. Conecta tu proyector por HDMI, DisplayPort o USB-C a tu computadora.
2. En tu sistema operativo, configura la pantalla en modo **"Extender pantalla"** (en Windows: `Win + P` ➔ **Extender**).
3. Mantén la ventana de control con los botones en tu monitor principal.
4. Presiona el botón azul **`▶ Proyectar`**.
5. Se abrirá una ventana emergente completamente negra. **Arrástrala a la pantalla del proyector**.
6. En la pantalla del proyector presiona la tecla **`F`** para activar pantalla completa nativa.
7. Desde tu laptop, arrastra las esquinas azules en la interfaz para hacer coincidir las formas con el objeto físico.

---

## ⌨️ Atajos de Teclado

| Tecla | Acción |
| :---: | :--- |
| `R` | Crear nuevo Rectángulo |
| `C` | Crear nuevo Círculo |
| `P` | Crear nuevo Polígono |
| `D` | Alternar modo Dibujo libre |
| `Supr` / `Backspace` | Eliminar superficie seleccionada |
| `Esc` | Deseleccionar / Cancelar trazado |
| `Ctrl + S` | Guardar proyecto en memoria |
| `F` *(en ventana proyector)* | Pantalla completa (Fullscreen) |
| `Esc` *(en ventana proyector)* | Salir de pantalla completa / Cerrar salida |

---

## 🛠️ Stack Tecnológico

* **Motor Gráfico:** [Three.js](https://threejs.org/) (r160) vía ES Module / CDN.
* **Render:** WebGL con proyección ortográfica normalizada `[0,1]`.
* **Streaming de Salida:** MediaStream Web API (`HTMLCanvasElement.captureStream`).
* **Estilos:** CSS3 nativo con CSS Grid, soporte Retina / HiDPI (`devicePixelRatio`) y tema oscuro moderno.

---

## 📝 Licencia

Este proyecto está bajo la Licencia **MIT**. Eres libre de usarlo, modificarlo y adaptarlo para proyectos artísticos, comerciales o educativos.
