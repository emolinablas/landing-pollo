# Landing Page - Pollo a la Leña

Landing page ultrarrápida en HTML5 y CSS puro, optimizada para pedidos directos vía WhatsApp y lista para desplegar en Netlify.

## Estructura
- `index.html`: Página principal con menú (Entero Q95, Medio Q50, Cuarto Q28), propuesta de valor, proceso de pedido en 3 pasos y botón flotante de WhatsApp.
- `netlify.toml`: Configuración de headers de seguridad y publicación para Netlify.

## Configuración del Número de WhatsApp
En `index.html` (línea ~737), reemplaza:
```javascript
const NUMERO_WHATSAPP = "50254289478";
```
por tu número real con código de país (ejemplo: `50212345678`).

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
