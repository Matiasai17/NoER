# NoER — Prototipo interactivo

Prototipo de la app de movilidad y cadetería de Nogoyá, con navegación completa entre pantallas dentro de un marco de iPhone.

## Ver el prototipo

👉 **https://matiasai17.github.io/NoER/**

(GitHub Pages puede tardar 1–2 minutos en activarse después del primer push).

## Qué se puede probar

- Pedir un viaje o una encomienda desde "¿A dónde vas?"
- Elegir destino, ver el desglose de precio y confirmar
- Ver el chofer asignado, el estado del viaje paso a paso, y calificar al llegar
- Revisar las pestañas Pedidos, Billetera, Avisos y Cuenta
- Activar el modo oscuro desde Cuenta
- Arrastrar una foto sobre el avatar en Cuenta

Es un prototipo de muestra (sin backend real): los datos son de ejemplo.

## Notas técnicas

Es un archivo `.html` autónomo que carga React, ReactDOM y Babel desde jsDelivr para
interpretar `ios-frame.jsx` en tiempo real. Requiere conexión a internet para abrirse.
