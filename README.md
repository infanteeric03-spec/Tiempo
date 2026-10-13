# Tiempo

Web app de previsión del tiempo en un solo archivo (`index.html`), sin dependencias ni servidor.

## Qué hace

- Buscador de ciudades de todo el mundo.
- Ciudad predeterminada (Oviedo por defecto), que se guarda en el navegador con el botón "Hacer predeterminada".
- Tiempo actual: temperatura, sensación térmica, viento, humedad, lluvia, UV, amanecer y atardecer.
- Previsión de las próximas 24 horas.
- Previsión de 7 días. Al tocar un día se despliega su previsión hora a hora.
- Diseño adaptado al móvil, con modo claro y oscuro automático.

## Datos

Los datos vienen de [Open-Meteo](https://open-meteo.com/), que es gratuito y no requiere clave de API.

## Uso

Abre `index.html` en un navegador, o publícalo con GitHub Pages:

1. Ve a **Settings → Pages**.
2. En **Source** elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`.
3. La app quedará en `https://infanteeric03-spec.github.io/Tiempo/`.

## Instalar como app

Es una PWA: se puede instalar y abre sin conexión mostrando la última previsión guardada.

- **Android (Chrome):** menú ⋮ → *Instalar aplicación* (o *Añadir a la pantalla de inicio*).
- **iPhone (Safari):** botón Compartir → *Añadir a pantalla de inicio*.
- **Ordenador (Chrome/Edge):** icono de instalar en la barra de direcciones.

Debe abrirse desde la dirección de GitHub Pages (HTTPS); abierta como archivo local no se puede instalar.

## Archivos

- `index.html`: la app completa.
- `manifest.webmanifest`: nombre, colores e iconos de la app instalada.
- `sw.js`: service worker para el funcionamiento sin conexión. Si cambias archivos de la app, sube también el número de `VERSION`.
- `icons/`: icono (SVG y PNG, con versión *maskable* para Android).

La ciudad predeterminada se guarda en cada dispositivo por separado.
