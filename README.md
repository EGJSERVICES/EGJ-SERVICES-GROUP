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
    /* Base styles and transitions */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, white, lightblue);
      color: #333;
      margin: 0;
      padding: 0;
      transition: background 0.3s, color 0.3s;
    }
    body.dark-mode {
      background: #1a1a1a;
      color: #f0f0f0;
    }
    /* Header */
    header {
      background: rgba(255, 255, 255, 0.9);
      padding: 15px;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      transition: background 0.3s;
    }
    body.dark-mode header {
      background: rgba(18, 18, 18, 0.9);
    }
    .logo {
      font-size: 28px;
      font-weight: bold;
    }
    nav ul {
      list-style: none;
      display: flex;
      flex-wrap: wrap;
      margin: 0;
      padding: 0;
    }
    nav ul li {
      margin: 0 15px;
    }
    nav ul li a {
      text-decoration: none;
      color: inherit;
      font-size: 18px;
      transition: color 0.3s;
    }
    nav ul li a:hover {
      color: #007BFF;
    }
    .search-bar {
      margin-top: 10px;
    }
    .search-bar input {
      padding: 10px;
      width: 200px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .search-bar button {
      padding: 10px 15px;
      border: none;
      background: #007BFF;
      color: white;
      border-radius: 5px;
      margin-left: 10px;
      cursor: pointer;
      transition: background 0.3s, transform 0.3s;
    }
    .search-bar button:hover {
      background: #0056b3;
      transform: scale(1.05);
    }
    .dark-mode .search-bar button {
      background: #1e88e5;
    }
    .dark-mode .search-bar button:hover {
      background: #1565c0;
    }
    .dark-mode-toggle {
      background: #007BFF;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
      font-weight: bold;
      transition: background 0.3s;
      margin-top: 10px;
    }
    .dark-mode-toggle:hover {
      background: #0056b3;
    }
    /* Hero Section */
    .hero {
      position: relative;
      text-align: center;
      padding: 100px 20px;
      background: url('images/construction-site-background.jpg') no-repeat center center/cover;
      color: white;
    }
    .hero::before {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0, 0, 0, 0.5);
      z-index: 1;
    }
    .hero > * {
      position: relative;
      z-index: 2;
    }
    .hero h1 {
      font-size: 48px;
      margin-bottom: 20px;
      transition: color 0.3s;
    }
    body.dark-mode .hero h1 {
      color: #fff;
    }
    .hero p {
      font-size: 24px;
      margin-bottom: 30px;
    }
    .btn {
      background: #007BFF;
      color: white;
      padding: 15px 30px;
      text-decoration: none;
      border-radius: 8px;
      font-size: 20px;
      font-weight: bold;
      box-shadow: 3px 3px 15px rgba(0,0,0,0.2);
      transition: background 0.3s, transform 0.3s;
    }
    .btn:hover {
      background: #0056b3;
      transform: translateY(-3px);
    }
    /* Dynamic boxes for sections */
    .dynamic-box {
      background: rgba(255, 255, 255, 0.8);
      padding: 40px;
      margin: 30px auto;
      border-radius: 8px;
      width: 90%;
      max-width: 1200px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      transition: transform 0.3s, background 0.3s;
    }
    .dark-mode .dynamic-box {
      background: rgba(50, 50, 50, 0.9);
    }
    .dynamic-box h2 {
      font-size: 32px;
      margin-bottom: 20px;
      transition: color 0.3s;
    }
    body.dark-mode .dynamic-box h2 {
      color: #fff;
    }
    /* Service Cards */
    .service-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
    }
    .service-card {
      background: white;
      padding: 20px;
      border-radius: 8px;
      width: 30%;
      margin: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      text-align: center;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .service-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    }
    .service-card img {
      max-width: 100%;
      border-radius: 8px;
      margin-bottom: 15px;
    }
    /* Google Map */
    #google-map {
      width: 100%;
      height: 400px;
      border: none;
      border-radius: 8px;
    }
    /* Footer */
    footer {
      text-align: center;
      padding: 20px;
      background: #007BFF;
      color: white;
      transition: background 0.3s;
    }
    /* Responsive styles */
    @media (max-width: 768px) {
      .service-card {
        width: 90%;
      }
      nav ul li {
        margin: 0 10px;
      }
      .search-bar input {
        width: 150px;
      }
    }
  </style>
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
    <button class="dark-mode-toggle" onclick="toggleDarkMode()">Toggle Dark Mode</button>
    <div class="search-bar">
      <input type="text" placeholder="Search...">
      <button><i class="fas fa-search"></i></button>
    </div>
  </header>

  <section class="hero dynamic-box">
    <h1>Reliable Construction Transportation Services</h1>
    <p>Serving Palm Beach, St. Lucie, and Broward Counties.</p>
    <a href="#contact" class="btn">Request a Quote</a>
  </section>

  <section id="services" class="dynamic-box">
    <h2>Our Services</h2>
    <p>We provide all kinds of aggregates, dirt, sand, trash, C&amp;D, and hourly projects.</p>
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

  <section id="map" class="dynamic-box">
    <h2>Our Service Areas</h2>
    <div id="google-map"></div>
  </section>

  <section id="contact" class="dynamic-box">
    <h2>Contact Us</h2>
    <p>Email: egjttrucking@gmail.com</p>
    <p>Phone: 5615068932</p>
    <p>Address: PO BOX 17017, West Palm Beach, FL 33416</p>
  </section>

  <footer>
    <p>&copy; 2025 EGJ Services Group. All rights reserved.</p>
  </footer>

  <script>
    function toggleDarkMode() {
      document.body.classList.toggle('dark-mode');
    }
    function initMap() {
      var location = { lat: 26.7153, lng: -80.0534 };
      var map = new google.maps.Map(document.getElementById('google-map'), {
        zoom: 10,
        center: location,
      });
      var marker = new google.maps.Marker({
        position: location,
        map: map
      });
    }
  </script>
  <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>
</body>
</html>