<!DOCTYPE html>
<html lang="en">
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
                <li><a href="#services">Services</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#map">Locations</a></li>
            </ul>
        </nav>
        <div class="search-bar">
            <input type="text" placeholder="Search...">
            <button><i class="fas fa-search"></i></button>
        </div>
    </header>
    
    <section class="hero">
        <h1>Reliable Construction Hauling Services</h1>
        <p>Serving Palm Beach, St. Lucie, and Broward Counties.</p>
        <a href="#contact" class="btn">Get a Quote</a>
    </section>
    
    <section id="services">
        <h2>Our Services</h2>
        <div class="service-container">
            <div class="service-card">
                <img src="images/dump-truck.jpg" alt="Dump Truck">
                <h3>Material Hauling</h3>
                <p>We transport aggregates, fill, concrete, asphalt, and more.</p>
            </div>
            <div class="service-card">
                <img src="images/construction-site.jpg" alt="Construction Site">
                <h3>Jobsite Deliveries</h3>
                <p>Fast and efficient delivery to keep your project on track.</p>
            </div>
            <div class="service-card">
                <img src="images/machine-work.jpg" alt="Machinery Work">
                <h3>Excavation Services</h3>
                <p>We provide excavation and land clearing services.</p>
            </div>
        </div>
    </section>
    
    <section id="about">
        <h2>About EGJ Services Group</h2>
        <p>Specializing in three-axle truck transportation, we ensure fast deliveries, exceptional service, and competitive pricing.</p>
    </section>
    
    <section id="map">
        <h2>Our Service Areas</h2>
        <div id="google-map"></div>
    </section>
    
    <section id="contact">
        <h2>Contact Us</h2>
        <p>Email: egjttrucking@gmail.com</p>
        <p>Phone: 561-506-8932</p>
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
