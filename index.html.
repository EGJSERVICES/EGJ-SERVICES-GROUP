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
    /* Enable smooth scrolling */
    html {
      scroll-behavior: smooth;
    }
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
      /* Construction-inspired gray gradient background */
      background: linear-gradient(to right, #666666, #aaaaaa);
      color: #333;
      margin: 0;
      padding: 0;
      transition: background 0.3s, color 0.3s;
      font-size: 12px; /* Base font size for paragraphs */
    }
    body.dark-mode {
      background: #1a1a1a;
      color: #f0f0f0;
    }
    /* Justify text inside dynamic boxes */
    .dynamicbox p {
      text-align: justify;
    }
    /* Header and New Company Clock */
    header {
      background: rgba(255,255,255,0.9);
      padding: 15px;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      transition: background 0.3s;
      margin-top: 20px; /* Adjusted since no top bar now */
    }
    body.dark-mode header {
      background: rgba(18,18,18,0.9);
    }
    .logo {
      font-size: 28px;
      font-weight: bold;
    }
    .logo img {
      width: 120px;
      height: auto;
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
    .searchbar {
      margin-top: 10px;
    }
    .searchbar input {
      padding: 10px;
      width: 200px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .searchbar button {
      padding: 10px 15px;
      border: none;
      background: #007BFF;
      color: white;
      border-radius: 5px;
      margin-left: 10px;
      cursor: pointer;
      transition: background 0.3s, transform 0.3s;
    }
    .searchbar button:hover {
      background: #0056b3;
      transform: scale(1.05);
    }
    .dark-mode .searchbar button {
      background: #1e88e5;
    }
    .dark-mode .searchbar button:hover {
      background: #1565c0;
    }
    .darkmodetoggle {
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
    .darkmodetoggle:hover {
      background: #0056b3;
    }
    /* New Company Clock in Header */
    #companyclock {
      font-size: 14px;
      margin-top: 10px;
      color: #007BFF;
      font-weight: bold;
    }
    body.dark-mode #companyclock {
      color: #66ccff;
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
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.5);
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
      border-radius: 8px;
      font-size: 20px;
      font-weight: bold;
      box-shadow: 3px 3px 15px rgba(0,0,0,0.2);
      transition: background 0.3s, transform 0.3s, box-shadow 0.3s;
    }
    .btn:hover {
      background: #0056b3;
      transform: translateY(-3px) scale(1.15);
      box-shadow: 5px 5px 20px rgba(0,0,0,0.3);
    }
    /* Dynamic Boxes for Sections */
    .dynamicbox {
      background: rgba(255,255,255,0.8);
      padding: 40px;
      margin: 30px 0;
      border-radius: 20px;
      width: 100%;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      transition: transform 0.3s, background 0.3s;
      text-align: center;
    }
    .dark-mode .dynamicbox {
      background: rgba(50,50,50,0.9);
    }
    .dynamicbox h2 {
      font-size: 32px;
      margin-bottom: 20px;
      transition: color 0.3s;
    }
    body.dark-mode .dynamicbox h2 {
      color: #fff;
    }
    .dynamicbox p {
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
      border-radius: 20px;
      width: 30%;
      margin: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      text-align: center;
      transition: transform 0.3s, box-shadow 0.3s;
      cursor: pointer;
    }
    .servicecard:hover {
      transform: translateY(-5px) scale(1.15);
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    }
    .servicecard img {
      max-width: 100%;
      border-radius: 20px;
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
      border-radius: 20px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      width: 22%;
      text-align: center;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .materialcard:hover {
      transform: translateY(-5px) scale(1.15);
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    }
    .materialcard img {
      max-width: 100%;
      border-radius: 20px;
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
      border-radius: 20px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .faqitem:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 15px rgba(0,0,0,0.15);
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
      border-radius: 20px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .reviewitem:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 15px rgba(0,0,0,0.15);
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
      border-radius: 5px;
      margin-bottom: 10px;
      width: 90%;
      max-width: 600px;
    }
    .reviewform button {
      padding: 10px 15px;
      border: none;
      background: #007BFF;
      color: white;
      border-radius: 5px;
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
      border-radius: 20px;
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
  <!-- New Company Clock in Header -->
  <header>
    <div class="logo"><img src="images/logo.png" alt="Logo"></div>
    <nav>
      <ul>
        <li><a href="#services">Services</a></li>
        <li><a href="#about">About Us</a></li>
        <li><a href="#contact">Contact</a></li>
        <li><a href="#map">Locations</a></li>
      </ul>
    </nav>
    <div id="companyclock"></div>
    <button class="darkmodetoggle" onclick="toggleDarkMode()">Toggle Dark Mode</button>
    <div class="searchbar">
      <input type="text" placeholder="Search...">
      <button><i class="fas fa-search"></i></button>
    </div>
  </header>
  
  <section class="hero dynamicbox">
    <h1>Reliable Construction Transportation Services</h1>
    <p>Serving Palm Beach, St Lucie, and Broward Counties.</p>
    <a href="#contact" class="btn">Request a Quote</a>
  </section>
  
  <section id="services" class="dynamicbox">
    <h2>Our Services</h2>
    <p>We provide all kinds of aggregates, dirt, sand, trash, C&amp;D, and hourly projects.</p>
    <div class="servicecontainer">
      <div class="servicecard" onclick="toggleDescription(this)">
        <img src="images/dumptruck.jpg" alt="Dump Truck">
        <div class="description">
          <h3>Material Transportation</h3>
          <p>We transport aggregates, fill, concrete, asphalt, and more.</p>
        </div>
      </div>
      <div class="servicecard" onclick="toggleDescription(this)">
        <img src="images/constructionsite.jpg" alt="Construction Site">
        <div class="description">
          <h3>On Site Deliveries</h3>
          <p>Fast and efficient delivery to keep your project moving.</p>
        </div>
      </div>
      <div class="servicecard" onclick="toggleDescription(this)">
        <img src="images/machinework.jpg" alt="Machine Work">
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
        <img src="images/concrete.jpg" alt="Concrete">
        <h3>Concrete</h3>
      </div>
      <div class="materialcard">
        <img src="images/asphalt.jpg" alt="Asphalt">
        <h3>Asphalt</h3>
      </div>
      <div class="materialcard">
        <img src="images/fill.jpg" alt="Fill">
        <h3>Fill</h3>
      </div>
      <div class="materialcard">
        <img src="images/sand.jpg" alt="Sand">
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
        <p>We are the trusted partner for any project in South Florida with years of experience and a commitment to reliability and efficiency.</p>
      </div>
      <div class="faqitem">
        <h3>How can I get a quote?</h3>
        <p>You can request a quote by contacting us through our website or calling us directly.</p>
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
    <p>With decades of industry experience, our state of the art fleet and expert drivers guarantee timely and secure transportation. Our commitment to safety, customer satisfaction, and innovation has made us the leading trucking partner in South Florida.</p>
  </section>
  
  <section id="contact" class="dynamicbox">
    <h2>Contact Us</h2>
    <p>Email: egjttrucking@gmail.com</p>
    <p>Phone: 5615068932</p>
    <p>Address: PO BOX 17017, West Palm Beach, FL 33416</p>
  </section>
  
  <footer>
    <p>&copy; 2025 EGJ Services Group. All rights reserved.</p>
  </footer>
  
  <script>
    // Company Clock Functionality
    function updateCompanyClock() {
      const clockEl = document.getElementById('companyclock');
      const now = new Date();
      // Format the time with seconds
      clockEl.textContent = "Current Time: " + now.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit', second: '2-digit' }) + " - West Palm Beach";
    }
    updateCompanyClock();
    setInterval(updateCompanyClock, 1000);
  
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
  
    // Review form functionality
    document.getElementById('submitreview').addEventListener('click', function() {
      const reviewText = document.getElementById('reviewtext').value.trim();
      if (reviewText) {
        const reviewContainer = document.getElementById('reviewcontainer');
        const reviewItem = document.createElement('div');
        reviewItem.className = 'reviewitem';
        reviewItem.innerHTML = `<p>${reviewText}</p><p><strong>Anonymous</strong></p>`;
        reviewContainer.appendChild(reviewItem);
        document.getElementById('reviewtext').value = '';
      } else {
        alert('Please enter a review before submitting.');
      }
    });
  </script>
  <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>
</body>
</html>