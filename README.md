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
      background: url('https://images.unsplash.com/photo-1597262975002-c5c3b14bbd62?auto=format&fit=crop&w=1600&q=80') no-repeat center center fixed;
      background-size: cover;
      color: #333;
      line-height: 1.6;
      overflow-x: hidden;
    }
    a {
      text-decoration: none;
      color: inherit;
    }
    /* Responsive Design */
    .container {
      max-width: 1200px;
      margin: auto;
      padding: 20px;
    }
    .header {
      text-align: center;
      padding: 40px 20px;
      background: rgba(43, 62, 80, 0.8);
      color: #fff;
      border-radius: 10px;
      margin-bottom: 20px;
    }
    .header h1 {
      font-size: 2.5em;
    }
    .map-container {
      width: 100%;
      height: 400px;
      margin-top: 20px;
      border-radius: 10px;
      overflow: hidden;
    }
    .button {
      display: inline-block;
      background: #4b79a1;
      color: #fff;
      padding: 12px 24px;
      border-radius: 5px;
      font-weight: bold;
      transition: background 0.3s;
      margin: 5px;
    }
    .button:hover {
      background: #283e51;
    }
    .materials-gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }
    .materials-gallery img {
      width: 100%;
      border-radius: 10px;
    }
    /* Footer */
    .footer {
      text-align: center;
      padding: 20px;
      background: #4b79a1;
      color: #fff;
      border-radius: 10px;
      margin-top: 20px;
    }
    /* Responsive adjustments */
    @media (max-width: 768px) {
      .header h1 {
        font-size: 2em;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <header class="header">
      <h1>EGJ SERVICES GROUP</h1>
      <p>EGJ Services Group specializes in three-axle truck transportation, hauling aggregates and excess materials across Palm Beach, St. Lucie, and Broward Counties. We ensure fast deliveries, exceptional service, transparency, and competitive pricing. Trust us for efficient and reliable hauling solutions that keep your projects on track!</p>
    </header>
    
    <section class="materials-gallery">
      <img src="https://images.unsplash.com/photo-1563805042-7684e8c0f4b9?auto=format&fit=crop&w=600&q=80" alt="Rocks">
      <img src="https://images.unsplash.com/photo-1592983463969-63f1a0f90b9d?auto=format&fit=crop&w=600&q=80" alt="Sand">
      <img src="https://images.unsplash.com/photo-1574180045827-681f8a1a9622?auto=format&fit=crop&w=600&q=80" alt="Fill">
      <img src="https://images.unsplash.com/photo-1562184647-8f2d2e8d2398?auto=format&fit=crop&w=600&q=80" alt="Concrete">
      <img src="https://images.unsplash.com/photo-1611068240937-60199cfa98f7?auto=format&fit=crop&w=600&q=80" alt="Asphalt">
      <img src="https://images.unsplash.com/photo-1581091870621-2e36c5c874e3?auto=format&fit=crop&w=600&q=80" alt="Millings">
    </section>
    
    <div class="map-container">
      <iframe width="100%" height="100%" frameborder="0" style="border:0" 
      src="https://www.google.com/maps/embed/v1/place?q=West+Palm+Beach,+FL&key=YOUR_GOOGLE_MAPS_API_KEY" allowfullscreen>
      </iframe>
    </div>
    
    <footer class="footer">
      <p>&copy; 2025 EGJ SERVICES GROUP. All rights reserved.</p>
    </footer>
  </div>
</body>
</html>
