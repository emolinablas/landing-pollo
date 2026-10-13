# Landing Page - Pollo a la Leña

Landing page ultrarrápida en HTML5 y CSS puro, optimizada para pedidos directos vía WhatsApp y lista para desplegar en Netlify.

## Estructura
- `index.html`: Página completa (HTML, CSS y JS en un solo archivo). Secciones: hero, menú con armador de pedido (Entero Q95, Medio Q50, Cuarto Q28), el sabor, cómo pedir en 3 pasos, local y llamado final. El armador suma las porciones y abre WhatsApp con el pedido y el total ya escritos.
- `images/`: Fotos en WebP recortadas sin texto encima, logo con fondo transparente, favicon e imagen para compartir en redes (`og-image.jpg`).
- `netlify.toml`: Configuración de headers de seguridad y publicación para Netlify.

## Configuración del Número de WhatsApp
El número aparece en los enlaces `wa.me` y en la constante `WHATSAPP` del script al final de `index.html`. Para cambiarlo, busca y reemplaza `50254289478` en todo el archivo por tu número con código de país (ejemplo: `50212345678`). Si cambia el número visible, reemplaza también `5428-9478`.

## Cambiar precios
Cada tarjeta del menú tiene `data-price` (lo usa el armador de pedido) y el precio visible dentro de `.price`. Actualiza ambos, junto con los precios del hero (`.hero-prices`) y el texto del mensaje en el enlace de la tarjeta.

---

## Cómo subir a GitHub y publicar en Netlify

### Opción 1: Repositorio independiente (Recomendado)
Desde la terminal, sitúate en la carpeta `landing-pollo`:

```bash
cd /Users/evermolina/Documents/Codigo/www/vid/landing-pollo
git init
git add .
git commit -m "feat: landing page pollo a la lena"
git branch -M main
```

1. Crea un repositorio vacío en tu GitHub llamado `landing-pollo`.
2. Vincula y sube los cambios:
```bash
git remote add origin https://github.com/TU_USUARIO/landing-pollo.git
git push -u origin main
```
3. En [Netlify](https://app.netlify.com/):
   - Haz clic en **"Add new site"** > **"Import an existing project"** > **GitHub**.
   - Selecciona el repositorio `landing-pollo`.
   - Deja "Build command" en blanco y "Publish directory" en `.`.
   - Haz clic en **Deploy**. ¡Listo en 5 segundos!

### Opción 2: Arrastrar y soltar (Netlify Drop - Inmediato sin GitHub)
1. Entra a [Netlify Drop](https://app.netlify.com/drop).
2. Arrastra la carpeta `landing-pollo` directamente al navegador.
3. El sitio estará activo al instante con una URL gratuita `.netlify.app`.
