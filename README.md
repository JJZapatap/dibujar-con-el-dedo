# ✏️ Dibujar con el dedo

Aplicación web que permite **dibujar con el dedo índice** usando la cámara del dispositivo y el modelo **MediaPipe Hand Landmarker** de Google.

![Demo](https://img.shields.io/badge/MediaPipe-Hand%20Landmarker-blue) ![JS](https://img.shields.io/badge/JavaScript-ES%20Modules-yellow) ![Licencia](https://img.shields.io/badge/Licencia-MIT-green)

## Cómo usarlo

1. Abre el archivo `index.html` en un navegador moderno (Chrome, Edge, Firefox).
2. **Importante**: necesita HTTPS o `localhost` para poder usar la cámara.
3. Pulsa **Iniciar cámara** y acepta el permiso.
4. Extiende el dedo índice frente a la cámara → el trazo sigue la punta del dedo.
5. Puedes cambiar el color, el grosor, borrar el dibujo o guardarlo como PNG.

### Servidor local rápido

```bash
# Con Node.js
npx serve .

# O con Python
python -m http.server 8000
```

Luego abre `http://localhost:3000` (o el puerto que indique).

## Características

- Detección en tiempo real de la mano (21 landmarks)
- Dibujo suave siguiendo el **landmark 8** (punta del índice)
- Vídeo espejado (como un espejo)
- Selector de color y grosor
- Botón para borrar y para guardar la imagen
- Funciona 100 % en el navegador (sin backend)

## Tecnologías

- [MediaPipe Tasks Vision](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker/web_js) (`@mediapipe/tasks-vision`)
- HTML5 Canvas + `getUserMedia`
- JavaScript moderno (ES modules + CDN)

## Estructura

```
.
├── index.html   # Toda la aplicación
└── README.md
```

## Licencia

MIT — úsalo libremente.
