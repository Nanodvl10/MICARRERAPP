# CARRERAAP

Mi app personal de carreras de trail (PWA): dieta y plan por días, ritmos km a km,
perfil y mapa del recorrido, y modo carrera con GPS para el día D.

**App:** https://nanodvl10.github.io/CARRERAAP/

## Estructura
- `index.html`, `app.js`, `styles.css`, `profile.js`, `manifest.json`, `service-worker.js`, iconos → la app.
- `races/` → un archivo por carrera + `registry.js` (lista de carreras) + `_PLANTILLA.js`.
- `strava-sync/` → sincronización opcional con Strava desde el homelab (no afecta a la app).

## Añadir una carrera
1. Crear `races/nombre-carrera.js` (a partir de `_PLANTILLA.js` o generado con Claude desde el GPX).
2. Añadir `"nombre-carrera.js"` a `races/registry.js`.
3. Añadir `'races/nombre-carrera.js'` a la lista `ASSETS` de `service-worker.js` (para que funcione sin conexión).
