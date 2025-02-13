<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EGJ SERVICES GROUP - Professional Trucking Services</title>
  <style>
    /* Global resets and box-sizing */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    /* Base styles for html and body */
    html, body {
      width: 100%;
      height: 100%;
      font-family: Arial, sans-serif;
      /* Lighter gradient for mobile devices */
      background: linear-gradient(to bottom, #f8f8f8, #e0e0e0);
      color: #333;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 20px;
      overflow-x: hidden;
      text-align: center;
    }
    /* Desktop background override: a lighter construction-themed image */
    @media (min-width: 769px) {
      html, body {
        background: url('https://source.unsplash.com/1600x900/?construction,materials,light') no-repeat center center fixed;
        background-size: cover;
      }
    }
    /* Main container */
    .container {
      width: 100%;
      max-width: 1400px;
      padding: 40px;
      background: rgba(255, 255, 255, 0.9);
      border-radius: 10px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin: auto;
      animation: fadeIn 1.5s ease-in-out;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    /* Content sections */
    .content {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      text-align: center;
      width: 100%;
    }
    .section {
      width: 90%;
      max-width: 600px;
      margin: 20px auto;
      padding: 20px;
      background: rgba(240, 240, 240, 0.95);
      border-radius: 10px;
      text-align: center;
      transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
    }
    .section:hover {
      transform: scale(1.02);
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }
    h2 {
      color: #FFA500;
      margin-bottom: 10px;
    }
    p, ul {
      font-size: 18px;
      line-height: 1.8;
      margin-bottom: 10px;
    }
    ul {
      padding-left: 0;
      list-style-position: inside;
    }
    /* Button styles */
    button {
      background-color: #FFA500;
      color: black;
      padding: 12px 24px;
      border: none;
      cursor: pointer;
      font-size: 18px;
      font-weight: bold;
      border-radius: 5px;
      margin-top: 10px;
      width: 100%;
      max-width: 300px;
      transition: background-color 0.3s ease;
    }
    button:hover {
      background-color: #FF8C00;
    }
    /* Footer styles */
    .footer {
      text-align: center;
      padding: 20px;
      width: 100%;
      animation: fadeIn 1s ease-in-out;
      color: #333;
    }
    /* New Construction Materials section images */
    .construction-images img {
      width: 100%;
      max-width: 600px;
      border-radius: 10px;
      margin-bottom: 20px;
      transition: transform 0.3s ease-in-out;
    }
    .construction-images img:hover {
      transform: scale(1.02);
    }
    /* Responsive adjustments */
    @media (max-width: 768px) {
      .section {
        width: 100%;
        max-width: 90%;
      }
      p, ul {
        font-size: 20px;
      }
      button {
        font-size: 20px;
        padding: 14px 28px;
      }
    }
    @media (max-width: 480px) {
      p, ul {
        font-size: 18px;
      }
      button {
        font-size: 18px;
        padding: 12px 24px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Removed duplicated company title -->
    <div class="content">
      <section class="section contact">
        <h2>Contact Us</h2>
        <p>Email: <a href="mailto:egjttrucking@gmail.com">egjttrucking@gmail.com</a></p>
        <p>Phone: <a href="tel:5615068932">561-506-8932</a></p>
        <p>Address: PO BOX 17017, West Palm Beach, FL 33416</p>
        <!-- Additional contact buttons -->
        <button onclick="window.location.href='mailto:egjttrucking@gmail.com'">Email Us</button>
        <button onclick="window.location.href='tel:5615068932'">Call Us</button>
      </section>
      <section class="section services">
        <h2>Our Services</h2>
        <p>EGJ Services Group specializes in high-quality trucking and hauling services using top-tier tri axle dump trucks.</p>
        <button onclick="alert('Request a Service Coming Soon!')">Request a Service</button>
        <button onclick="alert('FAQ Coming Soon!')">Frequently Asked Questions</button>
      </section>
      <section class="section tri-axle-info">
        <h2>Tri Axle Dump Truck Services</h2>
        <!-- Tri Axle Dump Truck image -->
        <img src="https://source.unsplash.com/600x400/?tri-axle,dump-truck" alt="Tri Axle Dump Truck" style="width:100%; border-radius:10px; margin-bottom:20px;">
        <p>Our fleet of tri axle dump trucks is equipped to handle a variety of heavy-duty transportation needs, ensuring efficiency and reliability.</p>
        <h3>Key Benefits:</h3>
        <ul>
          <li>Superior load capacity for transporting bulk materials</li>
          <li>Highly maneuverable, making them ideal for construction sites</li>
          <li>Cost-effective and time-saving for large-scale projects</li>
        </ul>
      </section>
      <section class="section construction-materials">
        <h2>Construction Materials</h2>
        <div class="construction-images">
          <img src="https://source.unsplash.com/600x400/?sand" alt="Sand">
          <img src="https://source.unsplash.com/600x400/?rock" alt="Rock">
          <img src="https://source.unsplash.com/600x400/?crushed,concrete" alt="Crushed Concrete">
        </div>
      </section>
    </div>
    <div class="footer">
      <p>&copy; 2025 EGJ SERVICES GROUP. All rights reserved.</p>
    </div>
  </div>
</body>
</html>