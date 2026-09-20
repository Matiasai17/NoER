# NoER — Prototipo interactivo

Prototipo de la app de movilidad y cadetería de Nogoyá, con navegación completa entre pantallas dentro de un marco de iPhone.

## Ver el prototipo

👉 **https://matiasai17.github.io/NoER/**

(GitHub Pages puede tardar 1–2 minutos en activarse después del primer push).

## Qué se puede probar

- Iniciar sesión con Google, Facebook o número de teléfono
- Elegir entre **Versión normal** o **Versión simple** (letra grande, para adultos mayores o baja visión), cambiable después desde Cuenta
- Pedir un viaje o una encomienda desde "¿A dónde vas?" (con búsqueda por voz)
- Elegir destino en el buscador o directamente en el mapa, ver el desglose de precio y confirmar
- Flujo propio de encomienda: quién recibe, qué se manda, cobrar al entregar y quién paga el envío
- Ver el chofer asignado, el estado del viaje paso a paso, y calificar al llegar
- Comprobante y recibo por viaje (descargar PDF / enviar por WhatsApp)
- Pantallas de "sin servicio" / sin conexión, probables desde **Cuenta → Modo demo**
- Revisar las pestañas Pedidos, Billetera, Avisos y Cuenta
- Activar el modo oscuro desde el header o desde Cuenta
- Arrastrar una foto sobre el avatar en Cuenta

Es un prototipo de muestra (sin backend real): los datos son de ejemplo.

## Notas técnicas

Es un archivo `index.html` autónomo que carga React, ReactDOM y Babel desde un CDN para interpretar `ios-frame.jsx` en tiempo real. Requiere conexión a internet para abrirse.
