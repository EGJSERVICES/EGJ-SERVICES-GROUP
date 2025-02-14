<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EGJ Services Group</title>
    <link rel="stylesheet" href="styles.css">
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>
</head>
<body>
    <header>
        <h1>EGJ Services Group</h1>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="hero">
        <h2>Your Trusted Partner in Construction Hauling</h2>
    </section>
    
    <section id="about">
        <p>EGJ Services Group specializes in three-axle truck transportation, hauling aggregates and excess materials across Palm Beach, St. Lucie, and Broward Counties. We ensure fast deliveries, exceptional service, transparency, and competitive pricing. Trust us for efficient and reliable hauling solutions that keep your projects on track!</p>
    </section>
    
    <section id="services">
        <h2>Our Services</h2>
        <ul>
            <li>Aggregate Hauling</li>
            <li>Concrete and Asphalt Transport</li>
            <li>Excess Material Removal</li>
        </ul>
    </section>
    
    <section id="map">
        <h2>Our Service Area</h2>
        <div id="map-container"></div>
    </section>
    
    <footer>
        <p>Contact us: egjttrucking@gmail.com | 561-506-8932</p>
        <p>Address: PO BOX 17017, West Palm Beach, FL 33416</p>
    </footer>
    
    <script>
        function initMap() {
            var location = { lat: 26.7153, lng: -80.0534 };
            var map = new google.maps.Map(document.getElementById("map-container"), {
                zoom: 10,
                center: location
            });
            var marker = new google.maps.Marker({ position: location, map: map });
        }
    </script>
</body>
</html>
