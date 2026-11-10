# Código Rojo Digital

Escape room de cierre del Periodo 2 (Cultura digital I). Página estática para GitHub Pages con Firebase como base de datos compartida.

## Qué va a GitHub

Sube solo esta carpeta: `index.html`, `roster.js`, `firebase-config.js`, `firestore.rules` y este README.
**No subas** `lista_maestra_cultura_digital_I_sec2.csv`: tiene los nombres completos de los alumnos.
`roster.js` contiene únicamente huellas cifradas (no hay nombres legibles).

## Pasos (unos 15 minutos)

1. **Firebase.** Entra a console.firebase.google.com con tu cuenta, crea un proyecto (sin Analytics).
2. **Autenticación.** Build > Authentication > Comenzar > Método de acceso > activa **Anónimo**.
3. **Base de datos.** Build > Firestore Database > Crear base de datos (modo producción). En la pestaña **Reglas**, pega el contenido de `firestore.rules` y publica.
4. **Datos de la app web.** Configuración del proyecto > Tus apps > icono `</>` (Web). Copia `apiKey`, `authDomain`, `projectId` y `appId` y pégalos en `firebase-config.js`. Esos datos son públicos por diseño; la protección está en las reglas.
5. **Dominio autorizado.** Authentication > Configuración > Dominios autorizados > agrega `TU-USUARIO.github.io`.
6. **GitHub.** Crea un repositorio, sube los 5 archivos, y en Settings > Pages elige la rama `main` y la carpeta `/ (root)`. La página queda en `https://TU-USUARIO.github.io/NOMBRE-REPO/`.
7. **Prueba tú primero** con dos dispositivos distintos antes de la clase.

## Cómo entra cada alumno

Escribe su nombre y primer apellido como aparecen en Schoology (acepta acentos, mayúsculas y orden "Nombre Apellido" o "Apellido Nombre"). Si vuelve a entrar desde otro dispositivo con el mismo nombre, recupera su avance.

## Acceso docente

En la pantalla de entrada, abre "Acceso docente". Ahí ves avance, puntos, claves de cada puerta, hallazgos con IA y reflexiones. Si cargas tu CSV maestro (se lee solo en tu navegador), también ves quién falta por entrar.
Es una protección ligera: sirve para un salón, no para datos sensibles.

## Después de la actividad

Borra los datos con "Reiniciar sesión" en el panel docente, o elimina el proyecto de Firebase.

## Límites conocidos

- Las respuestas y las claves están en el código de la página; un alumno técnico podría encontrarlas.
- Las reglas de Firestore permiten escribir a cualquier sesión anónima de la página; un alumno podría tocar el avance de otro si inspecciona el sitio.
- Si el repositorio es público, el código y `roster.js` son visibles para cualquiera.
