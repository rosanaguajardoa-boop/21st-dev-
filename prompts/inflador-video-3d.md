# Prompt: vídeo 3D del inflador de neumáticos inalámbrico (modelo CZX11)

Datos del producto (sacados de la ficha de Alibaba): compresor inalámbrico de 12 V, hasta 150 PSI (10,3 bar), manómetro digital, luz LED de emergencia, función de batería externa (powerbank), un solo cilindro, cuerpo de plástico negro, 15,5 × 7,8 × 5,7 cm, certificado CE.

---

## PROMPT PRINCIPAL (copiar y pegar en el generador de vídeo)

```
Photorealistic 3D product animation of a compact cordless electric tire
inflator (handheld portable air compressor, matte black body, 15.5 x 7.8 x
5.7 cm, digital pressure display, built-in LED light, screw-on air hose),
matching the reference image exactly: same shape, colors, logo, button
layout, display position and proportions. Premium tech-launch aesthetic,
like an Apple or Dyson product film. Designed for a scroll-driven website
animation.

Continuous single shot, no cuts, no scene changes, constant smooth speed
from start to finish.

Sequence:
1. (0-3s) HOOK + REVEAL: The inflator emerges from darkness as a thin rim
   light traces its silhouette, then floats centered and rotates slowly
   360° on its vertical axis, showing every side: front with the digital
   display and buttons, side with the air outlet and hose, back, and the
   front LED light. Matte black plastic with subtle soft-touch texture.
2. (3-6s) EXPLODED VIEW: The product smoothly separates into its internal
   components, which float apart in an orderly way along clear axes,
   perfectly aligned and evenly spaced like a technical engineering
   diagram, revealing: the two outer shell halves, the digital LCD pressure
   display and control button panel, the main circuit board with pressure
   sensor, the lithium battery pack (cylindrical cells), the high-speed DC
   motor, the metal single-cylinder piston compressor with its cooling fins,
   the cooling fan, the front LED light module, the USB output port, and the
   braided air hose with brass valve connector. Every part is precise,
   metallic where appropriate, and clearly readable.
3. (6-8s) REASSEMBLY + FUNCTION: The components reassemble seamlessly back
   into the exact original product. The digital display lights up with
   crisp glowing numbers counting up to "35 PSI", the front LED light turns
   on with a soft cool-white glow, and a subtle, elegant stream of visible
   air particles flows out from the nozzle of the hose. The product ends
   perfectly still, centered, heroic 3/4 front view.

Background: solid seamless deep black #0A0A0A, no floor, no horizon, no
props, soft contact shadow only.

Camera: locked-off, perfectly stable, product always centered and fully
in frame (including all exploded parts), no camera shake, no zoom jumps.

Lighting: consistent studio lighting throughout, soft key light from the
upper left, strong cool-white rim light outlining the black silhouette so
the edges never disappear into the background, subtle warm accent on the
metal parts, no flicker, no lighting changes between frames (only the
product's own display and LED turn on in the final part).

Style: high-end tech product render, ultra-sharp detail, crisp edges,
precise mechanical parts, realistic materials (matte plastic, brushed
aluminium, copper motor windings, green PCB, brass fittings), cinematic
contrast, 8K quality, no motion blur.

Avoid: cuts, morphing, parts appearing from nowhere, parts leaving the
frame, distorted logos or text, extra or duplicated components, changing
the product's shape or color, background changes, floor or reflections,
blur, flicker, watermarks, text overlays, hands, people.

Format: 16:9, 8 seconds, 24 fps, highest resolution available.
```

---

## Variante: fondo blanco (para la ficha de producto de Shopify)

Cambia solo estas dos líneas:

```
Background: solid seamless pure white #FFFFFF, no floor, no horizon, no
props, soft contact shadow only.

Lighting: consistent bright studio lighting, soft large key light, subtle
edge definition, no flicker, no lighting changes between frames.
```

---

## Cómo usar el vídeo en la web con scroll

El vídeo no lleva texto a propósito. Los gráficos y titulares se ponen en la
web por encima del vídeo, así quedan nítidos, se pueden traducir y editar, y no
aparecen letras deformadas generadas por la IA.

| Scroll | Segundos | Qué se ve | Texto que aparece en la web |
|---|---|---|---|
| 0–15 % | 0–1,5 s | Sale de la oscuridad | **"Nunca más te quedes tirado."** |
| 15–35 % | 1,5–3 s | Giro de 360° | "Cabe en tu guantera · 15 cm · 700 g" |
| 35–50 % | 3–4,5 s | Empieza el despiece | "Por dentro, ingeniería de verdad" |
| 50–65 % | 4,5–6 s | Despiece completo | Etiquetas con líneas: *Motor DC de alta velocidad* · *Cilindro metálico* · *Batería de litio recargable* · *Sensor de presión* |
| 65–85 % | 6–7,5 s | Se vuelve a montar, se enciende | "Hasta 150 PSI. Se para solo al llegar a la presión." |
| 85–100 % | 7,5–8 s | Plano final | "3 en 1: inflador · linterna LED · powerbank" + botón **Comprar ahora** |

Consejos técnicos:
- Para que el scroll vaya suave, exporta el vídeo con un fotograma clave en
  cada fotograma: `ffmpeg -i video.mp4 -c:v libx264 -g 1 -crf 20 -an scroll.mp4`
  o extrae una secuencia de imágenes (`ffmpeg -i video.mp4 -vf fps=24 frames/%03d.webp`)
  y píntala en un `<canvas>` según el scroll, que es el método que usa Apple.
- Genera el vídeo 3 o 4 veces y quédate con la versión en la que el producto
  se parezca más a tus fotos. Sube 2 o 3 fotos de referencia (frontal, lateral
  y 3/4) si la herramienta lo permite.
- Herramientas recomendadas para este prompt: Google Veo 3, Kling 2.x, Runway
  Gen-4 o Luma Ray (todas aceptan imagen de referencia + 8 s).
