<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EGJ SERVICES GROUP - Professional Trucking Services</title>
  <style>
    /* Global Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    /* Base Styles */
    body {
      font-family: Arial, sans-serif;
      background: url('https://source.unsplash.com/1600x900/?construction,truck') no-repeat center center fixed;
      background-size: cover;
      color: #333;
      line-height: 1.6;
    }
    a {
      text-decoration: none;
      color: inherit;
    }
    .container {
      max-width: 1300px;
      margin: auto;
      padding: 20px;
    }
    /* Navigation Bar */
    .navbar {
      background: #1e3a5f;
      color: #fff;
      padding: 15px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .navbar .logo {
      font-size: 2em;
      font-weight: bold;
    }
    .navbar ul {
      list-style: none;
      display: flex;
    }
    .navbar ul li {
      margin: 0 15px;
    }
    .navbar ul li a {
      color: #fff;
      font-size: 1.2em;
      transition: color 0.3s;
    }
    .navbar ul li a:hover {
      color: #FFD700;
    }
    /* Header Section */
    .header {
      text-align: center;
      padding: 60px 20px;
      background: rgba(0, 0, 0, 0.6);
      color: #fff;
      border-radius: 10px;
      margin-bottom: 20px;
    }
    .header h1 {
      font-size: 3em;
      margin-bottom: 10px;
    }
    .header p {
      font-size: 1.4em;
      margin-bottom: 20px;
    }
    /* Services Section */
    .section {
      background: #fff;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      margin-bottom: 20px;
      text-align: center;
    }
    .section h2 {
      color: #1e3a5f;
      margin-bottom: 15px;
    }
    /* Contact Section */
    .contact {
      text-align: center;
      background: #1e3a5f;
      color: #fff;
      padding: 20px;
      border-radius: 10px;
    }
    /* Map */
    .map-container {
      width: 100%;
      height: 400px;
      margin-top: 20px;
    }
    /* Footer */
    .footer {
      text-align: center;
      padding: 20px;
      background: #1e3a5f;
      color: #fff;
      border-radius: 10px;
      margin-top: 20px;
    }
    /* Responsive */
    @media (max-width: 768px) {
      .navbar ul {
        flex-direction: column;
        align-items: center;
      }
      .navbar ul li {
        margin: 10px 0;
      }
    }
  </style>
</head>
<body>
  <!-- Navigation Bar -->
  <nav class="navbar">
    <div class="logo">EGJ SERVICES GROUP</div>
    <ul>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <div class="container">
    <!-- Header Section -->
    <header class="header">
      <h1>Reliable Trucking Services</h1>
      <p>Fast, Transparent, and Competitive Pricing</p>
    </header>
    
    <!-- Services Section -->
    <section id="services" class="section">
      <h2>Our Services</h2>
      <p>We specialize in three-axle truck transportation, hauling aggregates and excess materials across Palm Beach, St. Lucie, and Broward Counties.</p>
    </section>
    
    <!-- Contact Section -->
    <section id="contact" class="contact">
      <h2>Contact Us</h2>
      <p>Email: <a href="mailto:egjttrucking@gmail.com" style="color:yellow;">egjttrucking@gmail.com</a></p>
      <p>Phone: <a href="tel:5615068932" style="color:yellow;">561-506-8932</a></p>
      <p>Address: PO BOX 17017, West Palm Beach, FL 33416</p>
    </section>
    
    <!-- Google Map -->
    <div class="map-container">
      <iframe width="100%" height="100%" frameborder="0" style="border:0" 
        src="https://www.google.com/maps/embed/v1/place?q=West+Palm+Beach,+FL&key=YOUR_GOOGLE_MAPS_API_KEY" allowfullscreen>
      </iframe>
    </div>
    
    <!-- Footer Section -->
    <footer class="footer">
      <p>&copy; 2025 EGJ SERVICES GROUP. All rights reserved.</p>
    </footer>
  </div>
</body>
</html>
