# Web Premium para tu Negocio

Este proyecto crea webs profesionales con animaciones de scroll para cualquier tipo de negocio. Solo tienes que hablar con Claude Code y darle los datos de tu negocio.

## Comportamiento al iniciar

Cuando el usuario abra esta carpeta y escriba cualquier cosa, responde:

> **Bienvenido al creador de webs premium**
>
> Voy a crear una web profesional con animaciones de scroll para tu negocio.
>
> **¿Cómo se llama tu negocio y a qué se dedica?**

Después usa la skill `web-scrolling` automáticamente.

## Cómo funciona

1. Claude te pregunta los datos de tu negocio (nombre, servicios, precios, contacto...)
2. Con tus datos reales genera una web profesional con animaciones
3. La abre en tu navegador
4. Si quieres cambiar algo, díselo

## Reglas

- Solo usa tus datos reales — nunca inventa información
- Si no tienes fotos, usa placeholders y te avisa dónde poner las tuyas
- Si no tienes testimonios, omite esa sección

## Diseño responsivo (obligatorio)

Todo el código HTML/CSS que se genere debe ser 100% responsivo por defecto:

- **Unidades relativas:** usa `rem`, `em`, `%`, `vw`, `vh`, `clamp()` y `min()`/`max()` para tamaños, espaciados y tipografía. Evita `px` fijos salvo en bordes finos o sombras.
- **Medios fluidos:** imágenes, vídeos, canvas e iframes siempre con `max-width: 100%` y `height: auto`.
- **Layouts flexibles:** los contenedores flex usan `flex-wrap: wrap`; las rejillas usan `grid-template-columns: repeat(auto-fit, minmax(..., 1fr))` cuando tenga sentido.
- **Media queries:** enfoque mobile-first con breakpoints al menos en `min-width: 600px`, `900px` y `1200px`.
- **Viewport:** incluye siempre `<meta name="viewport" content="width=device-width, initial-scale=1">`.
- **Sin scroll horizontal:** nada debe desbordar el ancho de pantalla en móvil (comprobar a 360px de ancho).

## Si tienes un vídeo

Ponlo en `assets/hero.mp4` y pide "quiero el efecto de vídeo con scroll". El vídeo avanzará fotograma a fotograma con el scroll, como en la web de Apple.
