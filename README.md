 <!DOCTYPE html>
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
    <a href="file:///Macintosh HD/Users/leoaguilar/Downloads/HOME.html"><a href="file:///Users/leoaguilar/Downloads/HOME.html" target="file:///Users/leoaguilar/Downloads/HOME.html"></a></a>
    <a href="file:///Macintosh HD/Users/leoaguilar/Downloads/CATALOGO.html"></a>
    <a href="file:///Macintosh HD/Users/leoaguilar/Downloads/SUCURSALES.html"></a>
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
<body>
<div class="b">
<h1 style="background-color:F54927;"> ¿Quieres formar parte de esto? ¡registrate! </h1>
<form> 
<fieldset>
    <legend> Llena el siguiente formulario </legend>
<label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="usuario_nombre" placeholder="Nombre (s)">
    <input type="text" id="apellido Paterno" name="usuario_apellido" placeholder="Apellido Paterno">
    <input type="text" id="apellido Materno" name="usuario_apellido" placeholder="Apellido Materno">
	<br>
    <br>
    <label for="correo">Correo electrónico:</label>
	<input type="email" id="correo" name="correo" placeholder="ejemplo@.com" required>
	<br>
    <br> 
<label for="telefono">Teléfono:</label>
<input type="tel" id="telefono" name="telefono" placeholder="12-223-2987" required>
</fieldset>
	<br>
    <br> 
    <fieldset>
    <legend>¿Quieres comprar algo?</legend>
    <label for="street">Domicilio</label>
    <input type= user id="street" name="calle"placeholder="Usa numeros y letras">
    <label for="Interior/exterior number">
    Número interior/exterior</label>
    <input type= password id="Interior/exterior number" name="Numero interior
    /exterior"placeholder="Usa numeros y letras">
    <br>
     <label for="Cologne">Colonia</label>
    <input type= user id="Cologne" name="Colonia"placeholder="Usa numeros y letras">
    <label for="City">Ciudad</label>
    <input type= user id="City" name="Ciudad"placeholder="Usa numeros y letras">
    <br>
    <label for="Zip code">Código postal</label>
    <input type= user id="Zip code" name="Código postal"placeholder="Usa numeros y letras">
    </fieldset>
    <br>
    <br>
    
    <label for="Comentarios o Notas Extra"> ¿Tienes alguna queja o sugerencia? </label>
    <textarea id="Comentarios o Notas Extra" name="usuario_mensaje" rows="4" cols="50"></textarea>
	<br>
    <br>
    <label> ¿Facturarás tu pedido? </label><br>
    
    <input type="radio" id="opcion1" name="opcion_unica" value="a">
    <label for="opcion1">SI</label>
    
    <input type="radio" id="opcion2" name="opcion_unica" value="b">
    <label for="opcion2">NO</label>
    <br>
    <br>
    <fieldset>
    <legend> Factura aquí </legend>
    <label for="RFC">RFC</label>
    <input type= user id="RFC" name="RFC"placeholder="Usa numeros y letras">
    <label for="Name or company name"> Razón social </label>
    <input type= password id="Name or company name" name="Nombre o razón social"placeholder="Usa numeros y letras">
    </fieldset>
    <br>
    <br>
    <label>Método de pago</label><br>
    
    <input type="radio" id="opcion1" name="opcion_unica" value="a">
    <label for="opcion1">Tarjeta de debito</label>
 	 <input type="radio" id="opcion2" name="opcion_unica" value="b">
    <label for="opcion2">PayPal</label>
    <input type="radio" id="opcion3" name="opcion_unica" value="b">
    <label for="opcion3">Tarjeta de credito</label>
    <br>
    <br>
    <fieldset>
    <legend> Datos obligatorios </legend>
    <label>Acepto términos y condiciones</label><br>
    <input type="radio" id="opcion1" name="opcion_unica" value="a">
    <label for="opcion1">SI</label>
    <input type="radio" id="opcion2" name="opcion_unica" value="b">
    <label for="opcion2">NO</label>
      <br>
    <label>Confirmo que mis datos son correctos</label><br>
    <input type="radio" id="opcion1" name="opcion_unica" value="a">
    <label for="opcion1">SI</label>
    <input type="radio" id="opcion2" name="opcion_unica" value="b">
    <label for="opcion2">NO</label>
      <br>
    <label> Acepto recibir promociones, noticias y notificaciones </label><br>
    <input type="radio" id="opcion1" name="opcion_unica" value="a">
    <label for="opcion1">SI</label>
    <input type="radio" id="opcion2" name="opcion_unica" value="b">
    <label for="opcion2">NO</label>
    </fieldset>
    <br>
    <br>
   <button type="submit">Enviar Formulario</button>
</form>

<footer>
    
</footer>

</body>
</html>
		
    <p style=background-color:floralwhite>©️ 2025 TravisFans ADJNL Derechos reservados.</p>
  </footer>
</body>
</html>
