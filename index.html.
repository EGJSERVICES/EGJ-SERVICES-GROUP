<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EGJ Services Group</title>
    <link rel="stylesheet" href="styles.css">
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    <script defer src="script.js"></script>
</head>
<body>
    <header>
        <div class="logo">EGJ Services Group</div>
        <nav>
            <ul>
                <li><a href="#services">Servicios</a></li>
                <li><a href="#about">Sobre Nosotros</a></li>
                <li><a href="#contact">Contacto</a></li>
                <li><a href="#map">Ubicaciones</a></li>
            </ul>
        </nav>
        <div class="search-bar">
            <input type="text" placeholder="Buscar...">
            <button><i class="fas fa-search"></i></button>
        </div>
    </header>

    <section class="hero">
        <div class="overlay"></div>
        <h1>Servicios de Transporte de Construcción Confiables</h1>
        <p>Sirviendo a los condados de Palm Beach, St. Lucie y Broward.</p>
        <a href="#contact" class="btn">Solicitar Cotización</a>
    </section>

    <section id="services">
        <h2>Nuestros Servicios</h2>
        <div class="service-container">
            <div class="service-card">
                <img src="images/dump-truck.jpg" alt="Camión Volquete">
                <h3>Transporte de Materiales</h3>
                <p>Transportamos agregados, relleno, concreto, asfalto y más.</p>
            </div>
            <div class="service-card">
                <img src="images/construction-site.jpg" alt="Sitio de Construcción">
                <h3>Entregas en Obra</h3>
                <p>Entrega rápida y eficiente para mantener su proyecto en marcha.</p>
            </div>
            <div class="service-card">
                <img src="images/machine-work.jpg" alt="Trabajo de Maquinaria">
                <h3>Servicios de Excavación</h3>
                <p>Ofrecemos servicios de excavación y limpieza de terrenos.</p>
            </div>
        </div>
    </section>

    <section id="about">
        <h2>Sobre EGJ Services Group</h2>
        <p>Especializados en transporte con camiones de tres ejes, aseguramos entregas rápidas, servicio excepcional y precios competitivos.</p>
    </section>

    <section id="map">
        <h2>Nuestras Áreas de Servicio</h2>
        <div id="google-map"></div>
    </section>

    <section id="contact">
        <h2>Contáctenos</h2>
        <p>Email: egjttrucking@gmail.com</p>
        <p>Teléfono: 561-506-8932</p>
        <p>Dirección: PO BOX 17017, West Palm Beach, FL 33416</p>
    </section>

    <footer>
        <p>&copy; 2025 EGJ Services Group. Todos los derechos reservados.</p>
    </footer>

    <script>
        function initMap() {
            var location = { lat: 26.7153, lng: -80.0534 };
            var map = new google.maps.Map(document.getElementById("google-map"), {
                zoom: 10,
                center: location,
            });
            var marker = new google.maps.Marker({ position: location, map: map });
        }
    </script>
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>
</body>
</html>
/* Estilos Generales */
body {
    margin: 0;
    font-family: Arial, sans-serif;
    color: #333;
}

/* Encabezado */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    background-color: #004080;
    color: #fff;
}

.logo {
    font-size: 1.5em;
    font-weight: bold;
}

nav ul {
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
}

nav ul li {
    margin-left: 20px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
    transition: color 0.3s;
}

nav ul li a:hover {
    color: #ffcc00;
}

.search-bar {
    display: flex;
    align-items: center;
}

.search-bar input {
    padding: 5px;
    border: none;
    border-radius: 3px;
}

.search-bar button {
    background-color: #ffcc00;
    border: none;
    padding: 5px 10px;
    margin-left: 5px;
    border-radius: 3px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.search-bar button:hover {
    background-color: #e6b800;
}

/* Sección Hero */
.hero {
    position: relative;
    background-image: url('images/construction-background.jpg');
    background-size 