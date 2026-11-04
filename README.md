# Sala de Crisis Opella · Accidente fatal en misión

Ejercicio guiado de gestión de crisis (nivel 1) para el equipo de crisis de Opella Colombia.
Escenario ficticio de entrenamiento basado en el *Tabletop Crisis Exercise · Fatal Road Accident on Duty*.

## Qué hace

1. **Contexto** y botón *Comenzar*.
2. **5 eventos**, cada uno con su video (en bucle) y audio de fondo. El evento 3 es solo video; las preguntas de los eventos 3 y 4 van en el evento 4.
3. **Evento 1:** ¿por qué es una situación de crisis? y selección de áreas responsables.
4. **En los eventos 1, 2, 4 y 5**, desde que se inicia el temporizador (10, 10, 12 y 13 minutos), en este orden:
   1. **FISA** propio del evento (Hechos, Impactos, Partes interesadas, Plan de acción). Se toca el título de cada punto y se abre una ventana con todos sus campos. En Impactos se llena la tabla Humano / Actividades / Legal / Imagen y reputación / Entorno × Inmediato / Futuro / Potencial y se marcan los más importantes. Desde el evento 2 se puede continuar con una copia del FISA anterior (el original no cambia) o empezar uno nuevo.
   2. **Encargados:** qué hará cada área activada.
   3. **Preguntas** del evento.
   - Al terminar: lista *¿Tuvimos en cuenta esto?*.
5. **Cierre:** preguntas de cierre, resumen y comentarios finales.
6. **Reporte** en pantalla y en PDF con los colores corporativos: tablero FISA y tabla de análisis de impactos por evento, encargados, preguntas y retroalimentación.

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
