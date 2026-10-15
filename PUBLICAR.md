# Publicar Lingua como sitio web

Este paquete es el sitio estático de Lingua. Incluye la app, sus actividades, configuración de Supabase, archivos para instalarla en iPhone como PWA y recursos visuales.

## Publicación

Sube **todo el contenido de esta carpeta** a un hosting de sitios estáticos con HTTPS, por ejemplo Netlify, Vercel o Cloudflare Pages. La página de entrada es `index.html`. No cambies la ubicación relativa de `config.js`, `manifest.json`, `sw.js`, `features.js`, `practice.js`, `games.js`, `cefr-content.js`, `audio/` ni `icons/`.

## Configuración de autenticación

La app ya apunta al proyecto Supabase configurado en `config.js`. Para que Google y la confirmación por correo regresen al sitio publicado, en Supabase Authentication > URL Configuration configura:

- **Site URL:** la URL HTTPS principal publicada, por ejemplo `https://tu-dominio.example`.
- **Redirect URLs:** agrega la URL HTTPS exacta del sitio (y la variante con `www` si también la utilizarás).

En Google Cloud, configura el origen HTTPS del sitio como origen JavaScript autorizado. Conserva como URI de redirección autorizada el callback de Supabase que muestra el proveedor de Google en la configuración de inicio de sesión de Supabase. No uses una URL `file://`.

## Instalar en iPhone

1. Abre la dirección HTTPS publicada en Safari.
2. Pulsa Compartir > Añadir a pantalla de inicio.
3. Añade Lingua a la pantalla de inicio.

Para distribuir una app iOS nativa en App Store hace falta compilarla y firmarla con Xcode en macOS; este paquete es un sitio web instalable (PWA).
