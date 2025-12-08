<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Álbumes de Tavis scott</title>
  <style>
    :root {
      --negro: #AD0000;
      --azul: #F54927;
      --hueso: #FFFFFF;
      --marfil: #F54927;
      --blanco: #FFFFFF;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--marfil);
      color: var(--negro);
    }

    header {
      background-color: var(--azul);
      color: var(--blanco);
      padding: 1rem 2rem;
      text-align: center;
    }

    nav {
      background-color: var(--negro);
      padding: 0.5rem 2rem;
      display: flex;
      justify-content: center;
      gap: 2rem;
    }

    nav a {
      color: var(--blanco);
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s;
    }

    nav a:hover {
      color: var(--azul);
    }

    main {
      padding: 2rem;
    }

    .producto {
      background-color: var(--blanco);
      margin: 1rem auto;
      padding: 1rem;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      max-width: 800px;
    }

    .producto img {
      width: 100%;
      border-radius: 6px;
    }

    .producto h2 {
      color: var(--azul);
    }

    footer {
      background-color: var(--negro);
      color: var(--blanco);
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
    }
  
	/* Estilo para el canvas donde se dibujará la imagen */
        canvas {
			
			
            border: 5px solid #AD0000;
            border-radius: 8px;
            background-color: #AD0000;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            max-width: 90%;
        }
        .controles {
            margin-top: 25px;
            display: flex;
            gap: 15px; /* Espacio entre botones */
        }
        button {
            padding: 12px 25px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            border: none;
            border-radius: 6px;
            color: black;
            background-color: #AD0000;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }
        button:hover {
            background-color: #AD0000;
            transform: scale(1.05);
        }
	  
	  div.a {
  text-align: center;
}

div.b {
  text-align: left;
}

div.c {
  text-align: right;
} 

div.d {
  text-align: justify;
  
div.b {
  text-align: left;
}
	</style>
</head>
<body>
	
	
<header>
    <h1> Travis Scott </h1>
    <p>Sus mejores álbumes y Traks Unreleased </p>
</header>

  <nav>
    <a href="file:///Macintosh HD/Users/d/Downloads/HOME.html"><a href="file:///Users/fr/Downloads/HOME.html" target="file:///Users/lfr/Downloads/HOME.html"></a></a>
    <a href="file:///Macintosh HD/Users/f/Downloads/CATALOGO.html"></a>
    <a href="file:///Macintosh HD/Users/fr/Downloads/SUCURSALES.html"></a>
  </nav>
	
	<section>
    <article>
		<iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/track/4MXhiYIRDMGAuvZc5IFTwC?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
		<div class="a">
     <h1 style="background-color:FFFFFF;"> Sus mejores Álbumes </h1>
      
<canvas id="miCanvas" width="600" height="400">
        Tu navegador no soporta el elemento canvas.
    </canvas>
   <div class="w-33"
			<div class="controles"> 
     <!-- Tres botones, cada uno con un ID único -->
		<button id="btnElefante">AstroWorld</button>
        <button id="btnGato">Rodeo</button>
        <button id="btnPerro">Utopia</button>
    </div>

<script>
        // --- LÓGICA DE JAVASCRIPT ---

        // 1. Obtenemos referencias a nuestros elementos HTML
        const canvas = document.getElementById('miCanvas');
        const context = canvas.getContext('2d'); // El contexto 2D es la API para dibujar

        const btnElefante = document.getElementById('btnElefante');
        const btnGato = document.getElementById('btnGato');
        const btnPerro = document.getElementById('btnPerro');

        // URLs de las imágenes que vamos a cargar
        const urlElefante = 'https://m.media-amazon.com/images/I/81nFF-rXdRL._AC_SX679_.jpg';
        const urlGato = 'https://gcp-images.merchbar.com/eyJidWNrZXQiOiJtZXJjaGJhci1pbWFnZXMiLCJrZXkiOiJwcm9kdWN0LzU5LzI0OTMveTRjZHRzMDEvWTRDRFRTMDEuSlBHIiwiZWRpdHMiOnsicmVzaXplIjp7IndpZHRoIjoxNDAwLCJmaXQiOiJjb3ZlciJ9fX0=?format=webp';
        const urlPerro = 'https://blackroom.boutique/wp-content/uploads/2024/04/travis-scott-utopia.jpeg';

        /**
         * Función que carga una imagen desde una URL y la dibuja en el canvas.
         * @param {string} url - La dirección de la imagen a cargar.
         */
        function cargarImagenEnCanvas(url) {
            const imagen = new Image(); // Creamos un nuevo objeto de imagen
            imagen.src = url; // Le asignamos la URL

            // Esperamos a que la imagen se cargue completamente antes de dibujarla
            imagen.onload = () => {
                // Limpiamos el canvas por si había una imagen anterior
                context.clearRect(0, 0, canvas.width, canvas.height);
                // Dibujamos la nueva imagen, ajustándola al tamaño del canvas
                context.drawImage(imagen, 0, 0, canvas.width, canvas.height);
            };

            // Manejo de errores por si la imagen no se puede cargar
            imagen.onerror = () => {
                console.error(`Error al cargar la imagen desde: ${url}`);
                context.clearRect(0, 0, canvas.width, canvas.height);
                context.font = "16px Arial";
                context.fillStyle = "red";
                context.fillText("No se pudo cargar la imagen.", 20, 40);
            };
        }

        // 3. Asignamos los eventos de clic a cada botón
        btnElefante.addEventListener('click', () => {
            cargarImagenEnCanvas(urlElefante);
        });

        btnGato.addEventListener('click', () => {
            cargarImagenEnCanvas(urlGato);
        });

        btnPerro.addEventListener('click', () => {
            cargarImagenEnCanvas(urlPerro);
        });
        
        // Opcional: Mostramos un mensaje inicial en el canvas
        context.font = "10px Arial";
        context.textAlign = "center";
        context.fillText("Selecciona una pala para cargar su imagen", canvas.width / 2, canvas.height / 2);
    </script>
		
		<div class="a">
      <h1 style="background-
<body><div class="b">
    <h1 style="background-color:floralwhite;">
        Se parte de esto
    </h1>

    <form id="Travisform"> 
        <fieldset>
            <legend>Travis shop</legend>
            
            <label for="nombre">Nombre:</label>
            <input type="text" id="nombre" name="usuario_nombre" placeholder="Nombre (s)">
            <br><br>
            
            <label for="correo">Correo electrónico:</label>
            <input type="email" id="correo" name="correo" placeholder="ejemplo@.com" required>
            <br><br>
            
            <label for="telefono">Teléfono:</label>
            <input type="tel" id="telefono" name="telefono" placeholder="12-223-2987" required>
        </fieldset>
        <br><br>
        <button type="submit">Enviar Formulario</button>
    </form>
</div>

<script>
    // URL de tu Google Apps Script
    const scriptURL = '[https://script.google.com/macros/s/AKfycby6vVJAMJCL36N86EmLBs-AuX483lWFwz3GWlyjuTrjvPXlviDDAdJAk2CGLIm9WJ0y/exec](https://script.google.com/macros/s/AKfycbxlTJPHi0xdxP1EC0qZ3QjAPaJqoRy65l_w5MFb6RwLqM4cIX1EDK8NixLZ98UXr4azTw/exec)';
    
    // Obtenemos el formulario por su ID
    const form = document.getElementById('Travisform');

    form.addEventListener('submit', e => {
        e.preventDefault(); // Detiene el envío normal (para que no te redirija)
        
        // Desactivamos el botón y mostramos un mensaje temporal
        const submitButton = form.querySelector('button[type="submit"]');
        submitButton.disabled = true;
        submitButton.textContent = 'Enviando...';
        
        // Enviamos los datos usando Fetch API
        fetch(scriptURL, { method: 'POST', body: new FormData(form)})
            .then(response => {
                // El script devuelve JSON con {"result": "success"}
                if (response.ok) {
                    // Si es exitoso, mostramos una alerta y limpiamos el formulario.
                    alert('¡Gracias! Por ser parte de esto.');
                    form.reset(); 
                } else {
                    alert('Error: No se pudo conectar con el servidor de Google.');
                }
            })
            .catch(error => {
                alert('Ocurrió un error al enviar: ' + error.message);
                console.error('Error!', error.message);
            })
            .finally(() => {
                // Restauramos el botón después de la operación
                submitButton.disabled = false;
                submitButton.textContent = 'Enviar Formulario';
            });
    });
</script>

<footer>
    <p style="background-color:floralwhite">©️ 2025 Travis shop. Todos los derechos reservados.</p>
</footer>
</body>
</html>
