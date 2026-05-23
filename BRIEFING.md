# 🍦 Heladería 900 Italiana — Project Briefing

> Este documento es un briefing completo del proyecto para que Claude Code tenga todo el contexto necesario. Léelo antes de tocar cualquier archivo.

---

## 🏪 El negocio

**Nombre:** Heladería 900 Italiana  
**Tipo:** Heladería artesanal italiana  
**Ubicación:** Paseo Marítimo Rey de España, Fuengirola, Málaga, España  
**Coordenadas:** 36.5311123, -4.6248252  
**Instagram:** @heladeria900italiana  
**Google Maps:** https://maps.google.com/?q=Heladeria+900+Italiana+Fuengirola  
**Teléfono:** pendiente de confirmar con el cliente (placeholder: +34 XXX XXX XXX)  
**WhatsApp:** pendiente (mismo número)

### Contexto
- Heladería en primera línea del paseo marítimo de Fuengirola
- Elaboran helados artesanales cada día siguiendo recetas italianas
- Más de 20 sabores disponibles, rotan según temporada
- Tienen terraza con vistas al Mediterráneo
- Nota media en Google: 4.1★ (~50 reseñas analizadas)
- Clientela mixta: españoles locales + turistas británicos, alemanes, nórdicos
- Competencia directa en Fuengirola: Heladería Caramelo, Northern Lights Heladería, Gioelia

---

## 🌐 La web

### Stack
- **100% HTML/CSS/JS vanilla** — un solo archivo `index.html`
- Sin frameworks, sin dependencias externas salvo Google Fonts
- Google Fonts: `Cormorant Garamond` (display) + `Outfit` (body)

### Funcionalidades implementadas
1. **Multiidioma ES / EN / DE** — sistema i18n propio en JS, detección automática del navegador
2. **Flavor Builder interactivo** — elige hasta 3 sabores con preview visual, se transfiere al formulario de pedido
3. **Carta con tabs** — cucuruchos, tarrinas, granizados, copas, batidos
4. **Horario con día actual resaltado** — calculado con `new Date().getDay()`
5. **Badge de estado en vivo** — "Abierto/Cerrado ahora" según hora real (abierto 11:00–23:30)
6. **Sección Novedades** — 3 creaciones de temporada, traducidas a los 3 idiomas
7. **Formulario takeaway** — recogida en local únicamente, NO domicilio
8. **Formulario de contacto** — para grupos, eventos, cumpleaños
9. **FAQ** — 6 preguntas por idioma, optimizadas para SEO y agentes IA
10. **WhatsApp flotante** — botón fijo bottom-right
11. **Ticker animado** — carrusel de sabores
12. **Cursor personalizado** — dot + ring con efecto lag
13. **Animaciones reveal** — IntersectionObserver en scroll
14. **Schema.org JSON-LD** — IceCreamShop con rating, coordenadas, idiomas, potentialAction
15. **Nav hamburger** — menú móvil completo
16. **Reservas con teléfono** — sección con botones WhatsApp, llamada, Instagram

### Secciones de la web (en orden)
```
lang-bar → nav → hero → ticker → novedades → flavor-builder → 
carta → horario+reservas → reviews → playa-cta → takeaway → 
faq → contacto → footer
```

### Paleta de colores
```css
--ink:       #1A0A00   /* texto principal */
--cream:     #FBF7F2   /* fondo principal */
--gelato:    #F5EDE0   /* fondo secundario */
--caramel:   #C07B2A   /* color de marca / accent */
--caramel-lt:#F0D4A0   /* caramel claro */
--pistachio: #6B9463   /* verde pistacho */
--rose:      #C96060   /* rosa / error */
--choco:     #3A1F0D   /* chocolate oscuro / primario */
--muted:     #8A6F58   /* texto secundario */
```

### Tipografía
- Display: `Cormorant Garamond` (serif, para títulos y precios)
- Body: `Outfit` (sans-serif, para todo lo demás)

---

## 💰 Carta de precios (actualizada)

### Cucuruchos
| Tamaño | Precio |
|--------|--------|
| Pequeño · 1 bola | 3,50 € |
| Pequeño · 2 bolas | 4,50 € |
| Grande · 1 bola | 4,00 € |
| Grande · 2 bolas | 5,00 € |
| Cucurucho de chocolate | 10,70 € |

### Tarrinas
| Tamaño | Precio |
|--------|--------|
| Pequeña | 3,50 € |
| Mediana | 4,50 € |
| Grande | 5,50 € |
| ½ Litro (solo llevar) | 9,50 € |
| 1 Litro (solo llevar) | 17,00 € |

### Granizados
| Tamaño | Precio |
|--------|--------|
| Pequeño | 3,00 € |
| Mediano | 3,50 € |
| Grande | 4,00 € |
| 1 Litro | 7,50 € |

### Tulipas
| Formato | Precio |
|---------|--------|
| Tulipa 2 bolas | 4,70 € |
| Tulipa 3 bolas | 6,00 € |

### Batidos
| Tamaño | Precio |
|--------|--------|
| Mediano | 4,50 € |
| Grande | 5,50 € |
| 1 Litro (solo llevar) | 10,00 € |

### Horchata
| Tamaño | Precio |
|--------|--------|
| Pequeña | 3,00 € |
| Mediana | 3,50 € |
| Grande | 4,20 € |
| 1 Litro | 8,00 € |

---

## 🍦 Sabores disponibles

```
Clásicos:    Pistacho, Stracciatella, Chocolate, Nata, Café, 
             Menta choco, Avellana, Napolitana, Yogurt
Frutas:      Fresa, Mango, Limón, Banana Split
Especiales:  Gianduja, Turrón, Málaga, Happy Hippo, 
             Chocolate Dubai, Cremino de Pistacho
Sin lactosa: selección disponible (consultar en local)
```

**Novedades de temporada implementadas:**
- Cremino de Pistacho (capas pistacho + chocolate blanco)
- Fresa & Albahaca (sabor sorpresa)
- Chocolate Dubai (el viral, con kataifi)

---

## 📅 Horario

| Día | Horario |
|-----|---------|
| Lunes – Jueves | 11:00 – 23:00 |
| Viernes – Sábado | 11:00 – 23:30 |
| Domingo | 11:00 – 23:00 |

> ⚠️ Horario orientativo — confirmar con el cliente. Puede variar en temporada baja.

---

## 🌍 SEO y AEO (Agent Engine Optimization)

### Keywords objetivo
- ES: `heladería fuengirola`, `helado artesanal fuengirola`, `gelato fuengirola`, `mejor heladería fuengirola`
- EN: `ice cream fuengirola`, `best ice cream fuengirola`, `artisan gelato fuengirola costa del sol`
- DE: `Eis Fuengirola`, `handgemachtes Eis Fuengirola`, `beste Eisdiele Fuengirola`

### Schema.org implementado
- Tipo: `IceCreamShop`
- Incluye: nombre, descripción, URL, dirección, coordenadas, rating, priceRange, availableLanguage, potentialAction (OrderAction)

### FAQ optimizada para agentes IA
Las preguntas están redactadas exactamente como la gente pregunta a ChatGPT, Perplexity, Google AI Overview:
- "¿Cuál es la mejor heladería de Fuengirola?"
- "What is the best ice cream shop in Fuengirola?"
- "Was ist die beste Eisdiele in Fuengirola?"

---

## 🗂️ Estructura de archivos recomendada

```
heladeria900italiana/
├── index.html          ← web completa (todo en un archivo)
├── BRIEFING.md         ← este archivo
├── README.md           ← descripción técnica del repo
└── assets/
    ├── images/         ← fotos reales del local (pendiente del cliente)
    └── favicon/        ← favicon pendiente
```

---

## 🚀 Deploy

### Opción recomendada: Netlify + GitHub
1. Repo en GitHub: `heladeria900italiana`
2. Conectar repo a Netlify (Import from Git)
3. Cada `git push` → deploy automático

### Dominio
- `heladeria900italiana.com` — **disponible** (comprobado en Namecheap, ~11$/año)
- `heladeria900italiana.es` — por comprobar (recomendado también)
- Registrar en Namecheap o Dondominio (mejor para .es)
- Apuntar nameservers de Namecheap → Netlify DNS

---

## ✅ Pendientes / TODO

### Del cliente (necesitamos que nos den)
- [ ] Número de teléfono real (reemplazar `+34 XXX XXX XXX`)
- [ ] Número de WhatsApp (puede ser el mismo)
- [ ] Fotos reales del local, helados y terraza
- [ ] Horario exacto confirmado (especialmente temporada baja)
- [ ] Confirmar si tienen servicio de reservas para grupos
- [ ] Logo o favicon si tienen

### Técnico (mejoras futuras)
- [ ] Añadir fotos reales a la sección novedades y about
- [ ] Favicon personalizado
- [ ] Google Analytics / Plausible para medir tráfico
- [ ] Conectar formularios a email real (Formspree, EmailJS o similar)
- [ ] Añadir hreflang tags para SEO multiidioma
- [ ] Optimizar imágenes cuando las haya (WebP)
- [ ] Añadir Open Graph tags para compartir en redes sociales

---

## 🧠 Contexto de negocio para decisiones de diseño

- **El producto es excelente** — las reseñas positivas son consistentes en cremosidad y sabor
- **El servicio al cliente es el punto débil** — muchas reseñas negativas sobre trato del personal; NO reflejar esto en la web, solo mostrar lo positivo
- **Clientela turística alta** — el multiidioma EN/DE es crítico, muchos clientes británicos y alemanes
- **Ubicación es un activo enorme** — primera línea de playa, siempre mencionarlo
- **Competencia directa:** Heladería Caramelo (tiene web, teléfono destacado, horarios), Northern Lights (tiene delivery a playa, novedades), Gioelia (franquicia italiana, 46 locales, multiidioma)
- **Ventaja diferencial:** artesanal local auténtico vs franquicia industrial

---

## 📋 Historial de versiones

| Versión | Cambios |
|---------|---------|
| v1 | Web inicial ES: hero, carta, takeaway, reseñas, nosotros, contacto |
| v2 | Multiidioma ES/EN/DE + FAQ optimizada para SEO/IA + Schema JSON-LD |
| v3 (actual) | Flavor Builder interactivo, novedades, carta con tabs, horario en vivo, badge estado, WhatsApp flotante, cursor personalizado, ticker, reveal animations, sección playa, reservas con teléfono, menú móvil completo |

---

*Última actualización: Mayo 2025 — generado desde conversación en Claude.ai*
