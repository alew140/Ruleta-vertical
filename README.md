# Ruleta Vertical (Vertical Roulette)

Una ruleta vertical interactiva construida con React que muestra imágenes o textos en una animación de desplazamiento vertical continuo.
DEMO: https://alew140.com/Over2

## Características

- Animación vertical fluida
- Soporte para imágenes y texto
- Tamaño responsive que se adapta a la altura de la ventana
- Configuración personalizable
- Borde y esquinas redondeadas personalizables
- Auto-inicio de la animación

## Requisitos

- React 18
- ReactDOM 18
- Babel (para JSX)
- TailwindCSS 2.2.19

## Configuración

El componente incluye varias opciones de configuración que pueden modificarse fácilmente:

### Items de la Ruleta
```javascript
const [items] = React.useState([
    { name: 'Item 1', imageUrl: 'URL_DE_LA_IMAGEN' },
    { name: 'Item 2', imageUrl: 'URL_DE_LA_IMAGEN' },
    { name: 'Item 3', imageUrl: 'URL_DE_LA_IMAGEN' },
]);
```

### Parámetros Configurables

- `speed`: Velocidad de la animación (default: 5000)
- `borde`: Ancho del borde en píxeles (default: 20)
- `rodondeado`: Radio de las esquinas [0-100] (default: 40)
- `colorDelBorde`: Color del borde (default: 'white')

## Uso

1. Incluye los scripts necesarios en tu HTML:
```html
<script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
<script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
```

2. Añade un contenedor con id "root":
```html
<div id="root"></div>
```

3. Personaliza los items de la ruleta modificando el array `items`:
```javascript
const [items] = React.useState([
    { 
        name: 'Nombre del Item', 
        imageUrl: 'URL_DE_LA_IMAGEN'
    },
    // Añade más items según necesites
]);
```

## Funcionamiento

- La ruleta comienza a girar automáticamente después de 500ms de carga
- El tiempo de giro es aleatorio (entre 3 y 10 segundos)
- Al detenerse, la ruleta se centra automáticamente en el item más cercano
- El tamaño se ajusta automáticamente al 90% de la altura de la ventana

## Notas Importantes

- Si no se proporciona una URL de imagen (`imageUrl`), se mostrará el nombre del item (`name`)
- La velocidad recomendada es 5000 para una animación fluida
- El ancho del borde recomendado es 20px
- El radio de redondeo recomendado es 40

## Personalización

Para modificar la apariencia:

1. Ajusta la velocidad:
```javascript
const speed = 5000; // Modifica según necesites
```

2. Modifica el borde:
```javascript
const borde = 20; // Ancho del borde en píxeles
const rodondeado = 40; // Radio de las esquinas
const colorDelBorde = 'white'; // Color del borde
```

## Estilo

El componente utiliza TailwindCSS para los estilos básicos y CSS personalizado para el fondo transparente. Para modificar los estilos, puedes ajustar las clases de Tailwind o añadir tus propios estilos CSS.
