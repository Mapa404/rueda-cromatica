# Rueda cromática

La rueda de color de papel, ahora para tocar en pantalla. Una web app interactiva para aprender y usar armonías de color, mezclar pinturas y jugar a adivinar mezclas.

## Qué hace

**Rueda**
- 12 colores de la rueda tradicional (amarillo, rojo, azul y sus mezclas), cada uno con su tinte, tono y sombra.
- Arrastrás el dial para girarlo, como la rueda física. También funciona con las flechas del teclado o tocando un color.
- 7 armonías: complementarios, análogos, tríada, complementario dividido, tétrada, cuadrado y monocromático.
- Variantes de cada paleta: puro, tinte (+ blanco), tono (+ gris) y sombra (+ negro).
- Copiás cualquier color, la lista de HEX o las variables CSS listas para usar.
- Vista previa de la paleta aplicada a una interfaz, con el contraste WCAG del botón y del título.
- Botón “Sorprendeme” para girar la rueda y probar una armonía al azar.
- Modo de giro libre, sin trabas, para tonos intermedios.

**Mezclador**
- Sumás gotas de rojo, amarillo, azul, blanco y negro y ves el resultado como en una paleta real (mezcla sustractiva).
- Muestra el nombre aproximado, el HEX, la escala de valor del 1 al 10 y te lleva al tono más cercano en la rueda.

**Desafío**
- Te muestra un color objetivo y tenés que lograrlo mezclando. Indica el porcentaje de parecido, da pistas y lleva una racha de aciertos.

## Accesibilidad

- Navegable con teclado (la rueda es un `slider` con flechas; las pestañas se mueven con ← →).
- Respeta `prefers-reduced-motion`.
- Mensajes de estado con `aria-live`.
- Sonido opcional, con botón para apagarlo.

## Cómo usarla

No necesita instalación ni build: es un solo archivo `index.html`.

```bash
git clone https://github.com/Mapa404/rueda-cromatica.git
cd rueda-cromatica
open index.html   # o abrilo con doble clic
```

### Publicarla

- **GitHub Pages:** Settings → Pages → Source: `Deploy from a branch` → `main` / `root`.
- **Netlify:** arrastrá la carpeta a app.netlify.com/drop o conectá el repo (sin comando de build, carpeta de publicación `/`).

## Tecnología

HTML, CSS y JavaScript sin dependencias. Las mezclas de tintes y tonos se calculan en OKLab; la mezcla de pinturas usa una media geométrica ponderada de la reflectancia para imitar la pintura real.

---

Hecho por [Mapa Bianchi](https://mapabianchi.online).
