# Sala de Crisis Opella · Accidente fatal en misión

Ejercicio guiado de gestión de crisis (nivel 1) para el equipo de crisis de Opella Colombia.
Escenario ficticio de entrenamiento basado en el *Tabletop Crisis Exercise · Fatal Road Accident on Duty*.

## Qué hace

1. **Contexto** y botón *Comenzar*.
2. **Evento 1:** video, ¿por qué es una situación de crisis? y selección de áreas responsables.
3. **Preguntas por evento** con temporizador (5, 5, 7 y 8 minutos), respuestas en texto y lista *¿Tuvimos en cuenta esto?*.
4. **Evento 3:** solo video.
5. **Cierre:** preguntas de cierre, resumen y comentarios finales.
6. **Reporte** en pantalla y descargable en PDF con los colores corporativos.

Las sesiones y respuestas se guardan en el navegador (localStorage) y aparecen en la pantalla de inicio, donde se pueden abrir o borrar.

## Estructura

```
index.html        Toda la aplicación (HTML, CSS y JavaScript)
videos/           evento1.mp4 … evento5.mp4  (se repiten en bucle)
audios/           evento1.mp3 … evento5.mp3  (arrancan con el video y suenan una sola vez)
```

Para cambiar un video o un audio, reemplace el archivo en su carpeta **con el mismo nombre**.
Las rutas están en la constante `MEDIA` dentro de `index.html`.

## Publicar en GitHub Pages

1. Cree un repositorio público en GitHub y suba todo el contenido de esta carpeta.
2. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
3. Elija la rama `main` y la carpeta `/ (root)` y guarde.
4. En uno o dos minutos la página queda en `https://<usuario>.github.io/<repositorio>/`.

## Notas

- El navegador solo permite sonido después de una interacción. Como el ejercicio arranca con el botón *Comenzar*, el audio suele sonar solo; si no, aparece el botón **Activar audio de fondo**.
- Las respuestas se guardan en el navegador del equipo donde se juega. Si se borran los datos del navegador, se pierden los intentos guardados: descarguen el PDF al terminar.
- Dependencia externa: [jsPDF 2.5.1](https://github.com/parallax/jsPDF) desde cdnjs, para generar el PDF.
