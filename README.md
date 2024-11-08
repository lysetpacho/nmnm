<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tienda de Moda Femenina - Modaz</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* Estilos CSS en tonos rosados */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            color: #333;
            background-color: #fce4ec;
        }

        header {
            background-color: #e91e63;
            color: #fff;
            padding: 1rem 0;
            position: relative;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }

        header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: auto;
            padding: 0 1rem;
        }

        header .logo {
            font-size: 1.8rem;
            font-family: 'Playfair Display', serif;
            letter-spacing: 2px;
        }

        header nav ul {
            display: flex;
            list-style: none;
        }

        header nav ul li {
            margin-left: 1.5rem;
        }

        header nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }

        header nav ul li a:hover {
            color: #ffccbc;
        }

        header .cart {
            position: relative;
            color: #fff;
            cursor: pointer;
        }

        header .cart .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background-color: #ff1744;
            color: #fff;
            border-radius: 50%;
            padding: 0.2rem 0.6rem;
            font-size: 0.9rem;
        }

        .hero {
            background: #f8bbd0 url('https://r.mobirisesite.com/864296/assets/images/photo-1486308510493-aa64833637bc.jpeg') center/cover no-repeat;
            color: #333;
            padding: 4rem 0;
            text-align: center;
            position: relative;
        }

        .hero h2 {
            font-size: 3rem;
            font-family: 'Playfair Display', serif;
            margin-bottom: 1rem;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
        }

        .hero .button {
            background-color: #e91e63;
            color: #fff;
            padding: 0.7rem 2rem;
            border: none;
            border-radius: 5px;
            text-decoration: none;
            margin-top: 1rem;
            display: inline-block;
            transition: background-color 0.3s;
        }

        .hero .button:hover {
            background-color: #d81b60;
        }

        .banners {
            display: flex;
            justify-content: center;
            margin: 2rem 0;
            gap: 1rem;
        }

        .banner {
            background-color: #fff;
            border-radius: 5px;
            padding: 1rem;
            text-align: center;
            width: 300px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
        }

        .banner:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }

        .banner h3 {
            color: #e91e63;
            margin-bottom: 0.5rem;
        }

        .banner p {
            margin-bottom: 0.5rem;
        }

        .promotions {
            text-align: center;
            margin: 2rem 0;
            font-size: 1.5rem;
            color: #e91e63;
        }

        section {
            padding: 4rem 0;
        }

        h2 {
            text-align: center;
            margin-bottom: 2rem;
            font-size: 2rem;
            color: #e91e63;
        }

        .product-grid {
            display: flex;
            gap: 1.5rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .product-card {
            background-color: #fff;
            border: 1px solid #ddd;
            border-radius: 5px;
            width: 220px;
            padding: 1rem;
            text-align: center;
            transition: transform 0.2s;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .product-card img {
            width: 100%;
            border-radius: 5px;
            margin-bottom: 1rem;
        }

        .product-card h3 {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
            font-family: 'Playfair Display', serif;
        }

        .product-card p {
            color: #e91e63;
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }

        .product-card .button {
            background-color: #e91e63;
            color: #fff;
            padding: 0.5rem 1rem;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .product-card .button:hover {
            background-color: #d81b60;
        }

        .cart-items {
            position: fixed;
            top: 0;
            right: 0;
            width: 300px;
            height: 100%;
            background-color: #fff;
            box-shadow: -2px 0 5px rgba(0, 0, 0, 0.2);
            padding: 1rem;
            display: none;
            overflow-y: auto;
            z-index: 1000;
        }

        .cart-items h3 {
            margin-bottom: 1rem;
            color: #e91e63;
            font-family: 'Playfair Display', serif;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 1px solid #ddd;
        }

        .cart-item p {
            color: #333;
        }

        .cart-item button {
            background-color: #ff1744;
            color: #fff;
            border: none;
            border-radius: 3px;
            cursor: pointer;
        }

        footer {
            background-color: #e91e63;
            color: #fff;
            text-align: center;
            padding: 1rem 0;
            margin-top: 2rem;
        }

        /* Sección de filosofía */
        .philosophy {
            display: flex;
            justify-content: space-between;
            margin: 2rem 0;
        }

        .philosophy .column {
            width: 48%;
            padding: 1rem;
            background-color: #fff;
            border: 1px solid #ddd;
            border-radius: 5px;
            transition: transform 0.2s;
        }

        .philosophy .column:hover {
            transform: scale(1.02);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .fade-in {
            animation: fadeIn 1s;
        }
/* Sección de filosofía */
        .philosophy {
            display: flex;
            justify-content: space-around; /* Evenly space columns */
            margin: 2rem 0;
            text-align: center; /* Center text */
        }

        .philosophy .column {
            width: 48%;
            padding: 1rem;
            background-color: #fff;
            border: 1px solid #ddd;
            border-radius: 5px;
            transition: transform 0.2s;
        }

        .philosophy .column:hover {
            transform: scale(1.02);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .fade-in {
            animation: fadeIn 1s;
        }

        /* Sección de redes sociales */
        .social-media {
            margin: 2rem 0;
        }

        .social-media a {
            margin: 0 1rem;
            font-size: 1.5rem;
            color: #e91e63;
            text-decoration: none;
        }

        /* Sección de marcas aliadas */
        .partners {
            margin: 2rem 0;
        }

        .partner {
            display: inline-block;
            text-align: center;
            margin: 0 1rem;
        }

        .partner img {
            width: 100px;
            height: auto;
            margin-bottom: 0.5rem;
        }
    </style>
</head>

<body>

    <!-- Encabezado -->
    <header>
        <div class="container">
            <h1 class="logo">Modaz</h1>
            <nav>
                <ul>
                    <li><a href="#home">Inicio</a></li>
                    <li><a href="#about">Nosotros</a></li>
                    <li><a href="#philosophy">Filosofía</a></li>
                    <li><a href="#products">Productos</a></li>
                    <li><a href="#contact">Contacto</a></li>
                </ul>
            </nav>
            <div class="cart" onclick="toggleCart()">
                🛒 Carrito <span class="cart-count" id="cart-count">0</span>
            </div>
        </div>
    </header>

    <section id="presentacion" style="padding: 4rem 2rem; background-color: #f3b3de; text-align: center;">
    <h1 style="color: #333; margin-bottom: 2.2rem;">Bienvenidos a MODA Z</h1>
    <p style="font-size: 1.8rem; color: #f93ae1; max-width: 600px; margin: 0 auto;">
        En Modaz, ofrecemos una amplia variedad de ropa de alta calidad que se adapta a todos los estilos y ocasiones. Nuestra misión es proporcionar prendas que no solo sean elegantes, sino también cómodas, para que cada uno de nuestros clientes se sienta seguro y especial.
    </p>
    <a href="#productos" style="display: inline-block; margin-top: 2rem; padding: 10px 20px; background-color: #ff00f7; color: #ffffff; text-decoration: none; border-radius: 5px;">
        Explora Nuestros Productos
    </a>
</section>


    <!-- Banners publicitarios -->
    <div class="banners">
        <div class="banner">
            <h3>¡Nuevas Llegadas!</h3>
            <p>Descubre la colección de esta temporada.</p>
            <a href="#products" class="button">Ver Más</a>
        </div>
        <div class="banner">
            <h3>Descuentos Especiales</h3>
            <p>¡Hasta un 30% en productos seleccionados!</p>
            <a href="#products" class="button">Aprovecha</a>
        </div>
        <div class="banner">
            <h3>Envío Gratis</h3>
            <p>En compras superiores a S/.200</p>
            <a href="#products" class="button">Detalles</a>
        </div>
    </div>

    <!-- Promociones -->
    <div class="promotions">
        <p>¡Compra hoy y obtén un 10% de descuento en tu primera compra!</p>
    </div>

    <!-- Sección de filosofía -->
    <section id="philosophy">
        <h2>Nuestra Filosofía</h2>
        <div class="philosophy fade-in">
            <div class="column">
                <h3>Calidad</h3>
                <p>Nos comprometemos a ofrecer productos de alta calidad que cumplan con las expectativas de nuestras clientas. Cada prenda es seleccionada cuidadosamente para garantizar su durabilidad y estilo.</p>
            </div>
            <div class="column">
                <h3>Sostenibilidad</h3>
                <p>Creemos en la moda responsable. Trabajamos con proveedores que comparten nuestra visión de sostenibilidad, utilizando materiales amigables con el medio ambiente y prácticas de producción éticas.</p>
            </div>
        </div>
    </section>

    <!-- Sección de productos -->
    <section id="products">
        <h2>Nuestros Productos</h2>
        <div class="product-grid">
            <div class="product-card">
                <img src="https://r.mobirisesite.com/864296/assets/images/photo-1519748771451-a94c596fad67.jpeg" alt="Blusa Casual">
                <h3>Blusa Casual</h3>
                <p>S/.80.00</p>
                <button class="button" onclick="addToCart('Blusa Casual', 80)">Agregar al Carrito</button>
            </div>
            <div class="product-card">
                <img src="https://r.mobirisesite.com/864296/assets/images/photo-1532073150508-0c1df022bdd1.jpeg" alt="Pantalones de Moda">
                <h3>Pantalones de Moda</h3>
                <p>S/.90.00</p>
                <button class="button" onclick="addToCart('Pantalones de Moda', 90)">Agregar al Carrito</button>
            </div>
            <div class="product-card">
                <img src="https://r.mobirisesite.com/864296/assets/images/photo-1477144281006-a10123007fba.jpeg" alt="Chaqueta Chic">
                <h3>Chaqueta Chic</h3>
                <p>S/.150.00</p>
                <button class="button" onclick="addToCart('Chaqueta Chic', 150)">Agregar al Carrito</button>
            </div>
            <div class="product-card">
                <img src="https://r.mobirisesite.com/864296/assets/images/photo-1648747066670-034eab81a631.jpeg" alt="Falda Larga">
                <h3>Falda Larga</h3>
                <p>S/.75.00</p>
                <button class="button" onclick="addToCart('Falda Larga', 75)">Agregar al Carrito</button>
            </div>
            <div class="product-card">
                <img src="https://r.mobirisesite.com/864296/assets/images/photo-1496747611176-843222e1e57c.jpeg" alt="Camiseta Divertida">
                <h3>Camiseta Divertida</h3>
                <p>S/.45.00</p>
                <button class="button" onclick="addToCart('Camiseta Divertida', 45)">Agregar al Carrito</button>
            </div>
            <div class="product-card">
                <img src="https://r.mobirisesite.com/864296/assets/images/photo-1551489186-ccb95a1ea6a3.jpeg" alt="Pantalones Cortos">
                <h3>Pantalones Cortos</h3>
                <p>S/.60.00</p>
                <button class="button" onclick="addToCart('Pantalones Cortos', 60)">Agregar al Carrito</button>
            </div>
            <div class="product-card">
                <img src="https://r.mobirisesite.com/864296/assets/images/photo-1506152983158-b4a74a01c721.jpeg" alt="Abrigo de Invierno">
                <h3>Abrigo de Invierno</h3>
                <p>S/.200.00</p>
                <button class="button" onclick="addToCart('Abrigo de Invierno', 200)">Agregar al Carrito</button>
            </div>
            <div class="product-card">
                <img src="https://r.mobirisesite.com/864296/assets/images/photo-1508427953056-b00b8d78ebf5.jpeg" alt="Mono Estiloso">
                <h3>Mono Estiloso</h3>
                <p>S/.130.00</p>
                <button class="button" onclick="addToCart('Mono Estiloso', 130)">Agregar al Carrito</button>
            </div>
            <div class="product-card">
                <img src="https://r.mobirisesite.com/864296/assets/images/photo-1486308510493-aa64833637bc.jpeg" alt="Blazer Moderno">
                <h3>Blazer Moderno</h3>
                <p>S/.110.00</p>
                <button class="button" onclick="addToCart('Blazer Moderno', 110)">Agregar al Carrito</button>
            </div>
        </div>
    </section>

   <section id="contacto" style="padding: 4rem 0; text-align: center; background-color: #fce4ec;">
    <h2 style="color: #e91e63; margin-bottom: 2rem;">Contáctanos</h2>
    <form style="max-width: 600px; margin: auto; display: flex; flex-direction: column;">
        <label for="nombre" style="margin-bottom: 0.5rem; text-align: left;">Nombre:</label>
        <input type="text" id="nombre" name="nombre" required placeholder="Tu nombre" 
               style="padding: 0.7rem; margin-bottom: 1rem; border: 1px solid #ddd; border-radius: 5px;">
        
        <label for="email" style="margin-bottom: 0.5rem; text-align: left;">Correo Electrónico:</label>
        <input type="email" id="email" name="email" required placeholder="Tu correo electrónico" 
               style="padding: 0.7rem; margin-bottom: 1rem; border: 1px solid #ddd; border-radius: 5px;">
        
        <label for="mensaje" style="margin-bottom: 0.5rem; text-align: left;">Mensaje:</label>
        <textarea id="mensaje" name="mensaje" required placeholder="Tu mensaje" rows="5"
                  style="padding: 0.7rem; margin-bottom: 1rem; border: 1px solid #ddd; border-radius: 5px;"></textarea>
        
        <button type="submit" style="background-color: #e91e63; color: #fff; padding: 0.7rem; border: none; border-radius: 5px; cursor: pointer;">
            Enviar Mensaje
        </button>
    </form>
</section>
 <section id="redes-sociales" style="padding: 2rem 0; text-align: center; background-color: #fce4ec;">
    <h2 style="color: #e91e63; margin-bottom: 1rem;">Síguenos en Redes Sociales</h2>
    <div style="display: flex; justify-content: center; gap: 2rem;">
        <a href="https://www.facebook.com/tu-perfil" target="_blank" style="text-decoration: none;">
            <img src="https://img.icons8.com/fluency/48/000000/facebook-new.png" alt="Facebook" style="width: 48px; height: 48px;">
        </a>
        <a href="https://www.instagram.com/tu-perfil" target="_blank" style="text-decoration: none;">
            <img src="https://img.icons8.com/fluency/48/000000/instagram-new.png" alt="Instagram" style="width: 48px; height: 48px;">
        </a>
        <a href="https://twitter.com/tu-perfil" target="_blank" style="text-decoration: none;">
            <img src="https://img.icons8.com/fluency/48/000000/twitter.png" alt="Twitter" style="width: 48px; height: 48px;">
        </a>
        <a href="https://www.linkedin.com/in/tu-perfil" target="_blank" style="text-decoration: none;">
            <img src="https://img.icons8.com/fluency/48/000000/linkedin.png" alt="LinkedIn" style="width: 48px; height: 48px;">
        </a>
    </div>
</section>

    <section id="marcas-aliadas" style="padding: 2rem 0; text-align: center; background-color: #f3f4f6;">
    <h2 style="color: #333; margin-bottom: 1rem;">Nuestras Marcas Aliadas</h2>
    <div style="display: flex; justify-content: center; flex-wrap: wrap; gap: 2rem;">
        <img src="ruta/logo1.png" alt="Marca 1" style="width: 150px; height: auto;">
        <img src="ruta/logo2.png" alt="Marca 2" style="width: 150px; height: auto;">
        <img src="ruta/logo3.png" alt="Marca 3" style="width: 150px; height: auto;">
        <img src="ruta/logo4.png" alt="Marca 4" style="width: 150px; height: auto;">
        <img src="ruta/logo5.png" alt="Marca 5" style="width: 150px; height: auto;">
    </div>
</section>

    <!-- Pie de página -->
    <footer>
        <p>&copy; 2024 Modaz. Todos los derechos reservados.</p>
    </footer>

    <script>
        let cart = [];

        function addToCart(productName, price) {
            const product = { name: productName, price: price };
            cart.push(product);
            updateCart();
        }

        function updateCart() {
            const cartContent = document.getElementById('cart-content');
            const cartCount = document.getElementById('cart-count');
            cartContent.innerHTML = ''; // Limpiar el contenido actual

            cart.forEach(item => {
                const div = document.createElement('div');
                div.classList.add('cart-item');
                div.innerHTML = `<p>${item.name} - S/.${item.price.toFixed(2)}</p>
                                <button onclick="removeFromCart('${item.name}')">Eliminar</button>`;
                cartContent.appendChild(div);
            });

            cartCount.innerText = cart.length;
        }

        function removeFromCart(productName) {
            cart = cart.filter(item => item.name !== productName);
            updateCart();
        }

        function toggleCart() {
            const cartItems = document.getElementById('cart-items');
            cartItems.style.display = cartItems.style.display === 'block' ? 'none' : 'block';
        }
    </script>

</body>

</html>
 
  
  
  
  
  
  
