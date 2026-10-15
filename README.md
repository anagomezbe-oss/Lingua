# Lingua

Sitio web estático instalable como PWA en iPhone y Android. La entrada del sitio es `index.html`.

## Publicar desde GitHub con Vercel

1. Descomprime este paquete.
2. Crea un repositorio en GitHub y sube **el contenido** de esta carpeta (no hace falta subir el ZIP como archivo).
3. En Vercel, importa ese repositorio y publica el proyecto. No requiere comando de build.
4. Vercel generará una dirección HTTPS gratuita `*.vercel.app`.
5. Para que Google y la confirmación de correo regresen a Lingua, añade la URL publicada a las URLs permitidas de redirección en Supabase y configura el origen autorizado de Google.

El dominio `lingua.com` ya está en uso; utiliza la URL de Vercel u otro dominio que te pertenezca.

