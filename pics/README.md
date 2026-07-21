# pics/ — Material de origen (My Dentist Querétaro)

Carpeta para las **fotos y materiales originales** que envíe el cliente
(sin procesar): fachada, interior, equipo, casos antes/después, logo en alta.

## Cómo usarlas en las webs

Las 3 webs (`v1.html`, `v2.html`, `v3.html`) muestran *placeholders* con degradado
navy→cian donde irán las fotos. Para que aparezcan las reales, exporta/optimiza
(preferible **WebP o JPG** ~1600px) y colócalas en `assets/images/` con estos nombres:

| Nombre en `assets/images/` | Qué foto va aquí |
|---|---|
| `hero.jpg` | Imagen principal: paciente sonriendo, gabinete bonito o fachada. |
| `clinica.jpg` | Interior / sala de espera / unidad dental. |
| `equipo.jpg` | Doctor(a) o equipo. |
| `fachada.jpg` | Fachada con rótulo VyDentist (para OpenGraph y Schema). |

Después, en la web elegida, sustituye el bloque `.ph-label` / `.ph` correspondiente
por un `<img src="assets/images/hero.jpg" alt="...">` (o úsalo como `background-image`).

## Fotos ya disponibles (del cliente)

- Fachada con rótulo **VyDentist** + logo del diente y datos de contacto.
- Unidad/silla dental (gabinete azul).
- Sala de espera con dispensador y sofá.
- Doctor trabajando con lupas.
- Logo del diente "My/Vy Dentist".

> Coloca estos archivos aquí en `pics/` cuando los tengas y expórtalos a `assets/images/`.

## Marca

- Azul marino `#0B3A5B` + cian/turquesa `#25C4E0`.
- Lema: **Una razón para sonreír**.
- Logo/favicon vectorial ya incluidos en `assets/brand/logo.svg` y `assets/favicon/favicon.svg`.
