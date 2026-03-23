# Brain Solutions

Sitio web estático de presentación para Brain Solutions.

## Stack

- HTML5
- CSS3
- JavaScript vanilla (script inline en el propio HTML)

## Estructura del proyecto

```text
brain-solutions/
├─ index.html
├─ README.md
└─ assets/
	├─ css/
	│  └─ style.css
	└─ img/
		├─ ...
```

Nota: el logo principal y la imagen de logística siguen referenciados desde Netlify porque esos archivos no están aún en `assets/img`.

## Cómo ejecutarlo en local

Opción rápida:
1. Abrir `index.html` en el navegador.

Opción recomendada (servidor local):
1. Desde la raíz del proyecto ejecutar:

```bash
python -m http.server 5500
```

2. Abrir:

```text
http://localhost:5500
```

## Edición de contenido

- Texto y estructura de secciones: `index.html`
- Estilos globales: `assets/css/style.css`
- Imágenes locales: `assets/img/`

## Pendiente para dejar producción al día

Objetivo: publicar todas las imágenes locales en Netlify, actualizar las referencias en `index.html` a URLs de Netlify y desplegar la versión final para acceso público.

### 1) Hostear en Netlify las imágenes de `assets/img`

Subir al host público de Netlify:

- `assets/img/enfoque.png`
- `assets/img/servicios.png`
- `assets/img/calidad.png`
- `assets/img/coaching.png`
- `assets/img/beneficios.png`
- `assets/img/marcelo.jpg`
- `assets/img/flavio.jpg`

También dejar disponibles en Netlify (ya usadas actualmente):

- `logo.png`
- `logistica.jpg`

### 2) Actualizar referencias en `index.html`

Cambiar las rutas locales de imágenes para que apunten al host público de Netlify.

Formato sugerido:

- `https://brainsolutions.netlify.app/NOMBRE_ARCHIVO`

Ejemplos:

- `https://brainsolutions.netlify.app/enfoque.png`
- `https://brainsolutions.netlify.app/servicios.png`
- `https://brainsolutions.netlify.app/calidad.png`
- `https://brainsolutions.netlify.app/coaching.png`
- `https://brainsolutions.netlify.app/beneficios.png`
- `https://brainsolutions.netlify.app/marcelo.jpg`
- `https://brainsolutions.netlify.app/flavio.jpg`

### 3) Deploy del `index.html` final

- Verificar que el `index.html` local tenga todos los cambios visuales y funcionales.
- Publicar esa versión en Netlify (deploy manual o por repositorio conectado).
- Confirmar en el dominio público que se ven todos los cambios.

### 4) Checklist de validación pública

- No hay imágenes rotas (sin errores 404).
- Hero, Servicios, Beneficios y Equipo muestran imágenes correctas.
- Navbar y favicon cargan correctamente.
- El sitio público coincide con la última versión local.
