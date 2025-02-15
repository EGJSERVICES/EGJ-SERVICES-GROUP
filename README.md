<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EGJ Services Group</title>
    <link rel="stylesheet" href="styles.css">
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    <script defer src="script.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(to bottom, white, lightblue);
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background: rgba(255, 255, 255, 0.9);
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .dynamic-island {
            position: fixed;
            top: 10px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0, 0, 139, 0.9);
            color: white;
            padding: 10px 20px;
            border-radius: 20px;
            font-size: 18px;
            font-weight: bold;
            animation: fadeIn 2s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .logo {
            display: flex;
            align-items: center;
        }
        .logo img {
            width: 60px;
            height: auto;
            margin-right: 10px;
        }
        .content-container {
            max-width: 1200px;
            margin: auto;
            padding: 0 20px;
        }
        .service-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="dynamic-island">EGJ Services Group - Reliable Hauling Services</div>
    
    <header>
        <div class="logo">
            <img src="images/dump-truck-logo.png" alt="Dump Truck Logo">
            <div>EGJ Services Group</div>
        </div>
        <nav>
            <ul>
                <li><a href="#services">Services</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#map">Locations</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero">
        <h1>Reliable Construction Transportation Services</h1>
        <p>Serving Palm Beach, St. Lucie, and Broward Counties.</p>
        <a href="#contact" class="btn">Request a Quote</a>
    </section>

    <section id="services">
        <h2>Our Services</h2>
        <p>We handle all kinds of aggregates, dirt, sand, trash, C&D (Construction & Demolition), and hourly projects.</p>
        <div class="service-container">
            <div class="service-card">
                <img src="images/dump-truck.jpg" alt="Dump Truck">
                <h3>Material Transportation</h3>
                <p>We transport aggregates, fill, concrete, asphalt, and more.</p>
            </div>
            <div class="service-card">
                <img src="images/construction-site.jpg" alt="Construction Site">
                <h3>On-Site Deliveries</h3>
                <p>Fast and efficient delivery to keep your project moving.</p>
            </div>
            <div class="service-card">
                <img src="images/machine-work.jpg" alt="Machine Work">
                <h3>Excavation Services</h3>
                <p>We offer excavation and land clearing services.</p>
            </div>
        </div>
    </section>

    <section id="about">
        <h2>About EGJ Services Group</h2>
        <p>Specializing in three-axle truck transportation, we ensure fast deliveries, exceptional service, and competitive pricing.</p>
    </section>

    <section id="map">
        <h2>Our Service Areas</h2>
        <div id="google-map" style="width:100%;height:400px;"></div>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <p>Email: <a href="mailto:egjttrucking@gmail.com">egjttrucking@gmail.com</a></p>
        <p>Phone: <a href="tel:5615068932">561-506-8932</a></p>
        <p>Address: PO BOX 17017, West Palm Beach, FL 33416</p>
    </section>

    <footer>
        <p>&copy; 2025 EGJ Services Group. All rights reserved.</p>
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
