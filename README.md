# Tiempo

Web app de previsión del tiempo en un solo archivo (`index.html`), sin dependencias ni servidor.

## Qué hace

- Buscador de ciudades de todo el mundo.
- Ciudad predeterminada (Oviedo por defecto), que se guarda en el navegador con el botón "Hacer predeterminada".
- Botón de ubicación para ver el tiempo donde estás, y opción "Abrir siempre con mi ubicación". El navegador pide permiso la primera vez; la ubicación no sale del dispositivo, solo se envían las coordenadas a Open-Meteo y a BigDataCloud para obtener el tiempo y el nombre del lugar.
- Tiempo actual: temperatura, sensación térmica, viento, humedad, lluvia, UV, amanecer y atardecer.
- Previsión de las próximas 24 horas. Al tocar una hora se abre su detalle: sensación térmica, lluvia en mm, viento con rachas, humedad, nubosidad, índice UV y un resumen en una frase. En "Más detalles": presión, visibilidad, punto de rocío y nieve.
- Previsión de 7 días. Al tocar un día se despliega su previsión hora a hora.
- Pestaña **Playas con niños**: ordena 13 playas de Asturias por comodidad en la arena (de 0 a 100) según viento, rachas y oleaje en el día y la franja elegidos (mañana 10–14 h o tarde 15–20 h). Avisa del viento de tierra por el riesgo para flotadores y colchonetas. Muestra la curva de marea del día con pleamares y bajamares; la tarjeta se puede plegar y la app recuerda si la dejaste abierta o cerrada. Se puede abrir directamente con `#playas`, y la app instalada tiene un acceso directo.
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

## Playas: datos y límites

La lista está al principio del bloque «Playas de Asturias con niños» de `index.html` (`BEACHES`). Cada playa tiene posición aproximada, orientación y un nivel de abrigo (`alto`, `medio`, `bajo`) tomado de las descripciones de Turismo Asturias y asturias.com. La orientación se supone norte para todas. Los modelos meteorológicos tienen celdas de varios kilómetros, así que lo que distingue a una playa de otra es sobre todo su abrigo, no una medición local. Las mareas (pleamar y bajamar) salen del nivel del mar que calcula Open-Meteo Marine: son horas aproximadas, pueden variar media hora o más, y conviene contrastarlas con una tabla de mareas. Siete playas llevan indicada la marea con la que van mejor, según las guías de turismo (`tide` y `tideWhy` en `BEACHES`).
