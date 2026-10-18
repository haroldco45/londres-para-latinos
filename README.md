# Londres para Latinos 🇬🇧🌎

Guía de supervivencia bilingüe (español / English) para latinos que llegan a Londres.
PWA instalable, hecha en HTML + JavaScript puro, sin servidor propio.

**Desarrollada por Vibras Positivas HM — Derechos de Autor Reservados**

🔗 https://haroldco45.github.io/londres-para-latinos/

## Qué trae

| Módulo | Qué hace |
|---|---|
| 🏰 Lugares de interés | 34 lugares con foto real, descripción, consejo, estación, si es gratis o de pago, ficha con historia de Wikipedia en español, pronunciación del nombre, "Cerca de mí", lista "Quiero ir / Ya fui" y 6 itinerarios de un día dibujados en el mapa |
| 🗺️ Mapa | Mapa interactivo: consulado de Colombia, IRMO, Casa Latina, LAWRS, urgencias (A&E), barrios latinos, lugares y aeropuertos. "Dónde estoy", paradas cercanas y líneas del metro dibujadas desde TfL |
| 🚇 Metro y bus | Planificador de rutas, estado de líneas y próximas llegadas **en vivo** (API oficial de TfL); tarifas 2026 y cómo usar contactless/Oyster |
| 💬 Frases | 14 situaciones (migración, metro, perdido, bus, restaurante, farmacia, médico GP, 999, policía, arriendo, entrevista, banco, charla) con audio en inglés británico y pronunciación para hispanohablantes |
| 🆘 SOS | 999 / 111 / 101 con un toque, organizaciones latinas y oficiales, y guías "¿qué hago si…?" |
| ✅ Primeros días | Lista de pasos que se guarda en el celular + requisitos de visa/ETA |
| 🩺 Salud (NHS) | A dónde ir según el problema (farmacia → GP → 111 → urgencias), cómo registrarse con un GP, costos, dentista, salud mental |
| 💼 Trabajo y estudio | Derecho a trabajar, NI number, derechos laborales, dónde buscar, ESOL, convalidar títulos y calculadora de pago que avisa si está bajo el salario mínimo |
| 🏠 Vivienda | Señales de estafa, depósito y su protección, Right to Rent, lista para revisar antes de firmar |
| 🫓 Comida latina | Zonas con productos de casa y nombres de alimentos en inglés con audio |
| 🧥 Clima y maleta | Ropa por mes, temperaturas promedio, horas de luz y próximos festivos (gov.uk en vivo) |
| 💷 Dinero | Cambio en vivo GBP ↔ COP, USD, EUR, MXN, PEN, CLP, ARS, VES, BRL; salario mínimo 2026 |
| ☕ Costumbres, 🛡️ Seguridad, 📸 Fotos y videos | Cultura, jerga, riesgos reales, fotos reales de Wikimedia Commons y videos |
| 📍 Mi dirección | Botón "Llévame a casa" y tarjeta en inglés para mostrar si te pierdes |

Encabezado con hora real de Londres y de Colombia (America/Bogota) y diferencia horaria automática (cambia sola el 25 de octubre de 2026 cuando Londres pasa a GMT).

## Datos verificados (octubre 2026)

- Bus/tranvía £1.75 hasta el 31 oct 2026; TfL anunció £1.85 desde el 1 nov 2026 (la app cambia el valor sola en esa fecha). Tope diario solo bus £5.25 → £5.55.
- Metro zona 1: £3.10 pico / £3.00 fuera de pico (desde 1 mar 2026). Tope diario zonas 1–2: £8.90, congelado hasta marzo 2027.
- Salario mínimo (National Living Wage, 21+): £12.71/h desde 1 abr 2026.
- Colombianos: visa de visitante obligatoria desde 26 nov 2024 (no aplica ETA). ETA para otros países: £20 desde 8 abr 2026.

Revisar estos valores cada abril/marzo, cuando cambian tarifas y salario.

## APIs usadas (gratis, sin clave)

- Transport for London Unified API — `api.tfl.gov.uk` (Powered by TfL Open Data)
- Open-Meteo (clima), ExchangeRate-API `open.er-api.com` (cambio), Wikipedia REST (fotos)
- Mapa: Leaflet + OpenStreetMap / CARTO

Si la app tiene mucho tráfico, sacar una clave gratis en https://api-portal.tfl.gov.uk y agregar `?app_key=...` a las llamadas de TfL.

## Archivos

```
index.html     App completa
manifest.json  PWA
sw.js          Service worker (funciona sin internet lo ya visitado)
icon-192.png, icon-512.png
og-image.png   Imagen para compartir en WhatsApp/redes (1200×630)
```

## Publicar en GitHub Pages

1. Crear el repositorio `londres-para-latinos` en github.com/haroldco45.
2. Subir todos los archivos a la raíz.
3. Settings → Pages → Branch `main` / root → Save.
4. Netlify se actualiza solo desde el repo.

Privacidad: la dirección y la lista de pasos se guardan solo en el navegador del usuario (localStorage); la app no recoge datos personales.
