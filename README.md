<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>EGJ Services Group</title>
  <link rel="stylesheet" href="styles.css" />
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <!-- Include jsPDF for PDF generation -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <script defer src="script.js"></script>
  <style>
    /* Base Styles and Transitions */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    html, body {
      width: 100%;
      height: 100%;
    }
    body {
      font-family: Arial, sans-serif;
      /* New construction-inspired gradient background */
      background: linear-gradient(to right, #003366, #336699);
      color: #333;
      margin: 0;
      padding: 0;
      transition: background 0.3s, color 0.3s;
      font-size: 12px;
      line-height: 1.5;
    }
    body.dark-mode {
      background: #1a1a1a;
      color: #f0f0f0;
    }
    p {
      text-align: justify;
      margin: 10px 0;
    }
    /* Top Bar: Contains the digital clock (with watch icon) and static company location */
    .topbar {
      position: fixed;
      top: 0;
      right: 0;
      width: 100%;
      display: flex;
      justify-content: flex-end;
      align-items: center;
      padding: 5px 15px;
      background: #007BFF;
      color: white;
      font-size: 14px;
      z-index: 1000;
    }
    .watch-container {
      display: flex;
      align-items: center;
      margin-right: 10px;
    }
    .watch-container img {
      width: 30px;
      height: 30px;
      margin-right: 5px;
    }
    .clockwatch {
      border: 2px solid white;
      border-radius: 50%;
      padding: 5px 10px;
      font-size: 14px;
      font-weight: bold;
    }
    .company-location {
      font-size: 14px;
      font-weight: bold;
    }
    /* Header */
    header {
      background: rgba(255, 255, 255, 0.9);
      padding: 15px;
      display: flex;
      flex-direction: column;
      align-items: center;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
      transition: background 0.3s;
      margin-top: 50px;
      text-align: center;
    }
    body.dark-mode header {
      background: rgba(18, 18, 18, 0.9);
    }
    .logo {
      font-size: 28px;
      font-weight: bold;
      margin-bottom: 10px;
      color: inherit;
      text-align: center;
    }
    .logo img {
      width: 120px;
      height: auto;
    }
    nav {
      width: 100%;
    }
    nav ul {
      list-style: none;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
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
      text-align: center;
    }
    nav ul li a:hover {
      color: #007BFF;
    }
    /* New "Work With Us" link styling remains the same */
    nav ul li a.workwithus {
      font-weight: bold;
    }
    /* Remove the search bar entirely */
    /* Header Extras: Clock and Navigation already added */
    .darkmodetoggle {
      background: #007BFF;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 0;
      cursor: pointer;
      font-size: 16px;
      font-weight: bold;
      transition: background 0.3s;
      margin-top: 10px;
    }
    .darkmodetoggle:hover {
      background: #0056b3;
    }
    /* Hero Section */
    .hero {
      position: relative;
      text-align: center;
      padding: 100px 20px;
      background: url('images/constructionsitebackground.jpg') no-repeat center center/cover;
      color: white;
    }
    .hero::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
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
      text-align: center;
    }
    body.dark-mode .hero h1 {
      color: #fff;
    }
    .hero p {
      font-size: 24px;
      margin-bottom: 30px;
      text-align: center;
    }
    .btn {
      background: #007BFF;
      color: white;
      padding: 15px 30px;
      text-decoration: none;
      border-radius: 0;
      font-size: 20px;
      font-weight: bold;
      box-shadow: 3px 3px 15px rgba(0, 0, 0, 0.2);
      transition: background 0.3s, transform 0.3s, box-shadow 0.3s;
      text-align: center;
      margin: 10px;
    }
    .btn:hover {
      background: #0056b3;
      transform: translateY(-3px) scale(1.15);
      box-shadow: 5px 5px 20px rgba(0, 0, 0, 0.3);
    }
    /* Dynamic Boxes for Sections */
    .dynamicbox {
      background: rgba(255, 255, 255, 0.8);
      padding: 40px;
      margin: 30px 0;
      border-radius: 0;
      width: 100%;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s, background 0.3s;
      text-align: center;
    }
    .dark-mode .dynamicbox {
      background: rgba(50, 50, 50, 0.9);
    }
    .dynamicbox h2 {
      font-size: 32px;
      margin-bottom: 20px;
      transition: color 0.3s;
      text-align: center;
    }
    body.dark-mode .dynamicbox h2 {
      color: #fff;
    }
    .dynamicbox p {
      margin: 10px 0;
      text-align: justify;
    }
    /* Service Cards */
    .servicecontainer {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
    }
    .servicecard {
      background: white;
      padding: 20px;
      border-radius: 0;
      width: 30%;
      margin: 15px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      text-align: center;
      transition: transform 0.3s, box-shadow 0.3s;
      cursor: pointer;
    }
    .servicecard:hover {
      transform: translateY(-5px) scale(1.15);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
    }
    .servicecard img {
      max-width: 100%;
      border-radius: 0;
      margin-bottom: 15px;
    }
    .description {
      display: none;
      text-align: left;
      padding: 10px;
      border-top: 1px solid #ccc;
      margin-top: 10px;
    }
    /* Materials Section */
    .materialscontainer {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      margin-top: 20px;
    }
    .materialcard {
      background: white;
      padding: 15px;
      margin: 15px;
      border-radius: 0;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      width: 22%;
      text-align: center;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .materialcard:hover {
      transform: translateY(-5px) scale(1.15);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
    }
    .materialcard img {
      max-width: 100%;
      border-radius: 0;
      margin-bottom: 10px;
    }
    /* FAQ Section */
    .faqcontainer {
      margin-top: 20px;
      text-align: justify;
    }
    .faqitem {
      background: white;
      padding: 20px;
      margin: 10px 0;
      border-radius: 0;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .faqitem:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
    }
    .faqitem h3 {
      font-size: 22px;
      margin-bottom: 10px;
    }
    .faqitem p {
      font-size: 18px;
    }
    /* Review Section */
    .reviewcontainer {
      margin-top: 20px;
      text-align: justify;
    }
    .reviewitem {
      background: white;
      padding: 20px;
      margin: 10px 0;
      border-radius: 0;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .reviewitem:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
    }
    .reviewform {
      margin-top: 20px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .reviewform textarea {
      padding: 10px;
      resize: vertical;
      min-height: 80px;
      border: 1px solid #ccc;
      border-radius: 0;
      margin-bottom: 10px;
      width: 90%;
      max-width: 600px;
    }
    .reviewform button {
      padding: 10px 15px;
      border: none;
      background: #007BFF;
      color: white;
      border-radius: 0;
      cursor: pointer;
      transition: background 0.3s, transform 0.3s;
    }
    .reviewform button:hover {
      background: #0056b3;
      transform: scale(1.05);
    }
    /* Google Map */
    #googlemap {
      width: 100%;
      height: 400px;
      border: none;
      border-radius: 0;
    }
    /* Contact Section */
    #contact {
      margin-top: 20px;
    }
    /* Footer */
    footer {
      text-align: center;
      padding: 20px;
      background: #007BFF;
      color: white;
      transition: background 0.3s;
    }
    /* Responsive Styles */
    @media (max-width: 768px) {
      .servicecard, .materialcard {
        width: 90%;
      }
      nav ul li {
        margin: 0 10px;
      }
      .searchbar input {
        width: 150px;
      }
      .materialcard {
        width: 45%;
      }
    }
  </style>
</head>
<body>
  <!-- Top Bar with Digital Clock and Company Location -->
  <div class="topbar" id="topbar">
    <div class="watch-container">
      <img src="images/watch.png" alt="Watch" class="watch-image" />
      <div class="clockwatch" id="companyclock"></div>
    </div>
    <span class="company-location">West Palm Beach, FL</span>
  </div>
  
  <header>
    <div class="logo" style="text-align:center;"><img src="images/logo.png" alt="Logo" /></div>
    <nav>
      <ul>
        <li><a href="#services" class="redirect-button" data-target="services">Services</a></li>
        <li><a href="#about" class="redirect-button" data-target="about">About Us</a></li>
        <li><a href="#contact" class="redirect-button" data-target="contact">Contact</a></li>
        <li><a href="#map" class="redirect-button" data-target="map">Locations</a></li>
        <li><a href="#workwithus" class="redirect-button" data-target="workwithus">Work With Us</a></li>
      </ul>
    </nav>
    <button class="darkmodetoggle" onclick="toggleDarkMode()">Toggle Dark Mode</button>
  </header>
  
  <section class="hero dynamicbox">
    <h1>Reliable Construction Transportation Services</h1>
    <p>Serving Palm Beach, St Lucie, and Broward Counties.</p>
    <a href="#" class="btn redirect-button" data-target="contact">Request a Quote</a>
  </section>
  
  <section id="services" class="dynamicbox">
    <h2>Our Services</h2>
    <p>We provide all kinds of aggregates, dirt, sand, trash, C&amp;D, and hourly projects.</p>
    <div class="servicecontainer">
      <div class="servicecard" onclick="toggleDescription(this)">
        <img src="images/dumptruck.jpg" alt="Dump Truck" />
        <div class="description">
          <h3>Material Transportation</h3>
          <p>We transport aggregates, fill, concrete, asphalt, and more.</p>
        </div>
      </div>
      <div class="servicecard" onclick="toggleDescription(this)">
        <img src="images/constructionsite.jpg" alt="Construction Site" />
        <div class="description">
          <h3>On Site Deliveries</h3>
          <p>Fast and efficient delivery to keep your project moving.</p>
        </div>
      </div>
      <div class="servicecard" onclick="toggleDescription(this)">
        <img src="images/machinework.jpg" alt="Machine Work" />
        <div class="description">
          <h3>Excavation Services</h3>
          <p>We offer excavation and land clearing services.</p>
        </div>
      </div>
    </div>
  </section>
  
  <section id="materials" class="dynamicbox">
    <h2>Construction Materials</h2>
    <div class="materialscontainer">
      <div class="materialcard">
        <img src="images/concrete.jpg" alt="Concrete" />
        <h3>Concrete</h3>
      </div>
      <div class="materialcard">
        <img src="images/asphalt.jpg" alt="Asphalt" />
        <h3>Asphalt</h3>
      </div>
      <div class="materialcard">
        <img src="images/fill.jpg" alt="Fill" />
        <h3>Fill</h3>
      </div>
      <div class="materialcard">
        <img src="images/sand.jpg" alt="Sand" />
        <h3>Sand</h3>
      </div>
    </div>
  </section>
  
  <section id="map" class="dynamicbox">
    <h2>Our Service Areas</h2>
    <div id="googlemap"></div>
  </section>
  
  <section id="faq" class="dynamicbox">
    <h2>Frequently Asked Questions</h2>
    <div class="faqcontainer">
      <div class="faqitem">
        <h3>What services do you provide?</h3>
        <p>We offer material transportation, on site deliveries, and excavation services. We handle aggregates, dirt, sand, trash, C&amp;D, and hourly projects.</p>
      </div>
      <div class="faqitem">
        <h3>Why choose us?</h3>
        <p>We are the trusted partner for any project in South Florida with decades of experience and a commitment to reliability and efficiency.</p>
      </div>
      <div class="faqitem">
        <h3>How can I get a quote?</h3>
        <p>You can request a quote by clicking on the “Request a Quote” button or contacting us directly.</p>
      </div>
      <div class="faqitem">
        <h3>What is your typical project size?</h3>
        <p>Our projects vary from small local jobs to large-scale construction projects. We tailor our services to your specific needs.</p>
      </div>
      <div class="faqitem">
        <h3>What are your payment terms?</h3>
        <p>We offer competitive pricing with flexible payment terms. Please contact us for detailed information.</p>
      </div>
    </div>
  </section>
  
  <section id="reviews" class="dynamicbox">
    <h2>Reviews</h2>
    <div class="reviewcontainer" id="reviewcontainer">
      <div class="reviewitem">
        <p>Great service and fast delivery. Highly recommended!</p>
        <p><strong>John Doe</strong></p>
      </div>
      <div class="reviewitem">
        <p>Reliable and efficient. The best trucking service in South Florida.</p>
        <p><strong>Jane Smith</strong></p>
      </div>
    </div>
    <div class="reviewform">
      <textarea id="reviewtext" placeholder="Leave your review here..."></textarea>
      <button id="submitreview">Submit Review</button>
    </div>
  </section>
  
  <section id="about" class="dynamicbox">
    <h2>About Us</h2>
    <p>EGJ Services Group specializes in three axle truck transportation, hauling aggregates and excess materials across Palm Beach, St Lucie, and Broward Counties. We ensure fast deliveries, exceptional service, transparency, and competitive pricing. Trust us for efficient and reliable hauling solutions that keep your projects on track!</p>
    <p>With decades of industry experience, our state-of-the-art fleet and expert drivers guarantee timely and secure transportation. Our commitment to safety, customer satisfaction, and innovation has made us the leading trucking partner in South Florida.</p>
  </section>
  
  <section id="contact" class="dynamicbox">
    <h2>Contact Us</h2>
    <p>Email: <a href="mailto:egjttrucking@gmail.com">egjttrucking@gmail.com</a></p>
    <p>Phone: <a href="tel:5615068932">5615068932</a></p>
    <p>Address: PO BOX 17017, West Palm Beach, FL 33416</p>
  </section>
  
  <!-- Hidden Section for "Work With Us" Form -->
  <section id="workwithus" class="dynamicbox" style="display: none; text-align: left;">
    <h2>Work With Us</h2>
    <form id="serviceForm">
      <div style="margin-bottom: 10px;">
        <label for="name"><strong>Name:</strong></label><br />
        <input type="text" id="name" name="name" required style="width: 100%;" />
      </div>
      <div style="margin-bottom: 10px;">
        <label for="phone"><strong>Phone:</strong></label><br />
        <input type="tel" id="phone" name="phone" required style="width: 100%;" />
      </div>
      <div style="margin-bottom: 10px;">
        <label for="email"><strong>Email:</strong></label><br />
        <input type="email" id="email" name="email" required style="width: 100%;" />
      </div>
      <div style="margin-bottom: 10px;">
        <label for="address"><strong>Mailing/Billing Address:</strong></label><br />
        <input type="text" id="address" name="address" required style="width: 100%;" />
      </div>
      <div style="margin-bottom: 10px;">
        <label for="companyLocation"><strong>Company Location:</strong></label><br />
        <input type="text" id="companyLocation" name="companyLocation" required style="width: 100%;" />
      </div>
      <div style="margin-bottom: 10px;">
        <label for="companyType"><strong>Type of Company:</strong></label><br />
        <input type="text" id="companyType" name="companyType" required style="width: 100%;" />
      </div>
      <div style="margin-bottom: 10px;">
        <label for="serviceType"><strong>Service Type Requested:</strong></label><br />
        <select id="serviceType" name="serviceType" required style="width: 100%;">
          <option value="Dump Truck Transportation">Dump Truck Transportation</option>
          <option value="Material Hauling">Material Hauling</option>
          <option value="Excavation Services">Excavation Services</option>
          <option value="On Site Deliveries">On Site Deliveries</option>
          <option value="Other">Other</option>
        </select>
      </div>
      <div style="margin-bottom: 10px;">
        <label for="dates"><strong>Dates Needed:</strong></label><br />
        <input type="date" id="dates" name="dates" required style="width: 100%;" />
      </div>
      <div style="margin-bottom: 10px;">
        <label for="reason"><strong>Reason Trucks Are Needed:</strong></label><br />
        <textarea id="reason" name="reason" required style="width: 100%;"></textarea>
      </div>
      <div style="margin-top: 20px; text-align: center;">
        <button type="submit">Submit Service Request</button>
        <button type="button" onclick="downloadPDF()">Download PDF</button>
        <a href="mailto:egjttrucking@gmail.com?subject=Service%20Request" style="margin-left: 10px; background: #007BFF; color: white; padding: 10px 15px; text-decoration: none; border-radius: 0;">Send Email</a>
      </div>
    </form>
  </section>
  
  <footer>
    <p>&copy; 2025 EGJ Services Group. All rights reserved.</p>
  </footer>
  
  <!-- Modal for Redirected Content -->
  <div id="modal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal()">&times;</span>
      <div id="modal-body"></div>
    </div>
  </div>
  
  <style>
    .modal {
      display: none;
      position: fixed;
      z-index: 2000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(0, 0, 0, 0.8);
    }
    .modal-content {
      background: white;
      margin: 5% auto;
      padding: 20px;
      border-radius: 8px;
      width: 90%;
      max-width: 800px;
      position: relative;
    }
    .modal-content .close {
      position: absolute;
      top: 10px;
      right: 20px;
      color: #aaa;
      font-size: 28px;
      font-weight: bold;
      cursor: pointer;
    }
    .modal-content .close:hover {
      color: black;
    }
  </style>
  
  <script>
    // Update the digital clock in the header
    function updateCompanyClock() {
      const clockEl = document.getElementById('companyclock');
      const now = new Date();
      clockEl.textContent = now.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit', second: '2-digit' });
    }
    updateCompanyClock();
    setInterval(updateCompanyClock, 1000);
    
    // Fetch user's city using ipinfo.io (replace YOUR_TOKEN with your valid token)
    fetch('https://ipinfo.io/json?token=YOUR_TOKEN')
      .then(response => response.json())
      .then(data => {
        const cityEl = document.getElementById('usercity');
        cityEl.textContent = data.city ? " - " + data.city : "";
      })
      .catch(error => console.error('Error fetching location:', error));
    
    function toggleDarkMode() {
      document.body.classList.toggle('dark-mode');
    }
    
    function initMap() {
      var location = { lat: 26.7153, lng: -80.0534 };
      var map = new google.maps.Map(document.getElementById('googlemap'), {
        zoom: 10,
        center: location,
      });
      var marker = new google.maps.Marker({
        position: location,
        map: map
      });
    }
    
    // Toggle description for service cards
    function toggleDescription(card) {
      var desc = card.querySelector('.description');
      if (desc.style.display === "none" || desc.style.display === "") {
        desc.style.display = "block";
      } else {
        desc.style.display = "none";
      }
    }
    
    // Modal functionality for redirect buttons (show only selected section's content)
    function openModal(content) {
      document.getElementById('modal-body').innerHTML = content;
      document.getElementById('modal').style.display = 'block';
    }
    function closeModal() {
      document.getElementById('modal').style.display = 'none';
    }
    document.querySelectorAll('.redirect-button').forEach(function(btn) {
      btn.addEventListener('click', function(e) {
        e.preventDefault();
        var targetId = btn.getAttribute('data-target');
        var content = document.getElementById(targetId).innerHTML;
        openModal(content);
      });
    });
    
    // Work With Us form submission with PDF generation using jsPDF
    document.getElementById('serviceForm')?.addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('name').value;
      const phone = document.getElementById('phone').value;
      const email = document.getElementById('email').value;
      const address = document.getElementById('address').value;
      const companyLocation = document.getElementById('companyLocation').value;
      const companyType = document.getElementById('companyType').value;
      const serviceType = document.getElementById('serviceType').value;
      const dates = document.getElementById('dates').value;
      const reason = document.getElementById('reason').value;
      
      const { jsPDF } = window.jspdf;
      const doc = new jsPDF();
      doc.setFontSize(12);
      doc.text("Service Agreement Request", 10, 10);
      doc.text(`Name: ${name}`, 10, 20);
      doc.text(`Phone: ${phone}`, 10, 30);
      doc.text(`Email: ${email}`, 10, 40);
      doc.text(`Mailing/Billing Address: ${address}`, 10, 50);
      doc.text(`Company Location: ${companyLocation}`, 10, 60);
      doc.text(`Company Type: ${companyType}`, 10, 70);
      doc.text(`Service Type: ${serviceType}`, 10, 80);
      doc.text(`Dates Needed: ${dates}`, 10, 90);
      doc.text(`Reason: ${reason}`, 10, 100);
      
      // Download the generated PDF
      doc.save("ServiceAgreement.pdf");
      
      alert("Your service request has been submitted. The PDF has been downloaded.");
      closeModal();
    });
  </script>
  <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>
</body>
</html>