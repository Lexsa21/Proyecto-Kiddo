# Kiddo Burger House

Landing page para una hamburguesería, con identidad visual fuerte, animaciones en CSS puro y diseño responsive. Sin frameworks ni librerías de JavaScript.

**Demo:** [lexsa21.github.io/Proyecto-Kiddo](https://lexsa21.github.io/Proyecto-Kiddo/)

## Qué tiene

- Hero animado con tipografía display y gradiente de marca
- Slider infinito hecho solo con `@keyframes`, sin JavaScript
- Cards del menú con hover de escala y desplazamiento
- Grid asimétrico en la sección de experiencias
- Formulario de reserva maquetado con CSS Grid
- Footer con imagen de fondo y overlay mediante pseudo-elemento
- Header fijo al scrollear y menú hamburguesa en mobile
- Responsive en mobile, tablet y desktop

## Stack

HTML5 semántico y CSS3, sin dependencias de build. El layout combina Grid y Flexbox según la sección. Las tipografías (Oleo Script, Bebas Neue, Alfa Slab One y Lato) vienen de Google Fonts, y los íconos del footer de Bootstrap Icons.

## Estructura

```
Proyecto-Kiddo/
├── index.html        # Página principal
├── styles.css        # Todos los estilos
└── img/              # Imágenes y assets
```

## Correr localmente

```bash
git clone https://github.com/Lexsa21/Proyecto-Kiddo.git
cd Proyecto-Kiddo
```

Abrí `index.html` en el navegador, o levantá un servidor local:

```bash
npx serve .
```

## Responsive

Tres breakpoints: 1024px para desktop, 768px para tablet y 480px para mobile. El slider y el grid de experiencias son los que más cambian de forma entre uno y otro.

## Sobre la implementación

El slider infinito fue la parte más interesante de resolver. La solución habitual es JavaScript con un temporizador, pero acá se logra duplicando la lista de items y animando el contenedor con `transform: translateX` en un ciclo que termina exactamente donde empieza. Como es una animación CSS, corre en la GPU y no necesita ni una línea de JS.

El overlay del footer usa un pseudo-elemento con fondo semitransparente en lugar de una imagen ya oscurecida, así el mismo archivo sirve para cualquier nivel de opacidad.

El formulario de reserva está armado con `grid-template-areas`, lo que permite reordenarlo entero en mobile cambiando solo la declaración de áreas, sin tocar el HTML.

---

Parte de mi portfolio: [lexsa21.github.io](https://lexsa21.github.io)
