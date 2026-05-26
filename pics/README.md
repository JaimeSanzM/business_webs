# Heladería 900 Italiana — Web

Web oficial de la Heladería 900 Italiana, ubicada en el Paseo Marítimo Rey de España, Fuengirola, Málaga.

## Stack

- **100% HTML/CSS/JS vanilla** — un único archivo `v1.html`, sin frameworks ni dependencias de build
- Google Fonts: `Cormorant Garamond` (display) + `Outfit` (body)
- Sin npm, sin bundler, sin dependencias externas salvo fonts

## Funcionalidades

| Feature | Descripción |
|---|---|
| Multiidioma ES/EN/DE | Sistema i18n propio en JS, detección automática de idioma del navegador |
| Flavor Builder | Elige hasta 3 sabores con preview visual; transfiere al formulario de pedido |
| Carta con tabs | Cucuruchos, tarrinas, granizados, copas, batidos, horchata |
| Horario en vivo | Día actual resaltado calculado con `new Date().getDay()` |
| Badge estado | "Abierto/Cerrado ahora" según hora real (11:00–23:30) |
| Novedades | 3 creaciones de temporada, traducidas a los 3 idiomas |
| Formulario takeaway | Recogida en local, sin domicilio |
| Formulario contacto | Para grupos, eventos y cumpleaños |
| FAQ SEO/AEO | 6 preguntas por idioma optimizadas para buscadores y agentes IA |
| WhatsApp flotante | Botón fijo bottom-right |
| Ticker animado | Carrusel de sabores |
| Cursor personalizado | Dot + ring con efecto lag |
| Reveal animations | IntersectionObserver en scroll |
| Schema.org JSON-LD | Tipo `IceCreamShop` con rating, coordenadas, idiomas, `potentialAction` |
| Nav hamburger | Menú móvil completo |

## Estructura

```
heladeria900italiana/
├── v1.html             ← web completa (todo en un archivo)
├── BRIEFING.md         ← briefing del proyecto para Claude Code
├── README.md           ← este archivo
└── assets/
    ├── images/         ← fotos reales del local (pendiente del cliente)
    └── favicon/        ← favicon (pendiente del cliente)
```

## Cómo trabajar con esto

Abre `v1.html` directamente en el navegador. No necesita servidor local.

Para un servidor rápido con live-reload:

```bash
npx serve .
# o
python -m http.server 8000
```

## Paleta de colores

| Variable | Valor | Uso |
|---|---|---|
| `--ink` | `#1A0A00` | Texto principal |
| `--cream` | `#FBF7F2` | Fondo principal |
| `--gelato` | `#F5EDE0` | Fondo secundario |
| `--caramel` | `#C07B2A` | Color de marca / accent |
| `--caramel-lt` | `#F0D4A0` | Caramel claro |
| `--pistachio` | `#6B9463` | Verde pistacho |
| `--rose` | `#C96060` | Rosa / error |
| `--choco` | `#3A1F0D` | Chocolate oscuro / primario |
| `--muted` | `#8A6F58` | Texto secundario |

## SEO / AEO

- Schema.org `IceCreamShop` con coordenadas, rating, `potentialAction: OrderAction`
- FAQ redactada como la gente pregunta a ChatGPT/Perplexity/Google AI Overview
- Titles dinámicos por idioma optimizados por keyword
- Keywords: `heladería fuengirola`, `ice cream fuengirola`, `Eis Fuengirola`

## Deploy recomendado

1. Repo en GitHub: `heladeria900italiana`
2. Conectar a [Netlify](https://netlify.com) (Import from Git)
3. Cada `git push` → deploy automático

**Dominio sugerido:** `heladeria900italiana.com` (disponible en Namecheap ~11$/año)

## Pendientes del cliente

- [ ] Número de teléfono real (reemplazar `+34 XXX XXX XXX`)
- [ ] Número de WhatsApp
- [ ] Fotos reales del local, helados y terraza → `assets/images/`
- [ ] Horario exacto confirmado (especialmente temporada baja)
- [ ] Logo / favicon → `assets/favicon/`
- [ ] Confirmar si tienen reservas para grupos

## Versiones

| Versión | Cambios |
|---|---|
| v1 | Web inicial ES: hero, carta, takeaway, reseñas, nosotros, contacto |
| v2 | Multiidioma ES/EN/DE + FAQ SEO/IA + Schema JSON-LD |
| v3 (actual) | Flavor Builder, novedades, carta tabs, horario en vivo, badge estado, WhatsApp flotante, cursor personalizado, ticker, reveal animations, sección playa, reservas, menú móvil |

---

*Proyecto generado desde conversación en Claude.ai — Mayo 2025*
