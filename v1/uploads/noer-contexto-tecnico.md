# NoER — Contexto técnico (para Claude Design)

> Nota: este documento cubre **solo restricciones técnicas**. La info de marca (paleta, tipografía, logo) no está incluida a propósito porque está en proceso de actualización (rebrand de logo reciente) — se define por separado.

## Qué es la app
PWA (Progressive Web App) de movilidad local: remises habilitados + cadetería, para un solo pueblo (sin multiciudad). No es una web común ni una app nativa.

## Stack
- **React + TypeScript + Vite**
- **CSS plano a mano** — no hay Tailwind, Bootstrap ni librería de componentes (Material UI, Chakra, etc.)
- No hay sistema de diseño previo que limite: libertad real sobre formas, espaciados y estilos de botones/tarjetas
- Contrapartida: todo lo que se proponga lo construye el desarrollador a mano — cuanto más reutilizable y consistente sea el sistema de estilos (mismo radio de borde, misma escala de espaciado, mismos tamaños de botón en todas las pantallas), más rápido se implementa

## Comportamiento como PWA
- Se instala desde el navegador ("agregar a pantalla de inicio")
- Una vez instalada, se abre **sin barra de navegador** — pantalla completa, como app nativa
- El diseño necesita su propia forma de mostrar "dónde estoy" (headers, botón de volver) — no hay barra de URL ni botones del navegador que ayuden

## Responsive
- **Mobile-first**, con un **único breakpoint en 720px**
- Diseñar siempre primero pensando en celular; el desktop es secundario y hoy tiene tratamiento mínimo

## Accesibilidad / movimiento
- La app respeta la configuración de sistema "reducir movimiento" (iOS/Android/Windows) — si está activada, las animaciones se apagan
- Cualquier animación o transición debe ser decorativa, no la única forma de entender un cambio de estado (tiene que tener sentido también sin ella)

## Íconos y caché
- Hay un service worker (caché offline) que guarda el ícono y el manifest de la PWA
- El ícono/logo **no se actualiza al instante** para quienes ya tienen la app instalada — el desarrollador tiene que "romper" esa caché a propósito al cambiar de marca
- No afecta el diseño en sí, pero es relevante para planificar el día de un anuncio de rebrand

## Mapa
- Google Maps (JavaScript API), no es un mapa propio
- Se puede aplicar un estilo de color personalizado al mapa (ocultar POIs, cambiar color de agua/calles, vía "Google Maps Styling") — es opcional, no bloquea el prototipo si no se hace

## Assets / imágenes
- No hay optimización automática de imágenes — los archivos se sirven tal cual se suben, sin compresión ni conversión
- Los assets (logo, fondos) deben entregarse ya optimizados en peso, especialmente imágenes de fondo grandes — si pesan mucho, la app carga más lento en el celular, sobre todo con señal de datos limitada

## Sistema de color (estructura, no valores)
- La app usa colores conectados a estados reales del sistema: **éxito / alerta / error / info**, más **1 color de marca**
- Cualquier paleta nueva que se proponga debe conservar esa misma cantidad de roles semánticos, porque están atados a estados funcionales reales (viaje confirmado, viaje cancelado, documento por vencer, etc.) que la app usa de forma consistente
- Los valores de color específicos no van en este documento — se definen aparte con la marca actualizada
