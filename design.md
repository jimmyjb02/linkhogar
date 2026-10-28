# LinkHogar — Sistema visual de @linkhogar.rd

> Referencia de diseño para todo lo que se publica en Instagram y TikTok.
> Levantado el 27 de octubre de 2026 a partir del perfil real y de las piezas
> guardadas en esta carpeta.

Este archivo describe **cómo se ve LinkHogar**, no qué se dice. La voz, los
formatos de copy y el procedimiento de render viven en
`Skills/post-linkhogar/SKILL.md`. Si algo se contradice, manda este archivo
para lo visual y la skill para lo editorial.

---

## 1. Lectura del perfil

**Estado al 27/10/2026:** 1,674 seguidores · 26 seguidos · nombre "LinkHogar
Solutions" · enlace a `wa.me/18094601290`.

Bio publicada:

```
LinkHogar Solutions
Diseño, instalación y configuración de casas inteligentes
🏠 Hogar inteligente a tu medida
💡 Domótica · Automatización · S… (truncada en la vista pública)
wa.me/18094601290
```

**Foto de perfil:** logo a color centrado sobre círculo blanco. Correcto — el
logo nunca va sobre navy en el avatar porque el degradado azul-verde pierde
contraste.

**Historias destacadas (6):** Servicios · Automatización · Iluminación ·
Sensores · Cerraduras · Energía. Portadas uniformes: círculo navy con halo
celeste y un ícono de línea blanco centrado. Es el elemento más consistente
del perfil; cualquier destacado nuevo se hace igual.

### Qué muestra la cuadrícula

La parrilla alterna tres cosas, y ese ritmo es deliberado:

| Tipo | Peso en la cuadrícula | Para qué sirve |
|---|---|---|
| Foto real de proyecto / instalación | ~40 % | Prueba de que instalamos, no solo vendemos |
| Portada de reel con titular condensado sobre foto | ~35 % | Gancho; es lo que para el scroll |
| Carrusel educativo (portada blanca + ícono navy) | ~25 % | Autoridad técnica; es lo que se guarda |

Las portadas de reel usan el mismo recurso siempre: **foto propia + titular en
condensada MAYÚSCULAS, blanco, sangrado al borde** (`DOMÓTICA`, `PANEL`,
`INTELIGENTE`, `TOMA CORRIENTES`, `CEREBRO de tu casa`). Esa sangría —la
palabra cortada por el canto del cuadro— es parte de la firma y conviene
mantenerla.

Los carruseles nuevos entran a la cuadrícula como **cuadros casi blancos**.
Eso es una ventaja: rompen el bloque oscuro de las fotos y hacen legible la
parrilla de tres en tres. Al programar, evita publicar dos carruseles seguidos
(quedan dos huecos blancos pegados en la misma fila).

### Diagnóstico — lo que hay que corregir

1. **Conviven tres generaciones de diseño.** El navy actual `#0d2436`, el
   navy viejo `#2E3C44` (carrusel de Zigbee) y el degradado azul claro de las
   piezas de servicios/comunicado. Solo la primera es la vigente.
2. **Quedan rastros de "intelihogar"** en publicaciones antiguas visibles en
   la cuadrícula. No se borran, pero nada nuevo lo usa.
3. **El rojo del carrusel de Zigbee no es de la marca** — venía del logo de
   Zigbee y se extendió a los resaltados del texto. No se repite.
4. **Oswald no siempre cargó.** En el carrusel de Wi-Fi el chip de portada y
   la línea de apoyo salieron en DM Sans en vez de la condensada. Revisar
   siempre que las fuentes estén junto al HTML antes de renderizar.

---

## 2. Tokens

### Color

| Rol | Hex | Uso |
|---|---|---|
| Navy profundo | `#0d2436` | Fondo de tarjeta, chips, titulares sobre claro, nodo central de diagramas |
| Navy secundario | `#163a55` | Degradados y bloques de apoyo. Nunca como fondo principal |
| Verde logo | `#5cc59a` | Acento positivo: ventajas, confirmaciones, resaltados sobre navy |
| Azul logo | `#3aa8de` | Acento neutro: datos, líneas de diagrama, resaltados sobre navy |
| Azul profundo | `#3b6fb6` | Resaltados sobre fondo blanco |
| Banda clara | `#f1f2f4` | Banda de portada, tarjetas secundarias |
| Blanco | `#ffffff` | Lienzo, tarjetas de diagrama |
| Texto sobre claro | `#18181b` · `#52525b` | Cuerpo y secundario |
| Texto sobre navy | `#ffffff` · `#e9eef2` | Titular y cuerpo |

Reglas:

- **Máximo dos acentos por carrusel.** Verde para lo que suma, azul para lo
  que explica. No se mezclan los tres.
- Los resaltados marcan **2–4 términos**, nunca frases completas ni una
  oración entera.
- Rojo, naranja y amarillo no existen en la paleta. Única excepción: el
  logotipo de una marca ajena conserva su color, y aun así es mejor sustituir
  el logotipo por un ícono propio en navy cuando la marca es solo un concepto
  (Wi-Fi, Bluetooth).
- Los degradados azul claro de las piezas de 2025 están retirados.

### Tipografía

| Rol | Fuente | Especificación |
|---|---|---|
| Titular | Oswald Bold 700 | MAYÚSCULAS, 104 px (88 px si son dos líneas), line-height 0.95, letter-spacing −0.5 px |
| Chip de portada | Oswald Bold | MAYÚSCULAS, 44 px, sobre pastilla navy radio 14 px, padding 18/40 px |
| Cuerpo | DM Sans Regular | 32 px, line-height 1.5, justificado |
| Lista | DM Sans | 31 px, line-height 1.45; el término en 700 blanco, el resto en `#e9eef2` |
| Línea de apoyo de portada | DM Sans | 34 px, centrada, navy |
| Etiquetas de diagrama | DM Sans 600 | 24 px, navy |

Nunca más de dos familias por pieza. Oswald es la firma: si un titular sale en
DM Sans, la pieza está mal renderizada.

**Tildes en mayúsculas, siempre:** ¿CÓMO FUNCIONA?, LÍMITES, DOMÓTICA.

### Medidas

| Elemento | Valor |
|---|---|
| Lienzo carrusel y feed | 1080 × 1350 |
| Lienzo reel, TikTok e historia | 1080 × 1920 |
| Margen de la tarjeta | 40 px laterales e inferior, 122 px superior |
| Padding interno de tarjeta | 54 px arriba/abajo, 52 px laterales |
| Radio de tarjeta navy | 36 px |
| Radio de tarjeta de diagrama | 26 px |
| Radio de foto embebida | 24 px (alto 430 px, `object-fit: cover`) |
| Barra superior | top 44 px, laterales 48 px, alto 52 px |
| Logo | 46 px de alto, arriba a la izquierda, idéntico en toda la serie |
| Sombras | Ninguna. La jerarquía es por color y aire |

---

## 3. Anatomía por formato

### Carrusel educativo — el formato insignia

5 a 8 slides, 1080 × 1350.

| Slide | Composición |
|---|---|
| 1 — Portada | Fondo blanco. Banda `#f1f2f4` de 600 px de alto desde y=360. Ícono navy grande (~470 px) centrado en la banda. Chip navy con el nombre de la serie montado sobre el borde superior de la banda. Línea de apoyo debajo, máximo 7 palabras |
| 2 — Definición | Tarjeta navy. Titular + 2 párrafos cortos |
| 3…N−2 — Desarrollo | Tarjeta navy. Un concepto por slide. Diagrama cuando el concepto sea espacial o de red |
| N−1 — Aterrizaje | Tarjeta navy con foto propia del proyecto. Es el slide que convierte |
| N — Cierre | Fondo navy con arco blanco: círculo de 1505 px en `left:-565px; top:-77px`. Logo de 470 px y tagline centrados en la zona blanca. Marcador de guardado blanco abajo a la derecha |

**Indicador de avance**, arriba a la derecha, pastilla de borde navy 2.5 px,
radio 999 px, alto 46 px:

- Slide 1: texto "Desliza →"
- Slides 2 a N−1: un punto navy de 17 px por slide recorrido
- Slide final: flecha "←", pastilla en borde blanco sobre el navy

**Aire.** Una tarjeta que termina a media altura está bien. Máximo ~45
palabras de cuerpo por slide: si no cabe, se recorta el tema, no la letra.

### Diagramas

Tarjeta blanca radio 26 px dentro de la tarjeta navy. Líneas punteadas
`#3aa8de` (stroke 3, dash 9/9). Nodos: círculos blancos con borde azul de
3.5 px, **radio mínimo 70 px** para que la etiqueta quepa dentro. Nodo central
navy sólido, radio 86 px, texto en Oswald blanco.

Antes de entregar: abrir el PNG y verificar que ninguna etiqueta se salga de
su círculo.

### Portada de reel / TikTok

1080 × 1920. Foto propia a sangre. Titular en condensada MAYÚSCULAS blanca,
alineado a un borde y **cortado por el canto del cuadro**. Sin logo en el
primer fotograma: el logo roba los primeros tres segundos, que son del gancho.
Texto en pantalla corto y legible sin audio.

### Antes / después

Foto real en ambos estados, mismo encuadre y, en lo posible, misma luz. Nunca
nombre completo del cliente ni dirección: "un apartamento en Naco" basta.

### Post único y comunicado

Una sola pieza, mensaje único, mucho aire. Encabezado con el logo sobre banda
clara, cuerpo en DM Sans justificado, firma "El equipo de LinkHogar". Formal
pero humano. El degradado azul del comunicado de 2025 se sustituye por navy
plano o blanco.

---

## 4. Fotografía

- Fotos propias de proyectos entregados siempre que existan. Hay material en
  `web/assets/img/proyectos/`.
- Interiores reales y ordenados; luz natural cuando se pueda.
- Nunca fotos de producto con marca de agua del proveedor ni renders de
  catálogo presentados como trabajo nuestro.
- El uniforme con el logo en la espalda es un activo: las fotos del equipo
  instalando son las que más prueban el modelo de negocio.

---

## 5. Uso del logo

- Versión a color sobre fondo blanco o claro. Sobre navy, el logo completo
  funciona porque "hogar" se invierte a blanco en el archivo de cierre.
- Alto fijo de 46 px en la barra superior; 470 px en el slide de cierre.
- En texto corrido la marca se escribe **LinkHogar**. En minúsculas
  (`linkhogar`) solo como imagen del logotipo.
- **"intelihogar" es el nombre viejo. No se usa en nada nuevo.**
- El archivo `Logos/Logo LinkHogar transparente.png` tiene fondo blanco opaco
  pese al nombre: recortarlo al contenido y volver transparente el blanco
  antes de usarlo.

---

## 6. Antes de publicar

- [ ] Navy `#0d2436`, no `#2E3C44` ni `#0E3A52`
- [ ] Titulares en Oswald, no en DM Sans
- [ ] Tildes en las mayúsculas
- [ ] Máximo dos colores de acento; nada de rojo
- [ ] Logo a 46 px, mismo lugar en todos los slides
- [ ] Indicador de avance correcto en cada slide
- [ ] Ningún texto desbordado ni etiqueta fuera de su círculo
- [ ] Sin dobles espacios
- [ ] Erratas ya publicadas que no se repiten: profesional, sin necesidad,
      inusual, automática, energía
- [ ] Ninguna afirmación técnica sin verificar: modelos, precios,
      compatibilidades y disponibilidad se confirman o se omiten
- [ ] La pieza no queda pegada en la cuadrícula a otra del mismo tipo

---

## 7. Archivos de referencia

| Ruta | Qué es |
|---|---|
| `Skills/post-linkhogar/SKILL.md` | Voz, formatos de copy y procedimiento de render |
| `Skills/post-linkhogar/plantilla/carrusel.html` | Implementación exacta de estos tokens |
| `Post/LinkHogar - Post WiFi/` | Referencia de estilo vigente |
| `Post/LinkHogar - Post Zigbee/` | Estructura correcta, color deprecado |
| `Logos/` | Logo a color, transparente y QR |
| `web/assets/css/styles.css` | Tokens de marca en la web |
| `web/assets/img/proyectos/` | Fotos propias de proyectos |

Nota: el `DESIGN.md` de la raíz de `LinkHogar/` **no es de esta marca** — es
una referencia de estilo de un tercero (Awesomic) guardada ahí por error. El
sistema visual de LinkHogar es este archivo.
