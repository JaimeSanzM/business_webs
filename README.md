# My Dentist Querétaro — Web

Web oficial de **My Dentist (VyDentist)**, clínica dental en el Centro de Querétaro
(Plaza Lecaroz, Av. Constituyentes). Rama `my_dentist_qro` del repositorio `business_webs`.

> **Una razón para sonreír.**

## Stack

- **100% HTML/CSS/JS vanilla** — cada web es un único archivo autocontenido, sin frameworks ni build.
- Sin npm, sin bundler, sin dependencias externas salvo Google Fonts.
- Marca propia inline en SVG (logo + favicon en `assets/`).

## Las 3 webs (elige una)

Tres direcciones de diseño distintas para el **mismo** negocio y contenido.
Estilo inspirado en clínicas premium tipo *dentaloth*, con alma propia de My Dentist
(azul marino + cian de la marca, y el lema *"Una razón para sonreír"*).

| Archivo | Concepto | Tipografía | Tono |
|---|---|---|---|
| `v1.html` | **Clínica Premium** — la insignia, cálida y sofisticada, con hero, tarjetas de servicios, sección doctor y testimonios. | Fraunces + Outfit | Confianza premium |
| `v2.html` | **Moderno & Bold** — vibrante, geométrico y amable, con formas redondeadas, stats y color. | Poppins | Cercano y enérgico |
| `v3.html` | **Editorial Minimal** — minimalista, mucho aire, índice de servicios y grandes citas serif. | Cormorant Garamond + Manrope | Elegante y sobrio |

## Funcionalidades (en las 3)

| Feature | Descripción |
|---|---|
| Multiidioma ES/EN | Sistema i18n propio en JS + detección del idioma del navegador (dental tourism) |
| Horario en vivo | Badge "Abierto/Cerrado ahora" calculado con la hora real y día resaltado |
| Formulario → WhatsApp | El formulario arma el mensaje y abre WhatsApp (wa.me) listo para enviar |
| WhatsApp flotante | Botón fijo bottom-right |
| Servicios | Ortodoncia, implantes, diseño de sonrisa, endodoncia, odontopediatría, limpieza/blanqueamiento |
| Testimonios | Reseñas de pacientes (carrusel en v3) |
| FAQ SEO/AEO | Preguntas redactadas como se le pregunta a Google/ChatGPT ("mejor dentista en Querétaro") |
| Schema.org JSON-LD | Tipo `Dentist` con dirección, coordenadas, horario, rating, idiomas y `ReserveAction` |
| Mapa | Google Maps embebido con las coordenadas reales |
| Reveal / nav sticky | Animaciones en scroll y menú móvil |

## Datos del negocio (embebidos)

- **Nombre:** My Dentist Querétaro (VyDentist)
- **Lema:** Una razón para sonreír
- **Dirección:** Av. Constituyentes Pte. 7, Local 8B, Plaza Lecaroz, Centro, Querétaro, Qro.
- **Teléfono:** 442 384 1772 · **WhatsApp:** 442 197 5987
- **Horario:** Lun–Vie 9:00–20:00 · Sáb 9:00–14:00 · Dom cerrado
- **Coordenadas:** 20.5872464, -100.3849817
- **Facebook:** [/QROmydentist](https://www.facebook.com/QROmydentist/)

## Paleta de marca

| Variable | Valor | Uso |
|---|---|---|
| `--navy` | `#0B3A5B` | Azul marino de marca / texto |
| `--cyan` | `#25C4E0` | Cian de marca / acento |
| `--cyan-dk` | `#12A6C4` | Cian oscuro (hover/detalles) |
| `--ice` | `#F3FAFC` | Fondo secundario claro |
| — | `#25D366` | Verde WhatsApp |

## Cómo trabajar con esto

Abre cualquiera de los `vN.html` directamente en el navegador. No necesita servidor.

```bash
npx serve .        # o
python -m http.server 8000
```

## Pendientes del cliente

- [ ] Fotos reales (fachada, interior, equipo/doctor, casos antes/después) → `assets/images/`
      Nombres esperados: `hero.jpg`, `clinica.jpg`, `equipo.jpg`, `fachada.jpg` (ver placeholders en las webs).
- [ ] Confirmar dirección/horario exactos y años de experiencia reales.
- [ ] Logo en alta resolución / favicon definitivo → `assets/favicon/`.
- [ ] Confirmar rating y nº de reseñas reales (ahora 4.8★ / +120, ajustar).
- [ ] Conectar formularios a email si se quiere además de WhatsApp (Formspree/EmailJS).

## Deploy recomendado

1. Repo `business_webs`, rama `my_dentist_qro`.
2. Renombrar el `vN.html` elegido a `index.html` (o configurar el publish).
3. Conectar a Netlify/Vercel (Import from Git) → deploy automático en cada push.

**Dominio sugerido:** `mydentistqueretaro.com`

---

*Generado con Claude Code — homólogo a la web de la Heladería 900 (rama `heladeria900italiana`).*
