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

La ciudad predeterminada se guarda en cada dispositivo por separado.
