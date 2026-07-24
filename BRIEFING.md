# 🦷 My Dentist Querétaro — Project Briefing

> Briefing del proyecto para Claude Code. Léelo antes de tocar cualquier archivo.
> Este negocio vive en la rama `my_dentist_qro` del repo multi-negocio `business_webs`.

---

## 🏥 El negocio

**Nombre:** My Dentist (marca visible: **VyDentist**)
**Tipo:** Clínica / consultorio dental
**Dentista:** Dr. Ernesto (mencionado en varias reseñas de Google)
**Diferenciales reales:** membresía de prevención, imagen 3D + radiografías, se habla inglés
**Lema:** *Una razón para sonreír*
**Ubicación:** Av. Constituyentes Pte. 7, Local 8B, Plaza Lecaroz, Centro, Santiago de Querétaro, Qro.
**Coordenadas:** 20.5872464, -100.3849817
**Teléfono:** 442 384 1772  ·  **WhatsApp / cel:** 442 197 5987
**Horario:** Lunes a Viernes 9:00–20:00 · Sábado 9:00–14:00 · Domingo cerrado
**Facebook:** https://www.facebook.com/QROmydentist/  (@mydentist)
**Google Maps:** My Dentist Queretaro

### Identidad visual (de las fotos del local y el logo)
- Marca: diente estilizado en **azul marino** con un trazo/curva en **cian/turquesa** → "My/Vy Dentist".
- Interiores de la clínica con paredes turquesa; ambiente limpio y moderno.
- Por eso la paleta de todas las webs es **azul marino (#0B3A5B) + cian (#25C4E0)**: es literalmente el alma de la marca.

### Contexto
- Clínica en el Centro de Querétaro, cerca de la Alameda (Plaza Lecaroz).
- Querétaro tiene turismo dental: pacientes de EE. UU./extranjero → **el inglés importa** (i18n ES/EN).
- Competencia local: muchas clínicas "diseño de sonrisa" (DSD). Diferencial de My Dentist: **trato cercano, humano y sin juicios** + precios claros.

---

## 🎨 Dirección de diseño

Referencias que le gustan al cliente: **dentaloth.com.mx** (clínica premium: limpia, sofisticada,
mucha foto de calidad, tipografía cuidada, CTA de cita muy visible) y paoladentista.com.
El encargo: *"me gusta el estilo de dentaloth pero que tenga alma propia de My Dentist"*.

→ Traducción a diseño: estética **premium-clínica, confiable y luminosa**, con la **paleta navy+cian**
de My Dentist y el lema *Una razón para sonreír*. Nada de recrear la heladería: dentista de principio a fin.

Se entregan **3 variantes** (homólogo a las v1/v2/v3 de la heladería):

1. **v1 · Clínica Premium** — insignia. Fraunces (serif cálido) + Outfit. Hero a dos columnas,
   tarjetas de servicio con icono, franja de confianza, sección doctor en navy, proceso, testimonios,
   agenda + mapa + horario en vivo, FAQ, CTA. Es la más cercana a dentaloth.
2. **v2 · Moderno & Bold** — Poppins, cian dominante, formas redondeadas/blobs, stats grandes,
   pastillas flotantes. Amable y enérgico, ideal para redes.
3. **v3 · Editorial Minimal** — Cormorant Garamond + Manrope, mucho blanco, índice de servicios
   numerado, grandes citas serif, carrusel de testimonios. Sobrio y de autor.

Las tres comparten contenido, datos y features; cambian el lenguaje visual.

---

## 🧩 Servicios (contenido de las webs)

- **Ortodoncia** — brackets tradicionales, estéticos y alineadores invisibles.
- **Implantes dentales** — titanio, reposición de piezas perdidas.
- **Diseño de sonrisa** — carillas y coronas de porcelana, planificación digital.
- **Endodoncia** — tratamientos de conducto sin dolor.
- **Odontopediatría** — primeras visitas sin miedo para niños.
- **Limpieza y blanqueamiento** — higiene profesional y blanqueamiento.
- **Membresía de prevención** — plan de suscripción para revisiones/limpiezas constantes (muy valorado en reseñas).
- *(Base: odontología general / valoración · imagen 3D y radiografía digital)*

### Testimonios (reseñas reales de Google, ya en las 3 webs, ES/EN)
Shaddai · Dul · Diana · Armando · Margaret (EN).
Todas 5★. Traducidas al inglés en el selector ES/EN.

---

## 🛠️ Stack y funcionalidades

- **HTML/CSS/JS vanilla**, un archivo por variante (`v1.html`, `v2.html`, `v3.html`).
- **i18n ES/EN** propio (diccionario JS + `data-i18n`), con detección de navegador y `localStorage`.
- **Horario en vivo**: `new Date().getDay()/getHours()` → badge Abierto/Cerrado + día resaltado.
- **Formulario → WhatsApp**: arma el mensaje y abre `wa.me/524421975987`.
- **WhatsApp flotante** fijo.
- **Schema.org `Dentist` JSON-LD**: dirección, geo, `openingHoursSpecification`, `aggregateRating`,
  `availableLanguage`, `ReserveAction`.
- **SEO/AEO**: `<title>`/description por keyword, FAQ redactada como búsquedas reales
  ("¿mejor dentista en el Centro de Querétaro?", "Who is the best dentist in Querétaro?").
- **Mapa** de Google embebido con coordenadas reales.
- Reveal on scroll (IntersectionObserver), nav sticky, menú móvil.

### Paleta
```css
--navy:#0B3A5B  /* marca / texto */      --cyan:#25C4E0  /* acento */
--cyan-dk:#12A6C4                          --ice:#F3FAFC  /* fondo claro */
WhatsApp: #25D366
```

---

## 🖼️ Imágenes (pendiente del cliente)

Las webs funcionan con placeholders elegantes (degradados navy→cian + iconos SVG) donde irán las fotos.
Cuando el cliente las envíe, colocar en `assets/images/` con estos nombres para que aparezcan:

- `hero.jpg` — foto principal (sonrisa/paciente o fachada bonita).
- `clinica.jpg` — interior/gabinete.
- `equipo.jpg` — doctor/equipo.
- `fachada.jpg` — fachada del local (para OpenGraph / Schema).

*(Existe una foto de fachada con el rótulo VyDentist y el logo del diente; ideales para hero/equipo.)*

---

## 🚀 Deploy

1. Elegir variante → renombrarla a `index.html` (o configurar publish del `vN.html`).
2. Netlify/Vercel import from Git (rama `my_dentist_qro`) → deploy automático.
3. Dominio sugerido: `mydentistqueretaro.com`.

---

## ✅ TODO / pendientes del cliente

- [ ] Fotos reales (hero, clínica, equipo, fachada, antes/después).
- [ ] Confirmar dirección exacta, horario y años de experiencia.
- [ ] Rating y nº de reseñas reales (placeholder: 4.8★ / +120).
- [ ] Logo alta resolución / favicon definitivo.
- [ ] ¿Redes además de Facebook? (Instagram, TikTok).
- [ ] ¿Conectar formulario a email además de WhatsApp?

---

*Última actualización: 2026 — generado con Claude Code. Homólogo a la Heladería 900 (rama `heladeria900italiana`).*
