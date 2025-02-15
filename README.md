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
            background: linear-gradient(to right, white, lightblue);
            color: #333;
            margin: 0;
            padding: 0;
            transition: background 0.3s, color 0.3s;
        }
        body.dark-mode {
            background: #121212;
            color: #fff;
        }
        header {
            background: rgba(255, 255, 255, 0.9);
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo img {
            height: 60px;
        }
        nav ul {
            list-style: none;
            display: flex;
        }
        nav ul li {
            margin: 0 20px;
        }
        .search-bar input {
            padding: 10px;
            width: 250px;
        }
        .hero {
            text-align: center;
            padding: 80px 20px;
            background: rgba(0, 0, 0, 0.5);
            color: white;
            font-size: 1.5em;
        }
        .btn {
            background: lightblue;
            color: white;
            padding: 15px 30px;
            font-size: 1.2em;
            text-decoration: none;
            border-radius: 8px;
        }
        .btn:hover {
            background: darkblue;
        }
        .service-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            padding: 20px;
        }
        .service-card {
            background: white;
            padding: 25px;
            border-radius: 8px;
            width: 30%;
            margin: 15px;
            box-shadow: 0px 0px 15px gray;
        }
        footer {
            text-align: center;
            padding: 20px;
            background: lightblue;
            color: white;
        }
        .dark-mode-toggle {
            position: fixed;
            top: 10px;
            right: 10px;
            background: black;
            color: white;
            padding: 10px 15px;
            cursor: pointer;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="dark-mode-toggle" onclick="toggleDarkMode()">Dark Mode</div>
    <header>
        <div class="logo"><img src="images/logo.png" alt="EGJ Services Group"></div>
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
        <h1>Reliable Construction Transportation Services</h1>
        <p>Serving Palm Beach, St. Lucie, and Broward Counties.</p>
        <a href="#contact" class="btn">Request a Quote</a>
    </section>

    <section id="services">
        <h2>Our Services</h2>
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
        <p>We are the trusted partner for any project in South Florida, specializing in all kinds of aggregates, dirt, sand, trash, C&D, and hourly projects.</p>
    </section>

    <section id="map">
        <h2>Our Service Areas</h2>
        <div id="google-map" style="width:100%;height:400px;"></div>
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

        function toggleDarkMode() {
            document.body.classList.toggle("dark-mode");
        }
    </script>
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>
</body>
</html>
