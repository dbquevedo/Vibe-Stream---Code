# Vibe-Stream
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
        <div class="avatar-falso">V</div>ñ
        <div class="text-details">
            <div class="video-title">Título de tu genial video</div>
            <div class="video-meta">NombreDeTuCanal</div>
            <div class="video-meta">Hace 1 hora</div>
        </div>
    </div>
</div>
```

## 🤔Y que pasa si No tengo el Video y Solo lo tengo por Enlace
En caso si no tiene El video pero si el Codigo tambien puede poner el enlace, no es obligatorio
Si usted no tiene el video puede tambien quedar Asi
```html
<div class="video-card">
    <div class="thumbnail-wrapper">
        <video src="https://data.video/tu-video.mp4" poster="https://data.photo/tu-portada.jpg" controls preload="metadata"></video>
    </div>
    <div class="video-info">
        <div class="avatar-falso">V</div>ñ
        <div class="text-details">
            <div class="video-title">Título de tu genial video</div>
            <div class="video-meta">NombreDeTuCanal</div>
            <div class="video-meta">Hace 1 hora</div>
        </div>
    </div>
</div>
```
## 🟧⬛️ Es necesario tener siempre los mismos Colores
No, no es necesario que todo tenga los mismos colores
a pesar que puedes ponerle los colores no puedes cambiar el diseño
ya que eso Arruina nuestra marca

## 🖋️ Como puedo cambiar los Colores
para Cambiar los colores debes de ir Exactamente a esta Linea
```style
    <style>
        :root {
            --bg-main: #121212;
            --bg-nav: #1f1f1f;
            --bg-card: #181818;
            --text-main: #f0f0f0;
            --text-muted: #909090;
            --brand-orange: #f1680d;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        body { 
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; 
            background-color: var(--bg-main); 
            color: var(--text-main); 
            display: flex; 
            flex-direction: column; 
            height: 100vh; 
            overflow: hidden; 
        }

        /* Barra Superior */
        header { background-color: var(--bg-nav); height: 56px; display: flex; align-items: center; justify-content: space-between; padding: 0 24px; border-bottom: 1px solid #2d2d2d; z-index: 10; }
        .logo { display: flex; align-items: center; gap: 10px; font-weight: 700; font-size: 1.2rem; }
        .logo-icon { width: 26px; height: 26px; background-color: var(--brand-orange); border-radius: 6px; }
        .search-bar { background: #121212; border: 1px solid #383838; padding: 8px 16px; border-radius: 20px; width: 450px; color: white; font-size: 0.9rem; }

        .app-container { display: flex; flex: 1; overflow: hidden; }

        /* Menú Lateral */
        aside { width: 240px; background-color: var(--bg-nav); padding: 16px 8px; display: flex; flex-direction: column; gap: 4px; border-right: 1px solid #2d2d2d; }
        .menu-item { padding: 10px 14px; border-radius: 6px; text-decoration: none; color: var(--text-main); font-size: 0.9rem; display: flex; align-items: center; gap: 12px; }
        .menu-item.active { background-color: rgba(241, 104, 13, 0.15); color: var(--brand-orange); font-weight: 600; }

        /* Cuadrícula de Videos */
        main { flex: 1; padding: 24px 32px; overflow-y: auto; }
        h1 { font-size: 1.3rem; font-weight: 600; margin-bottom: 24px; }
        .video-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 24px; }
        
        .video-card { background-color: transparent; display: flex; flex-direction: column; gap: 10px; }
        
        .thumbnail-wrapper { width: 100%; aspect-ratio: 16/9; background-color: #000; border-radius: 8px; overflow: hidden; position: relative; border: 1px solid #252525; }
        .thumbnail-wrapper video { width: 100%; height: 100%; object-fit: cover; display: block; }
        
        .video-info { display: flex; gap: 12px; padding: 0 4px; }
        .avatar-falso { width: 36px; height: 36px; background: #333; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 0.8rem; font-weight: bold; }
        .text-details { display: flex; flex-direction: column; gap: 4px; }
        .video-title { font-size: 0.95rem; font-weight: 600; line-height: 1.4; color: #fff; }
        .video-meta { font-size: 0.85rem; color: var(--text-muted); }
    </style>
```
Puedes Cambiar los Colores de los Textos o el fondo pero el Diseño no

## ©️ Que pasa si Pongo Contenido con Derechos de Autor
Si ingresas contendio con Derechos de Autor en el sitio no pasara nada, ya que el sitio es privado, si lo deseas lo puedes publicar, pero si no lo deseas no pasa nada 

## ✅ℹ️🅱️3️⃣ Debe de Tener el Mismo nombre siempre o Puedo ponerle el que yo quiera
Porsupuesto que puedes cambiarla el Nombre y ponerle el que tu Desees, hasta puedes ponerle un logo distinto
**Para Ediar el Nombre debes de Modificarlo en estas lineas**
Titulo de la Pagina
```html
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vibe Stream - Tu Contendio Con Estilo (Open Sourse) - Gato Jardinero MIP</title>
```
Nombre de la Plataforma
```html
        <div class="logo">
            <div class="logo-icon"></div>
            <span>Vibe Stream</span>
        </div>
```
## ⚖️ Licencia
Este proyecto es de código abierto bajo la **Licencia MIT**. Puedes usarlo, modificarlo y distribuirlo libremente para cualquier tipo de plataforma.
