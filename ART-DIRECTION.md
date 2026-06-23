# AllImport — Dirección de Arte Fotográfica

> Documento de dirección visual para recrear las 11 imágenes de producto en Higgsfield.
> **Tipografía y fuentes del sitio: SIN CAMBIOS.** Este documento cubre exclusivamente fotografía y dirección de arte.
> Formato de salida: **4:5 vertical, 1024 × 1280 px** (reemplaza el actual 896×1152; mismo encuadre de las cards `aspect-ratio:4/5`).

---

## 1. Diagnóstico de las imágenes actuales

Todas comparten un **degradado gris carbón radial** con viñeta — el tell #1 de "marketplace generado por IA". No es un fondo real: es un gradiente. Eso, sumado a packaging de reventa y productos flotando sin sombra de contacto, baja la percepción de marca.

| # | Producto | Problemas detectados |
|---|----------|----------------------|
| 01 | Camiseta Argentina | Fondo degradado genérico · prenda flotando plana, sin volumen real · sombra de contacto ausente · composición centrada-frontal sin intención |
| 02 | Messi #10 | Mismo degradado pero **balance de blancos más cálido** que 01/03 → set inconsistente · flota · plano |
| 03 | Argentina 3★ | Fondo **más claro y luz más pareja** que 01/02 → tres remeras, tres iluminaciones distintas |
| 04 | Pack Apple (4 cajas) | **Grid de 4 cajas tipo bundle de reventa** · sombras débiles · sensación catálogo importador · muestra cajas, no producto |
| 05 | Cable + Cargador | **Cajas retail con blister/hang-tab visible** = tell de reventa · muestra el packaging, no el producto |
| 06 | Kit iPhone 16 | Mismas cajas con hang-tab · texto de packaging dominando · marketplace |
| 07 | JBL Go 2 | **El peor iluminado**: producto negro sobre fondo casi negro, se funde y pierde forma · sin separación · turbio |
| 08 | AirPods Pro 2 (caja) | El mejor del set (es el hero/OG) · aún así fondo degradado genérico · muestra caja, no producto |
| 09 | MagSafe Battery | Caja retail con **hang-tab** · centrada · plana |
| 10 | Elf Bar | **Caja retail con etiqueta "WARNING: nicotine" a la vista** · packaging chillón · sensación kiosko/marketplace total |
| 11 | AirPods Pro 2 (estuche abierto) | Bien que muestra **producto real** y no caja · pero flota, sombra débil, fondo genérico |

**Patrones transversales a corregir:**
1. Fondo degradado falso → reemplazar por **superficie/entorno real**.
2. Temperatura de color a la deriva → **un solo balance de blancos** en todo el set.
3. **Packaging de reventa con hang-tab** (05, 06, 09) → mostrar **producto**, no la caja.
4. Packaging chillón (10) y grid de cajas (04) → **producto limpio**, no envoltorio.
5. Productos flotando → **sombra de contacto real** que ancle cada pieza.
6. Composición siempre centrada-frontal → **ritmo de aire negativo + variación de ángulo**.

---

## 2. El sistema visual — "AllImport Studio"

Fusión deliberada de las cuatro referencias:
- **Apple** → claridad, aire negativo, sombra honesta, producto protagonista.
- **Aesop** → calidez del neutro, materialidad, calma.
- **Nothing** → precisión, sin props, sin trucos de gradiente, una sola sombra.
- **Sonos** → superficie tonal con textura sutil, luz envolvente suave.

### 2.1 Fondo
- **Superficie seamless bone/hueso cálido**: de `#EFEDE8` (zona de luz) a `#D8D4CC` (caída), **infinity cove** (la pared funde con el piso sin línea de horizonte dura).
- Textura **micro-mate tipo yeso/concreto pulido suave** — perceptible pero nunca ruidosa. **Nunca un degradado plano de Photoshop.**
- Cero props, cero superficies reflectantes tipo espejo, cero viñeta artificial.

> Excepción coherente: para piezas que pidan drama (audio negro), se permite la variante **"graphite"** — superficie piedra gris oscuro `#1C1C1E→#0E0E10`, mismo esquema de luz. Usar solo donde se indica abajo, para que el set no quede partido.

### 2.2 Iluminación
- **Una key grande y suave** (softbox/octa grande) desde **arriba-izquierda ~45°**, difusión alta → transición de sombra larga y limpia.
- **Fill mínimo** desde la derecha (rebote blanco) solo para que la sombra no empaste; ratio key:fill ≈ **3:1**.
- **Sin destellos especulares duros**; en productos brillantes (cajas blancas, estuche AirPods) un **único gradiente especular suave**, no múltiples reflejos.
- Misma temperatura en todo el set: **5200K neutro-cálido**.

### 2.3 Composición y encuadre
- **Aire negativo generoso**: el producto ocupa **55–65% de la altura**, **levemente sobre el centro óptico** (centro geométrico desplazado ~8% hacia arriba).
- **Margen de respeto** uniforme: nunca tocar bordes; mínimo 12% de aire a cada lado.
- Tech pequeño (cargadores, parlante, estuche): **ángulo 3/4 a la altura del ojo con leve picado 10–15°** → da volumen y "peso".
- Cajas selladas (cuando se muestren): **3/4 a 35°**, una sola caja protagonista (no grids).
- Indumentaria: **ghost-mannequin dimensional** (volumen de cuerpo invisible), 3/4 leve, con caída y arrugas naturales — no plancha plana.

### 2.4 Sombras
- **Sombra de contacto real y anclada** bajo cada producto: suave, direccional (cae hacia abajo-derecha por la key), con **degradé natural** (más densa en el punto de apoyo).
- Densidad media — **nunca producto flotando**, nunca sombra dura recortada tipo sticker.

### 2.5 Escala de producto (consistencia entre cards)
Para que el catálogo se vea como un set y no como piezas sueltas, normalizar el "peso visual":
- **Indumentaria**: llena ~70% de altura.
- **Cajas/estuches medianos** (AirPods, MagSafe, JBL): ~50% de altura, centrados con aire.
- **Accesorios chicos** (cable, cargador): ~45%, agrupación mínima y ordenada.
- Mantener **misma distancia de cámara aparente** → coherencia de escala percibida.

---

## 3. Prompts optimizados por producto (Higgsfield)

> Estructura: **[sujeto exacto] + [encuadre/ángulo] + [fondo del sistema] + [luz del sistema] + [sombra] + [render specs]**.
> Aplicar a TODOS el mismo **negative prompt base** (abajo) y **4:5 / 1024×1280**.
> Recomendado: modelo foto-realista de alta fidelidad de Higgsfield (consultá `models_explore` con "premium product photography"); usar `generate_image`.

**NEGATIVE PROMPT base (para todos):**
```
gradient backdrop, dark vignette, floating product, no shadow, harsh shadow,
sticker cutout, retail blister, hang tab, warning labels, busy background,
props, clutter, multiple harsh reflections, oversaturated, plastic CGI look,
text artifacts, watermark, low resolution, marketplace catalog look
```

**STYLE SUFFIX base (para todos):**
```
premium product photography, Apple x Aesop x Sonos art direction, warm bone
seamless infinity cove (#EFEDE8 to #D8D4CC), soft micro-matte plaster texture,
single large soft key light top-left 45°, gentle 3:1 fill, realistic grounded
contact shadow falling lower-right, generous negative space, 5200K neutral-warm
white balance, shot on Phase One, 100mm macro, f8, ultra sharp, photorealistic,
8k, editorial catalogue
```

---

### 01 · Camiseta Argentina Campeón
```
Argentina national football jersey, white and sky-blue vertical stripes, Adidas
+ AFA crest, 3 stars, shown on an invisible ghost-mannequin with full body
volume and natural fabric folds, 3/4 front angle, centered with generous
headroom, fabric filling ~70% of frame height
```
+ STYLE SUFFIX + NEGATIVE.

### 02 · Messi #10
```
Argentina football jersey with "MESSI 10" print on the back, white and sky-blue
stripes, ghost-mannequin showing the BACK at a slight 3/4 turn, natural drape
and shoulder volume, dimensional not flat
```
+ STYLE SUFFIX + NEGATIVE.

### 03 · Argentina · 3 Estrellas
```
Argentina champion jersey, embroidered 3 stars and golden details, ghost-
mannequin front view slight 3/4, crisp fabric texture, identical lighting and
bone backdrop to the other two jerseys for a matched set
```
+ STYLE SUFFIX + NEGATIVE.

### 04 · Pack Accesorios Apple  *(cambiar de "grid de cajas" a producto agrupado)*
```
Apple accessories hero arrangement: AirPods Pro 2, white MagSafe battery pack,
USB-C to Lightning cable softly coiled, and a 20W charger — the actual PRODUCTS
(not retail boxes), arranged as a clean diagonal still-life with even spacing,
3/4 elevated angle, each item with its own grounded contact shadow
```
+ STYLE SUFFIX + NEGATIVE.

### 05 · Cable + Cargador Apple  *(mostrar producto, no la caja)*
```
Apple 20W USB-C power adapter standing upright next to an elegantly coiled
USB-C to Lightning cable, the actual products out of packaging, 3/4 eye-level
angle with slight top-down tilt, products filling ~45% height, calm spacing
```
+ STYLE SUFFIX + NEGATIVE.

### 06 · Kit iPhone 16 Pro Max  *(producto, no caja)*
```
Apple fast-charge kit for iPhone 16 Pro Max: 20W USB-C adapter and a braided
USB-C 60W cable neatly coiled, real products, 3/4 elevated angle, premium
arrangement with breathing room, matched bone backdrop
```
+ STYLE SUFFIX + NEGATIVE.

### 07 · JBL Go 2  *(rescatar del subexpuesto → variante graphite)*
```
JBL Go 2 portable bluetooth speaker, matte black fabric grille with orange JBL
loop, 3/4 angle, on the GRAPHITE variant surface (dark stone #1C1C1E to #0E0E10)
so the black product separates cleanly with a bright rim of soft light along its
top-left edge, strong key for material definition, grounded shadow
```
+ STYLE SUFFIX (swap "bone seamless" → "graphite stone seamless") + NEGATIVE.

### 08 · AirPods Pro 2  *(HERO / OG — fija el sistema)*
```
Apple AirPods Pro 2 charging case, closed, pristine white, floating buds detail
optional, single hero product, 3/4 angle at eye-level with subtle 12° top-down
tilt, centered slightly above optical center, large negative space, flagship
catalogue hero shot
```
+ STYLE SUFFIX + NEGATIVE. *(Esta es la imagen de mayor visibilidad: LCP + OG + primera card. Generarla primero y usarla como referencia de estilo para el resto.)*

### 09 · MagSafe Battery Pack  *(producto, no caja con hang-tab)*
```
Apple MagSafe Battery Pack, white, the actual product (no box, no hang tab),
shown attaching magnetically to the back of an iPhone or standalone at a clean
3/4 angle, soft single specular gradient, grounded contact shadow
```
+ STYLE SUFFIX + NEGATIVE.

### 10 · Elf Bar  *(eliminar packaging chillón y warning label)*
```
Elf Bar disposable vape device, single unit standing upright, minimal and clean,
NO retail box, NO warning labels, NO loud graphics, matte device finish, 3/4
eye-level angle, treated like a premium design object, calm bone backdrop,
grounded shadow
```
+ STYLE SUFFIX + NEGATIVE.

### 11 · AirPods Pro 2 · Edición  *(ya es producto — elevar)*
```
Apple AirPods Pro 2 with the charging case OPEN and both earbuds seated, white,
3/4 elevated angle showing the buds, single hero product, subtle specular
gradient on the glossy case, grounded contact shadow, generous negative space
```
+ STYLE SUFFIX + NEGATIVE.

---

## 4. Orden de prioridad

Prioridad = **visibilidad en el sitio × deficiencia actual**.

| Prioridad | Imagen | Por qué primero |
|-----------|--------|-----------------|
| **P1 — crítico** | **08 AirPods (hero/OG)** | Mayor visibilidad: imagen LCP precargada + OG social + primera card. **Generar primero** y usar como patrón de estilo del set |
| **P1** | **07 JBL Go 2** | Defecto más grave (se funde en negro). Mayor salto de calidad |
| **P1** | **10 Elf Bar** | Tell de marketplace más fuerte (warning label + packaging kiosko) |
| **P2 — alto** | **04 Pack Apple** | Card destacada "Más vendidos"; grid de cajas → producto |
| **P2** | **01 Argentina Campeón** | Primera card de la grilla, muy vista |
| **P2** | **05 / 06 Cable / Kit iPhone** | Hang-tab de reventa → producto real |
| **P3 — medio** | **02 Messi · 11 AirPods Edición** | Mejorables pero ya aceptables |
| **P3** | **03 Argentina 3★ · 09 MagSafe** | Solo unificar luz/fondo y quitar hang-tab |

**Flujo recomendado:** generar **08** → aprobar el look → generar **07 y 10** (mayor impacto) → resto en orden. Tras cada imagen, reconvertir a WebP (el pipeline `<picture>` ya está montado) manteniendo 4:5.

---

## 5. Checklist de aceptación (por imagen)

- [ ] Fondo es superficie real con textura, **no** un degradado.
- [ ] Mismo balance de blancos (5200K) que el resto del set.
- [ ] Sombra de contacto real anclando el producto (no flota, no recorte sticker).
- [ ] Sin hang-tab / blister / warning label / packaging chillón.
- [ ] Se ve el **producto**, no la caja (salvo 08 donde la caja sellada es el hero).
- [ ] Aire negativo generoso; producto en la escala normalizada de su categoría.
- [ ] 4:5, 1024×1280, nítido, sin artefactos de texto/IA.
