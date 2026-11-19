# MULTIMEDIAL
#### Exploración creativa de arte, tecnología y medios digitales interactivos.

#### Cultura web y arte digital.

#### UNIDAD I

Ejercicio 1, semana 1:

```js
<!DOCTYPE html>
<!-- Indica al navegador que este documento usa HTML5 -->

<html>
<!-- Inicio del documento HTML -->

<head>
<!-- Sección donde van metadatos, título y estilos -->

<meta charset="UTF-8">
<!-- Define la codificación de caracteres para que se vean bien tildes y símbolos -->

<title>Multimedial</title>
<!-- Título de la página que aparece en la pestaña del navegador -->

<style>
/* Aquí comienza la sección de estilos CSS que define la apariencia visual */

body{
/* "body" se refiere a todo el contenido visible de la página */

  background-color: white;
  /* Define que el fondo de toda la página sea blanco */

  color: black;
  /* Define que el color del texto sea negro */

  margin: 0;
  /* Elimina los márgenes que los navegadores agregan por defecto */

  height: 100vh;
  /* Hace que el alto del cuerpo sea igual al 100% de la altura de la pantalla */

  display: flex;
  /* Activa el sistema Flexbox para organizar y centrar elementos */

  justify-content: center;
  /* Centra el contenido horizontalmente */

  align-items: center;
  /* Centra el contenido verticalmente */

  font-family: Arial, sans-serif;
  /* Define la tipografía del texto */

  font-size: 60px;
  /* Define el tamaño grande del texto */

}
/* Fin de las reglas de estilo del body */

</style>
<!-- Fin de la sección de estilos -->

</head>
<!-- Fin de la sección head -->

<body>
<!-- Inicio del contenido visible de la página -->

MULTIMEDIAL
<!-- Texto que aparece en el centro de la pantalla -->

</body>
<!-- Fin del contenido visible -->

</html>
<!-- Fin del documento HTML -->

```
### Mi primera página web

Index:

```js
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Digital Media - Inicio</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            /* Transición suave para el color de fondo */
            background-color: #e0e5ec; 
            font-family: 'Courier New', Courier, monospace;
            transition: background-color 0.8s ease;
        }

        /* Cambia el fondo de la página cuando pasas el mouse por la ventana */
        body:has(.ventana-principal:hover) {
            background-color: #d1d9e6;
        }

        .ventana-principal {
            background-color: white;
            border: 2px solid #333;
            box-shadow: 8px 8px 0px SteelBlue; 
            padding: 40px;
            max-width: 500px;
            text-align: center;
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .ventana-principal:hover {
            transform: scale(1.01);
            box-shadow: 12px 12px 0px #4682B4;
        }

        h1 {
            font-size: 2.5rem;
            color: #2d3436;
            border-bottom: 2px solid SteelBlue;
            padding-bottom: 10px;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .perfil-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border: 1px solid #333;
            margin-bottom: 20px;
            /* Imagen limpia, sin filtros de color */
        }

        .nav-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 10px;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: bold;
            padding: 12px 25px;
            border: 2px solid #333;
            background-color: white;
            position: relative;
            z-index: 1;
            transition: all 0.3s ease;
            overflow: hidden;
        }

        /* --- ANIMACIÓN VIBRANTE DE COLOR --- */
        @keyframes vibrante {
            0% { background-color: #4682B4; border-color: #333; }
            33% { background-color: #00ced1; border-color: #00ced1; }
            66% { background-color: #1e90ff; border-color: #1e90ff; }
            100% { background-color: #4682B4; border-color: #333; }
        }

        .nav-links a:hover {
            color: white;
            transform: translateY(-5px);
            /* Aplicamos la animación cíclica al hover */
            animation: vibrante 1.5s infinite linear;
            box-shadow: 0 10px 20px rgba(70, 130, 180, 0.3);
        }

        .nav-links a:active {
            transform: translateY(0);
            box-shadow: none;
        }

    </style>
</head>
<body>

    <div class="ventana-principal">
        <h1>DIGITAL MEDIA</h1>
        <img src="img/inicio.jpg" alt="Inicio" class="perfil-img">
        
        <div class="nav-links">
            <a href="obras.html">OBRAS</a>
            <a href="contacto.html">CONTACTO</a>
        </div>
    </div>

</body>
</html>
```
Obras:

```js
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Obras - Pulsaciones de Color</title>
    <style>
        body {
            background-color: #f8f9fa;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 40px;
            /* Transición suave para el cambio de fondo */
            transition: background-color 0.6s ease;
        }

        /* EFECTO DE FONDO REACTIVO:
           Cuando el cursor está sobre una card, el fondo del body 
           se tiñe levemente del color de esa obra (con mucha transparencia) */
        body:has(.obra-card:hover) {
            background-color: #f0f2f5; /* Un tono base de reacción */
        }

        .header-obras {
            text-align: center;
            margin-bottom: 50px;
        }

        .separador-serie {
            text-align: center;
            margin-top: 100px; 
            margin-bottom: 50px;
            padding-top: 40px;
            border-top: 2px dashed #ddd; 
        }

        .grid-obras {
            display: flex;
            flex-wrap: wrap; 
            justify-content: center;
            gap: 25px; 
            max-width: 1200px;
            margin: 0 auto;
        }

        .obra-card {
            background: white;
            border: 1px solid #ddd;
            padding: 15px;
            width: 250px; 
            box-shadow: 4px 4px 10px rgba(0,0,0,0.05);
            transition: 0.3s;
            cursor: pointer;
            --color-obra: #adb5bd;
            position: relative;
            z-index: 1;
        }

        /* EFECTO DE AURA INTERACTIVA */
        .obra-card:hover {
            border-color: var(--color-obra);
            transform: scale(1.05); /* Un poco más de escala para resaltar */
            box-shadow: 0 10px 30px rgba(0,0,0,0.1), 0 0 20px var(--color-obra);
            z-index: 10;
        }

        .obra-card img {
            width: 100%;
            height: 200px;
            object-fit: cover; 
            border-bottom: 1px solid #eee;
            margin-bottom: 10px;
        }

        .obra-card h2 {
            font-size: 14px;
            color: #555;
            margin: 5px 0;
        }

        .obra-card p {
            font-size: 12px;
            color: #888;
        }

        .btn-volver {
            display: inline-block;
            margin-top: 20px;
            text-decoration: none;
            color: SteelBlue;
            font-weight: bold;
            transition: 0.3s;
        }
        
        .btn-volver:hover {
            color: #4682B4;
            transform: translateX(-5px);
        }

        /* ESTILOS DEL ZOOM (LIGHTBOX) */
        .lightbox {
            display: none;
            position: fixed;
            z-index: 1000;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background-color: rgba(0, 0, 0, 0.85);
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .lightbox.active {
            display: flex;
            opacity: 1;
        }

        .lightbox-img {
            max-width: 90%;
            max-height: 85%;
            border: 3px solid white;
            box-shadow: 0 0 30px rgba(0,0,0,0.5);
            transform: scale(0.9);
            transition: transform 0.4s ease;
        }

        .lightbox.active .lightbox-img {
            transform: scale(1);
        }

        .close-lightbox {
            position: absolute;
            top: 20px; right: 30px;
            color: white;
            font-size: 40px;
            cursor: pointer;
        }

        body.modal-open { overflow: hidden; }
    </style>
</head>
<body>

    <div class="header-obras">
        <h1>Pulsaciones de Color</h1>
        <p>Serie completa de 30 piezas</p>
        <a href="index.html" class="btn-volver">← Volver al inicio</a>
    </div>

    <div id="lightbox" class="lightbox">
        <span class="close-lightbox" id="close-lightbox">&times;</span>
        <img class="lightbox-img" id="lightbox-img" src="" alt="Obra Ampliada">
    </div>

    <div class="grid-obras">
        <div class="obra-card" style="--color-obra: #ff85a2;"><img src="img/1.jpg"><h2>N° 1</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #4dabf7;"><img src="img/2.jpg"><h2>N° 2</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #51cf66;"><img src="img/3.jpg"><h2>N° 3</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #fcc419;"><img src="img/4.jpg"><h2>N° 4</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #ff85a2;"><img src="img/5.jpg"><h2>N° 5</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #4dabf7;"><img src="img/6.jpg"><h2>N° 6</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #51cf66;"><img src="img/7.jpg"><h2>N° 7</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #fcc419;"><img src="img/8.jpg"><h2>N° 8</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #ff85a2;"><img src="img/9.jpg"><h2>N° 9</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #4dabf7;"><img src="img/10.jpg"><h2>N° 10</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #51cf66;"><img src="img/11.jpg"><h2>N° 11</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #fcc419;"><img src="img/12.jpg"><h2>N° 12</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #ff85a2;"><img src="img/13.jpg"><h2>N° 13</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #4dabf7;"><img src="img/14.jpg"><h2>N° 14</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #51cf66;"><img src="img/15.jpg"><h2>N° 15</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #fcc419;"><img src="img/16.jpg"><h2>N° 16</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #ff85a2;"><img src="img/17.jpg"><h2>N° 17</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #4dabf7;"><img src="img/18.jpg"><h2>N° 18</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #51cf66;"><img src="img/19.jpg"><h2>N° 19</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #fcc419;"><img src="img/20.jpg"><h2>N° 20</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #ff85a2;"><img src="img/21.jpg"><h2>N° 21</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #4dabf7;"><img src="img/22.jpg"><h2>N° 22</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #51cf66;"><img src="img/23.jpg"><h2>N° 23</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #fcc419;"><img src="img/24.jpg"><h2>N° 24</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #ff85a2;"><img src="img/25.jpg"><h2>N° 25</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #4dabf7;"><img src="img/26.jpg"><h2>N° 26</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #51cf66;"><img src="img/27.jpg"><h2>N° 27</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #fcc419;"><img src="img/28.jpg"><h2>N° 28</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #ff85a2;"><img src="img/29.jpg"><h2>N° 29</h2><p>Papel recortado, 2025.</p></div>
        <div class="obra-card" style="--color-obra: #4dabf7;"><img src="img/30.jpg"><h2>N° 30</h2><p>Papel recortado, 2025.</p></div>
    </div>

    <div class="separador-serie">
        <h1>Condición Digital</h1>
        <p>CD escaneado en Photoshop e intervenido</p>
    </div>

    <div class="grid-obras">
        <div class="obra-card" style="--color-obra: #ff00ff;"><img src="img/rosado.jpg"><h2>Magenta</h2><p>Intervención digital, 2023.</p></div>
        <div class="obra-card" style="--color-obra: #0000ff;"><img src="img/azul.jpg"><h2>Blue</h2><p>Intervención digital, 2023.</p></div>
        <div class="obra-card" style="--color-obra: #ffff00;"><img src="img/amarillo.jpg"><h2>Yellow</h2><p>Intervención digital, 2023.</p></div>
    </div>

    <div class="separador-serie">
        <h1>Módulo Díez</h1>
        <p>Serie de pinturas</p>
    </div>

    <div class="grid-obras">
        <div class="obra-card" style="--color-obra: #ff0000;">
            <img src="img/modulo.png">
            <h2>Módulo Díez</h2><p>Acrílico sobre MDF, 2026.</p>
        </div>
    </div>

    <div class="separador-serie">
        <h1>SHEETS</h1>
        <p>Serie de pinturas</p>
    </div>

    <div class="grid-obras">
        <div class="obra-card" style="--color-obra: #8e44ad;">
            <img src="img/laminas.jpg">
            <h2>SHEETS</h2><p>Esmalte al agua sobre MDF, 2026.</p>
        </div>
    </div>

    <div style="text-align: center; margin: 80px 0;">
        <a href="index.html" class="btn-volver">Volver al inicio</a>
    </div>

    <script>
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = document.getElementById('lightbox-img');
        const closeBtn = document.getElementById('close-lightbox');
        const body = document.body;

        // Mejoramos el script para que el fondo cambie dinámicamente al color de la obra
        document.querySelectorAll('.obra-card').forEach(card => {
            card.addEventListener('mouseenter', () => {
                const color = card.style.getPropertyValue('--color-obra');
                // Aplicamos el color con mucha transparencia (opacidad baja)
                body.style.backgroundColor = color + "15"; 
            });
            
            card.addEventListener('mouseleave', () => {
                body.style.backgroundColor = "#f8f9fa"; // Volver al color original
            });
        });

        document.addEventListener('click', (e) => {
            const card = e.target.closest('.obra-card');
            if (card) {
                const img = card.querySelector('img');
                lightboxImg.src = img.src;
                lightbox.classList.add('active');
                body.classList.add('modal-open');
            }
        });

        function closeLightbox() {
            lightbox.classList.remove('active');
            body.classList.remove('modal-open');
        }

        closeBtn.addEventListener('click', closeLightbox);
        lightbox.addEventListener('click', (e) => {
            if (e.target === lightbox) closeLightbox();
        });

        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') closeLightbox();
        });
    </script>
</body>
</html>
```
Contacto:

```js
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Contacto</title>
    <style>
        body {
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #d1d8e0;
            margin: 0;
            font-family: 'Courier New', Courier, monospace;
            /* Transición suave para el fondo de la página */
            transition: background-color 0.6s ease;
        }

        /* El fondo reacciona cuando interactúas con la caja de contacto */
        body:has(.contacto-box:hover) {
            background-color: #c0c9d3;
        }

        .contacto-box {
            background: white;
            border: 2px solid black;
            width: 350px;
            padding: 0;
            overflow: hidden;
            /* Sombra sólida roja que combina con el tema */
            box-shadow: 8px 8px 0px rgba(220, 20, 60, 0.4);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .contacto-box:hover {
            transform: scale(1.02);
            box-shadow: 12px 12px 0px crimson;
        }

        .barra-superior {
            background: black;
            color: white;
            padding: 5px 10px;
            font-size: 12px;
            display: flex;
            justify-content: space-between;
            transition: background 0.3s;
        }

        /* La barra superior se ilumina en rojo al pasar el cursor por la caja */
        .contacto-box:hover .barra-superior {
            background: crimson;
        }

        .contenido-contacto {
            padding: 30px;
            text-align: center;
        }

        .contenido-contacto img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            border: 2px solid black;
            margin-bottom: 15px;
            transition: transform 0.5s ease;
        }

        .contacto-box:hover img {
            transform: rotate(5deg);
        }

        .email {
            font-weight: bold;
            background: #ffffcc;
            padding: 5px;
            border: 1px dashed transparent;
            transition: 0.3s;
        }

        .contacto-box:hover .email {
            border-color: crimson;
            background: #fff0f0;
        }

        .links-nav {
            margin-top: 20px;
            border-top: 1px dashed black;
            padding-top: 15px;
        }

        .links-nav a {
            text-decoration: none;
            color: black; /* Cambiado a negro para que el rojo destaque más */
            font-size: 14px;
            margin: 0 10px;
            padding: 5px 10px;
            border: 1px solid transparent;
            transition: all 0.3s ease;
            display: inline-block;
        }

        /* --- ANIMACIÓN VIBRANTE EN ROJO --- */
        @keyframes vibrante-rojo {
            0% { background-color: crimson; }
            50% { background-color: #ff4d4d; }
            100% { background-color: #b30000; }
        }

        .links-nav a:hover {
            color: white;
            transform: translateY(-3px);
            animation: vibrante-rojo 1s infinite alternate;
            box-shadow: 0 5px 10px rgba(220, 20, 60, 0.3);
            border-color: black;
        }

        .links-nav a:active {
            transform: translateY(0);
        }
    </style>
</head>
<body>

    <div class="contacto-box">
        <div class="barra-superior">
            <span>contacto.exe</span>
            <span>[X]</span>
        </div>
        <div class="contenido-contacto">
            <img src="img/contact.jpg" alt="Contacto">
            <p>¿Tienes dudas?</p>
            <p class="instagram">Instagram - gg.loyola</p>
            
            <div class="links-nav">
                <a href="index.html">Inicio</a>
                <a href="obras.html">Obras</a>
            </div>
        </div>
    </div>

</body>
</html>
```
### Unidad II. [Programación visual creativa basada en nodos]II: 
### Programación visual creativa basada en nodos. 

#### PROCESO

Bocetos previos:



#### ENTREGA

- Carpeta 1: [Desarrollo técnico](https://drive.google.com/drive/folders/1uITbzPT7acqZKZbtXDkI69XUZxU-1WL3)


- Carpeta 2: [Experimentación](https://drive.google.com/drive/folders/1uITbzPT7acqZKZbtXDkI69XUZxU-1WL3)

- Carpeta 3: [Video ejemplo](https://drive.google.com/drive/folders/1uITbzPT7acqZKZbtXDkI69XUZxU-1WL3) 


