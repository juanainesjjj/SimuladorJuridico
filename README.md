# Simulador Jurídico EDOMEX — PWA (Instalable)

Este paquete contiene una app web progresiva (PWA) lista para desplegar en **cualquier hosting estático**.

## Archivos
- `index.html` — Aplicación React (JSX en navegador con Babel). Incluye registro del Service Worker.
- `service-worker.js` — Cachea los archivos esenciales para uso offline.
- `manifest.webmanifest` — Metadatos de instalación PWA (icono, tema, nombre).
- `assets/icon-256.svg` — Ícono de la app.
- `rules-example.json` — Ejemplo de reglas externas.

## Cómo desplegar
1. Sube todos los archivos a una **URL HTTPS** (GitHub Pages, Vercel, Netlify, S3+CloudFront, etc.).
2. Asegúrate de servir con cabecera correcta para `manifest.webmanifest` (`application/manifest+json` o `application/json`).
3. Abre la URL en Chrome/Edge/Safari móvil y usa **Instalar app** / **Agregar a pantalla de inicio**.

## Cargar reglas desde URL segura
- En la sección “Cargar reglas desde URL segura” pega la URL del JSON (por ejemplo, `https://tu-dominio/reglas-simulador.json`).
- (Opcional) Si tu endpoint requiere token, ingrésalo en el campo **Bearer**.
- La app guardará una **caché local** (puedes borrarla desde el mismo panel).

## Desarrollo local
- Puedes abrir `index.html` directamente en tu navegador (Chrome permite SW en `file://` solo en algunos casos). Idealmente usa un servidor local:
  ```bash
  npx serve .
  # o
  python3 -m http.server 8080
  ```
  Luego visita `http://localhost:8080`.

## Nota
Esta herramienta es de **apoyo** y no sustituye la función jurisdiccional. Verifica la **normatividad vigente**.
