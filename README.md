<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="description" content="EGJ Services Group – Leading trucking services in South Florida. We specialize in three-axle truck transportation, hauling aggregates, and more." />
  <meta name="keywords" content="trucking, construction, dump truck, hauling, aggregates, South Florida" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>EGJ Services Group | Professional Trucking Services</title>
  <!-- External CSS -->
  <link rel="stylesheet" href="styles.css" />
  <!-- Font Awesome for icons -->
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <!-- Google Maps API -->
  <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY"></script>
  <!-- jsPDF for PDF generation -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <!-- Custom JavaScript -->
  <script defer src="script.js"></script>
  <style>
    /* ========== CSS Variables for Theme Colors ========== */
    :root {
      --bg-color: #f5f5f5;
      --text-color: #333;
      --nav-bg: #f0f0f0;
      --nav-border: #add8e6;
      --btn-bg: #007BFF;
      --btn-hover-bg: #0056b3;
      --content-bg: #ffffff;
      --header-bg: rgba(255, 255, 255, 0.95);
      --modal-bg: #ffffff;
      --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
    body.dark-mode {
      --bg-color: #121212;
      --text-color: #f0f0f0;
      --nav-bg: #222;
      --nav-border: #444;
      --btn-bg: #1E90FF;
      --btn-hover-bg: #1C86EE;
      --content-bg: #1e1e1e;
      --header-bg: rgba(18, 18, 18, 0.95);
      --modal-bg: #1e1e1e;
      --shadow: 0 4px 6px rgba(255, 255, 255, 0.1);
    }
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }
    body {
      background-color: var(--bg-color);
      color: var(--text-color);
      transition: background-color 0.3s, color 0.3s;
    }
    header {
      background: var(--header-bg);
      padding: 1.5rem;
      text-align: center;
      font-size: 1.8rem;
      font-weight: bold;
      box-shadow: var(--shadow);
    }
    nav {
      background: var(--nav-bg);
      padding: 1rem;
      text-align: center;
      border-bottom: 2px solid var(--nav-border);
    }
    nav .btn {
      margin: 0 10px;
      padding: 12px 24px;
      font-size: 1rem;
      text-decoration: none;
      color: var(--text-color);
      background: var(--btn-bg);
      border-radius: 5px;
      transition: background 0.3s;
    }
    nav .btn:hover {
      background: var(--btn-hover-bg);
    }
    .container {
      max-width: 1100px;
      margin: 20px auto;
      padding: 25px;
      background: var(--content-bg);
      box-shadow: var(--shadow);
      border-radius: 10px;
    }
    .btn {
      display: inline-block;
      padding: 12px 24px;
      background: var(--btn-bg);
      color: white;
      border: none;
      cursor: pointer;
      transition: background 0.3s;
      border-radius: 5px;
      font-size: 1rem;
      text-decoration: none;
    }
    .btn:hover {
      background: var (--btn-hover-bg);
    }
    section {
      margin-bottom: 20px;
    }
    #map {
      width: 100%;
      height: 400px;
      margin-top: 20px;
      border-radius: 10px;
    }
    footer {
      background: var(--nav-bg);
      padding: 1rem;
      text-align: center;
      border-top: 2px solid var(--nav-border);
      margin-top: 20px;
    }
    footer p {
      margin: 5px 0;
    }
  </style>
</head>
<body>
  <header>
    EGJ Services Group
  </header>
  <nav>
    <a href="#services" class="btn">Services</a>
    <a href="#about" class="btn">About Us</a>
    <a href="#contact" class="btn">Contact</a>
  </nav>
  <div class="container">
    <section id="services">
      <h2>Our Services</h2>
      <p>We specialize in three-axle truck transportation, hauling aggregates, and more. Our fleet is equipped to handle projects of any size, ensuring timely and efficient delivery.</p>
    </section>
    <section id="about">
      <h2>About Us</h2>
      <p>EGJ Services Group is a leading provider of trucking services in South Florida. With years of experience, we are committed to delivering exceptional service and building lasting relationships with our clients.</p>
    </section>
    <section id="contact">
      <h2>Contact Us</h2>
      <p><strong>Email:</strong> <a href="mailto:EGJTTRUCKING@GMAIL.COM">EGJTTRUCKING@GMAIL.COM</a></p>
      <p><strong>Phone:</strong> <a href="tel:5615068932">561-506-8932</a></p>
      <p><strong>Address:</strong> 17017 West Palm Beach, FL 33416</p>
      <div id="map"></div>
    </section>
  </div>
  <footer>
    <p>&copy; 2025 EGJ Services Group. All rights reserved.</p>
  </footer>
  <script>
    function initMap() {
      var location = { lat: 26.7153, lng: -80.0534 }; // Coordinates for West Palm Beach, FL
      var map = new google.maps.Map(document.getElementById('map'), {
        center: location,
        zoom: 12
      });
      var marker = new google.maps.Marker({
        
