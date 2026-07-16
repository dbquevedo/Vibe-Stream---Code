# Vibe-Stream---Code
Bienvenido a Vibe Stream, Vibe stream es una plataforma libre y de codigo abierto, con el codogo básicamente puedes crear tu propia YouTube, pero no es necesario usar VPS, carga el Archivo o enlace y Caratula del video y listo, si deseas agregarle servidor es tu decisión 
# 🚀 Vibe Stream - Tu Plataforma de Videos Personal y Gratis

Vibe Stream es una plantilla de código abierto (Open Source) diseñada para que cualquiera pueda crear su propio sitio web de videos con la estética oscura y profesional de PeerTube, **100% gratis y sin la obligación de administrar servidores ni bases de datos**.

Ideal para proyectos de videos divertidos, infantiles, creadores independientes o portafolios personales. El control es tuyo: funciona de forma local en tus dispositivos o se puede subir a internet sin costo.

## ✨ Características
* **Cero Servidores obligatorios**: Funciona leyendo tus archivos locales en la misma carpeta o mediante enlaces directos (como Internet Archive).
* **Diseño PeerTube**: Interfaz oscura moderna con menú lateral y cuadrícula adaptativa.
* **Libertad Total**: Úsalo para la temática que quieras. Si en el futuro deseas mudarte a un servidor propio, eres libre de hacerlo.
* **Sin JavaScript Obligatorio**: Evita bloqueos de seguridad en tabletas (iPad) y dispositivos móviles.

## 🛠️ Cómo crear tu propia plataforma en 3 pasos

1. **Descarga el código**: Copia el archivo `index.html` en una carpeta de tu computadora o tableta.
2. **Prepara tus archivos**: Coloca tus videos (`.mp4`) e imágenes de portada (`.jpg` o `.png`) dentro de esa misma carpeta.
3. **Personaliza**: Abre el código con cualquier editor de texto o bloc de notas, busca la sección `<div class="video-grid">` y cambia los nombres de los archivos por los tuyos:

```html
<div class="video-card">
    <div class="thumbnail-wrapper">
        <video src="tu-video.mp4" poster="tu-portada.jpg" controls preload="metadata"></video>
    </div>
    <div class="video-info">
        <div class="avatar-falso">V</div>
        <div class="text-details">
            <div class="video-title">Título de tu genial video</div>
            <div class="video-meta">NombreDeTuCanal</div>
            <div class="video-meta">Hace 1 hora</div>
        </div>
    </div>
</div>
```

## ⚖️ Licencia
Este proyecto es de código abierto bajo la **Licencia MIT**. Puedes usarlo, modificarlo y distribuirlo libremente para cualquier tipo de plataforma.
