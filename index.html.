<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="description" content="EGJ Services Group – Leading trucking services in South Florida. We specialize in three-axle truck transportation, hauling aggregates, and more." />
  <meta name="keywords" content="trucking, construction, dump truck, hauling, aggregates, South Florida" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>EGJ Services Group</title>
  <!-- External CSS -->
  <link rel="stylesheet" href="styles.css" />
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <!-- jsPDF for PDF generation -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <script defer src="script.js"></script>
  <style>
    /* Base Styles */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    html, body { width: 100%; height: 100%; }
    body {
      font-family: Arial, sans-serif;
      /* Background: gradient from white to light blue */
      background: linear-gradient(to bottom, white, #add8e6);
      color: #333;
      margin: 0;
      padding: 0;
      transition: background 0.3s, color 0.3s;
      font-size: 14px;
      line-height: 1.6;
    }
    body.dark-mode {
      background: #121212;
      color: #f0f0f0;
    }
    p { text-align: justify; margin: 10px 0; }
    
    /* Main Container for wider content */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    
    /* Dark Mode Toggle Switch with Label */
    .switch {
      position: fixed;
      top: 20px;
      right: 20px;
      display: flex;
      align-items: center;
      z-index: 1000;
      font-size: 14px;
      font-weight: bold;
      color: #333;
    }
    .switch span.label-text { margin-right: 8px; }
    .switch input { opacity: 0; width: 0; height: 0; }
    .slider {
      position: relative;
      cursor: pointer;
      width: 50px;
      height: 24px;
      background-color: #ccc;
      transition: 0.4s;
      border-radius: 34px;
    }
    .slider:before {
      position: absolute;
      content: "";
      height: 18px;
      width: 18px;
      left: 3px;
      bottom: 3px;
      background-color: white;
      transition: 0.4s;
      border-radius: 50%;
    }
    input:checked + .slider {
      background-color: #2196F3;
    }
    input:checked + .slider:before {
      transform: translateX(26px);
    }
    @media (max-width: 600px) {
      .switch { font-size: 12px; }
      .slider { width: 40px; height: 20px; }
      .slider:before { height: 16px; width: 16px; left: 2px; bottom: 2px; }
    }
    
    /* Header */
    header {
      background: rgba(255,255,255,0.95);
      padding: 20px;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      transition: background 0.3s;
      margin-top: 20px;
      opacity: 0;
      animation: fadeIn 1s forwards;
    }
    body.dark-mode header { background: rgba(18,18,18,0.95); }
    .logo { font-size: 32px; font-weight: bold; margin-bottom: 10px; color: inherit; }
    .logo img { width: 150px; height: auto; }
    .header-extras {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 5px;
      margin-bottom: 10px;
    }
    .digitalclock, .company-location { font-size: 20px; font-weight: bold; }
    
    /* Navigation Bar */
    nav {
      width: 100%;
      background: #f0f0f0;
      border-top: 2px solid #add8e6;
      border-bottom: 2px solid #add8e6;
      margin-top: 10px;
    }
    nav ul {
      list-style: none;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      padding: 10px 0;
      margin: 0;
    }
    nav ul li { margin: 0 15px; }
    nav ul li a {
      text-decoration: none;
      color: #333;
      font-size: 18px;
      font-weight: bold;
      padding: 5px 10px;
      transition: background 0.3s, transform 0.3s;
      border-radius: 5px;
    }
    nav ul li a:hover { background: #007BFF; color: white; transform: scale(1.05); }
    body.dark-mode nav { background: #222; }
    body.dark-mode nav ul li a { color: #f0f0f0; }
    body.dark-mode nav ul li a:hover { background: #0056b3; }
    
    /* Hero Section (Tri-Axle Dump Truck Background) */
    .hero {
      position: relative;
      text-align: center;
      padding: 120px 20px;
      background: url('https://images.unsplash.com/photo-1572562699232-1a5c3dfb2416?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
      color: white;
      opacity: 0;
      animation: fadeIn 1s forwards;
      animation-delay: 0.5s;
    }
    .hero::before {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.5);
      z-index: 1;
    }
    .hero > * { position: relative; z-index: 2; }
    .hero h1 {
      font-size: 56px;
      margin-bottom: 20px;
      transition: color 0.3s, transform 0.5s;
      /* 4D Animation: continuous 3D rotation effect */
      animation: rotate4d 4s infinite;
    }
    body.dark-mode .hero h1 { color: #fff; }
    .hero p { font-size: 26px; margin-bottom: 40px; }
    .btn {
      background: #007BFF;
      color: white;
      padding: 15px 30px;
      text-decoration: none;
      font-size: 20px;
      font-weight: bold;
      transition: background 0.3s, transform 0.3s;
      display: inline-block;
      margin: 10px 0;
      border-radius: 5px;
    }
    .btn:hover { background: #0056b3; transform: translateY(-3px) scale(1.1); }
    
    /* Section Styles – Minimal and Clean */
    section {
      padding: 40px 20px;
      margin: 30px 0;
      opacity: 0;
      animation: fadeIn 1s forwards;
      animation-delay: 0.3s;
    }
    section h2 { font-size: 32px; margin-bottom: 20px; text-align: center; }
    section p { margin: 10px 0; }
    
    /* Service Cards – 3D Hover Effects */
    .servicecontainer { display: flex; flex-wrap: wrap; justify-content: space-around; }
    .servicecard {
      perspective: 1000px;
      padding: 20px;
      width: 30%;
      margin: 15px;
      border-bottom: 2px solid #007BFF;
      text-align: center;
      transition: transform 0.3s;
      cursor: pointer;
      border-radius: 5px;
      background: #fff;
    }
    .servicecard:hover { transform: rotateY(8deg) rotateX(5deg) scale(1.05); }
    .servicecard img { max-width: 100%; margin-bottom: 15px; border-radius: 5px; }
    .description {
      display: none;
      text-align: left;
      margin-top: 10px;
      border-top: 1px solid #ccc;
      padding-top: 10px;
    }
    
    /* Materials Section – 3D Hover Effects */
    .materialscontainer { display: flex; flex-wrap: wrap; justify-content: space-around; margin-top: 20px; }
    .materialcard {
      perspective: 1000px;
      padding: 15px;
      margin: 15px;
      width: 22%;
      text-align: center;
      transition: transform 0.3s;
      border-radius: 5px;
      background: #fff;
    }
    .materialcard:hover { transform: rotateY(8deg) scale(1.05); }
    .materialcard img { max-width: 100%; margin-bottom: 10px; border-radius: 5px; }
    
    /* FAQ Section */
    .faqcontainer { margin-top: 20px; text-align: justify; }
    .faqitem {
      padding: 20px;
      margin: 10px 0;
      transition: transform 0.3s;
      background: #fff;
      border-radius: 5px;
    }
    .faqitem:hover { transform: scale(1.02); }
    .faqitem h3 { font-size: 22px; margin-bottom: 10px; }
    .faqitem p { font-size: 18px; }
    
    /* Review Section */
    .reviewcontainer { margin-top: 20px; text-align: justify; }
    .reviewitem {
      padding: 20px;
      margin: 10px 0;
      transition: transform 0.3s;
      background: #fff;
      border-radius: 5px;
    }
    .reviewitem:hover { transform: scale(1.02); }
    .reviewform {
      margin-top: 20px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .reviewform input,
    .reviewform textarea {
      padding: 10px;
      margin-bottom: 10px;
      width: 90%;
      max-width: 600px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .reviewform button {
      padding: 10px 15px;
      border: none;
      background: #007BFF;
      color: white;
      transition: background 0.3s, transform 0.3s;
      cursor: pointer;
      border-radius: 5px;
    }
    .reviewform button:hover { background: #0056b3; transform: scale(1.05); }
    
    /* Contact Section */
    #contact a { color: #007BFF; text-decoration: none; }
    #contact a:hover { text-decoration: underline; }
    
    /* Modal */
    .modal {
      display: none;
      position: fixed;
      z-index: 2000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(0,0,0,0.8);
    }
    .modal-content {
      background: white;
      margin: 5% auto;
      padding: 20px;
      border-radius: 8px;
      width: 90%;
      max-width: 800px;
      position: relative;
      animation: modalIn 0.5s ease-out;
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
    .modal-content .close:hover { color: black; }
    @keyframes modalIn { from { opacity: 0; transform: translateY(50px); } to { opacity: 1; transform: translateY(0); } }
    
    /* Footer */
    footer { text-align: center; padding: 20px; background: #007BFF; color: white; transition: background 0.3s; }
    
    /* Responsive */
    @media (max-width: 768px) {
      .servicecard, .materialcard { width: 90%; }
      nav ul li { margin: 0 10px; }
    }
    
    /* Animations */
    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    /* 4D Animation (continuous 3D rotation effect) */
    @keyframes rotate4d {
      0% { transform: perspective(800px) rotateX(0deg) rotateY(0deg) rotateZ(0deg); }
      25% { transform: perspective(800px) rotateX(20deg) rotateY(20deg) rotateZ(10deg); }
      50% { transform: perspective(800px) rotateX(0deg) rotateY(40deg) rotateZ(0deg); }
      75% { transform: perspective(800px) rotateX(20deg) rotateY(20deg) rotateZ(-10deg); }
      100% { transform: perspective(800px) rotateX(0deg) rotateY(0deg) rotateZ(0deg); }
    }
  </style>
</head>
<body>
  <!-- Dark Mode Toggle Switch with Label -->
  <label class="switch">
    <span class="label-text">Dark Mode</span>
    <input type="checkbox" id="darkModeToggle">
    <span class="slider"></span>
  </label>
  
  <!-- Main Container -->
  <div class="container">
    <!-- Header Section -->
    <header>
      <div class="logo">
        <img src="https://images.unsplash.com/photo-1581092795363-9146b5e80db3?ixlib=rb-1.2.1&auto=format&fit=crop&w=150&q=80" alt="Logo" />
      </div>
      <div class="header-extras">
        <div class="digitalclock" id="companyclock"></div>
        <div class="company-location">West Palm Beach, FL</div>
      </div>
      <nav>
        <ul>
          <li><a href="#services" class="redirect-button" data-target="services">Services</a></li>
          <li><a href="#about" class="redirect-button" data-target="about">About Us</a></li>
          <li><a href="#contact" class="redirect-button" data-target="contact">Contact</a></li>
          <li><a href="#map" class="redirect-button" data-target="map">Locations</a></li>
          <li><a href="#workwithus" class="redirect-button" data-target="workwithus">Work With Us</a></li>
        </ul>
      </nav>
    </header>
    
    <!-- Hero Section with Tri-Axle Dump Truck Background -->
    <section class="hero">
      <h1>Reliable Construction Transportation Services</h1>
      <p style="margin-bottom: 40px;">Serving Palm Beach, St Lucie, and Broward Counties.</p>
      <a href="#" class="btn redirect-button" data-target="contact" style="margin-top:20px;">Request a Quote</a>
    </section>
    
    <!-- Services Section -->
    <section id="services">
      <h2>Our Services</h2>
      <p>We offer a comprehensive range of trucking services for construction projects—including material transportation, on site deliveries, and excavation services.</p>
      <div class="servicecontainer">
        <div class="servicecard" onclick="toggleDescription(this)">
          <img src="https://images.unsplash.com/photo-1611095973511-68fa81f48972?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Dump Truck Transportation" />
          <div class="description">
            <h3>Material Transportation</h3>
            <p>Our modern fleet ensures safe and efficient transport of aggregates, concrete, and more.</p>
          </div>
        </div>
        <div class="servicecard" onclick="toggleDescription(this)">
          <img src="https://images.unsplash.com/photo-1569004622937-6d7cd68aef7d?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="On Site Deliveries" />
          <div class="description">
            <h3>On Site Deliveries</h3>
            <p>We deliver materials directly to your construction site, keeping projects on schedule.</p>
          </div>
        </div>
        <div class="servicecard" onclick="toggleDescription(this)">
          <img src="https://images.unsplash.com/photo-1611158721515-3a7a9506c7df?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Excavation Services" />
          <div class="description">
            <h3>Excavation Services</h3>
            <p>Our excavation experts offer efficient land clearing and site preparation services.</p>
          </div>
        </div>
      </div>
    </section>
    
    <!-- Materials Section -->
    <section id="materials">
      <h2>Construction Materials</h2>
      <div class="materialscontainer">
        <div class="materialcard">
          <img src="https://images.unsplash.com/photo-1570172619642-9977d8c1606e?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Concrete" />
          <h3>Concrete</h3>
        </div>
        <div class="materialcard">
          <img src="https://images.unsplash.com/photo-1560357879-3a61a3d2d6f6?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Asphalt" />
          <h3>Asphalt</h3>
        </div>
        <div class="materialcard">
          <img src="https://images.unsplash.com/photo-1552635036-3e9bfb99795a?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Fill" />
          <h3>Fill</h3>
        </div>
        <div class="materialcard">
          <img src="https://images.unsplash.com/photo-1576129143113-8da0e87d8b6d?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Sand" />
          <h3>Sand</h3>
        </div>
      </div>
    </section>
    
    <!-- Google Map Section (Using Embedded Iframe) -->
    <section id="map">
      <h2>Our Service Areas</h2>
      <!-- Embedded Google Map -->
      <iframe 
        src="https://www.google.com/maps/embed?pb=!1m17!1m12!1m3!1d4603.734359952162!2d-80.14422492364695!3d26.706649976770603!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m2!1m1!2zMjbCsDQyJzIzLjkiTiA4MMKwMDgnMjkuOSJX!5e1!3m2!1sen!2sus!4v1739717706873!5m2!1sen!2sus" 
        width="100%" 
        height="400" 
        style="border:0;" 
        allowfullscreen="" 
        loading="lazy" 
        referrerpolicy="no-referrer-when-downgrade">
      </iframe>
    </section>
    
    <!-- FAQ Section -->
    <section id="faq">
      <h2>Frequently Asked Questions</h2>
      <div class="faqcontainer">
        <div class="faqitem">
          <h3>What services do you provide?</h3>
          <p>We offer material transportation, on site deliveries, and excavation services—handling aggregates, dirt, sand, trash, C&amp;D, and more.</p>
        </div>
        <div class="faqitem">
          <h3>Why choose us?</h3>
          <p>With decades of experience and cutting-edge equipment, we are the trusted partner for construction projects in South Florida.</p>
        </div>
        <div class="faqitem">
          <h3>How can I get a quote?</h3>
          <p>Simply click on the “Request a Quote” button or contact us directly.</p>
        </div>
        <div class="faqitem">
          <h3>What is your typical project size?</h3>
          <p>Our projects range from small local jobs to large-scale construction projects, tailored to your needs.</p>
        </div>
        <div class="faqitem">
          <h3>What are your payment terms?</h3>
          <p>We offer competitive pricing with flexible payment options—please contact us for details.</p>
        </div>
      </div>
    </section>
    
    <!-- Reviews Section -->
    <section id="reviews">
      <h2>Reviews</h2>
      <div class="reviewcontainer" id="reviewcontainer">
        <div class="reviewitem">
          <p>Great service and fast delivery. Highly recommended!</p>
          <p><strong>John Doe</strong> – <em>Acme Construction</em></p>
        </div>
        <div class="reviewitem">
          <p>Reliable and efficient. The best trucking service in South Florida.</p>
          <p><strong>Jane Smith</strong> – <em>BuildRight Inc.</em></p>
        </div>
      </div>
      <div class="reviewform">
        <input type="text" id="reviewerName" placeholder="Your Name" required />
        <input type="text" id="reviewerCompany" placeholder="Your Company" required />
        <textarea id="reviewtext" placeholder="Leave your review here..." required></textarea>
        <button id="submitreview">Submit Review</button>
      </div>
    </section>
    
    <!-- About Us Section -->
    <section id="about">
      <h2>About Us</h2>
      <p>EGJ Services Group specializes in three-axle truck transportation, hauling aggregates and excess materials across Palm Beach, St Lucie, and Broward Counties. We ensure fast deliveries, exceptional service, transparency, and competitive pricing. Trust us for efficient and reliable hauling solutions that keep your projects on track!</p>
      <p>With decades of industry experience, our state-of-the-art fleet and expert drivers guarantee timely and secure transportation. Our commitment to safety, customer satisfaction, and innovation has made us the leading trucking partner in South Florida.</p>
    </section>
    
    <!-- Contact Section -->
    <section id="contact">
      <h2>Contact Us</h2>
      <p>Email: <a href="mailto:egjttrucking@gmail.com">egjttrucking@gmail.com</a></p>
      <p>Phone: <a href="tel:5615068932">5615068932</a></p>
      <p>Address: PO BOX 17017, West Palm Beach, FL 33416</p>
    </section>
    
    <!-- Hidden "Work With Us" Form -->
    <section id="workwithus" style="display: none; text-align: left; padding: 40px 20px;">
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
          <a href="mailto:egjttrucking@gmail.com?subject=Service%20Request" style="margin-left: 10px; background: #007BFF; color: white; padding: 10px 15px; text-decoration: none;">Send Email</a>
        </div>
      </form>
    </section>
    
    <!-- Footer -->
    <footer>
      <p>&copy; 2025 EGJ Services Group. All rights reserved.</p>
    </footer>
  </div> <!-- End container -->
  
  <!-- Modal for Redirected Content -->
  <div id="modal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal()">&times;</span>
      <div id="modal-body"></div>
    </div>
  </div>
  
  <!-- Optimization, Animation & AI Scripts -->
  <script>
    // --- Update Digital Clock with Date ---
    function updateCompanyClock() {
      const clockEl = document.getElementById('companyclock');
      const now = new Date();
      const date = now.toLocaleDateString();
      const time = now.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit', second: '2-digit' });
      clockEl.innerHTML = date + "<br>" + time;
    }
    updateCompanyClock();
    setInterval(updateCompanyClock, 1000);
    
    // --- Debounce Function for Scroll Events ---
    function debounce(func, wait, immediate) {
      let timeout;
      return function() {
        const context = this, args = arguments;
        const later = function() {
          timeout = null;
          if (!immediate) func.apply(context, args);
        };
        const callNow = immediate && !timeout;
        clearTimeout(timeout);
        timeout = setTimeout(later, wait);
        if (callNow) func.apply(context, args);
      };
    }
    
    // --- On-scroll Animation for Elements with .animate-on-scroll ---
    function animateOnScroll() {
      const elements = document.querySelectorAll('.animate-on-scroll');
      elements.forEach(el => {
        const rect = el.getBoundingClientRect();
        if (rect.top < window.innerHeight && rect.bottom > 0) {
          el.classList.add('animated');
        } else {
          el.classList.remove('animated');
        }
      });
    }
    window.addEventListener('scroll', debounce(animateOnScroll, 100));
    animateOnScroll();
    
    // --- Lazy Loading Images ---
    document.addEventListener("DOMContentLoaded", function() {
      const lazyImages = document.querySelectorAll("img[data-src]");
      if ("IntersectionObserver" in window) {
        const imgObserver = new IntersectionObserver((entries, observer) => {
          entries.forEach(entry => {
            if (entry.isIntersecting) {
              const img = entry.target;
              img.src = img.getAttribute("data-src");
              observer.unobserve(img);
            }
          });
        });
        lazyImages.forEach(img => imgObserver.observe(img));
      } else {
        lazyImages.forEach(img => { img.src = img.getAttribute("data-src"); });
      }
    });
    
    // --- Modal Functionality ---
    function openModal(content) {
      document.getElementById('modal-body').innerHTML = content;
      document.getElementById('modal').style.display = 'block';
    }
    function closeModal() {
      document.getElementById('modal').style.display = 'none';
    }
    document.querySelectorAll('.redirect-button').forEach(btn => {
      btn.addEventListener('click', function(e) {
        e.preventDefault();
        const targetId = btn.getAttribute('data-target');
        const content = document.getElementById(targetId).innerHTML;
        openModal(content);
      });
    });
    
    // --- Work With Us Form: PDF Generation via jsPDF ---
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
      doc.text(`Type of Company: ${companyType}`, 10, 70);
      doc.text(`Service Type: ${serviceType}`, 10, 80);
      doc.text(`Dates Needed: ${dates}`, 10, 90);
      doc.text(`Reason: ${reason}`, 10, 100);
      
      doc.save("ServiceAgreement.pdf");
      alert("Your service request has been submitted. The PDF has been downloaded.");
      closeModal();
    });
    
    // --- Initialize Google Map (Embedded iframe is used, so this script is no longer needed) ---
    // If you prefer using the API, replace the iframe with a div and provide a valid API key.
    function initMap() {
      // This function is kept for backward compatibility. The map is loaded via the iframe below.
    }
    
    // --- Toggle Description for Service Cards ---
    function toggleDescription(card) {
      const desc = card.querySelector('.description');
      desc.style.display = (desc.style.display === "none" || desc.style.display === "") ? "block" : "none";
    }
    
    // --- Dark Mode Toggle via Switch ---
    document.getElementById("darkModeToggle").addEventListener("change", function() {
      if (this.checked) {
        document.body.classList.add("dark-mode");
      } else {
        document.body.classList.remove("dark-mode");
      }
    });
    
    // --- AI Virtual Assistant Chatbot (Proactive Integration) ---
    function initChatbot() {
      const chatbot = document.createElement('div');
      chatbot.id = 'chatbot';
      chatbot.innerHTML = `
        <div id="chatbot-header">
          Virtual Assistant
          <button id="closeChatbot" onclick="toggleChatbot()">X</button>
        </div>
        <div id="chatbot-body"></div>
        <input type="text" id="chatbot-input" placeholder="How can I help you?" />
      `;
      document.body.appendChild(chatbot);
      
      document.getElementById('chatbot-input').addEventListener('keypress', function(e) {
        if (e.key === 'Enter') {
          const userMessage = this.value;
          this.value = '';
          addChatMessage('user', userMessage);
          setTimeout(() => {
            const response = getAIResponse(userMessage);
            addChatMessage('ai', response);
          }, 1000);
        }
      });
    }
    
    function addChatMessage(sender, message) {
      const chatBody = document.getElementById('chatbot-body');
      const msgDiv = document.createElement('div');
      msgDiv.className = 'chat-message ' + sender;
      msgDiv.textContent = message;
      chatBody.appendChild(msgDiv);
      chatBody.scrollTop = chatBody.scrollHeight;
    }
    
    function getAIResponse(message) {
      return "I'm here to help! Could you please provide more details about your question?";
    }
    
    function toggleChatbot() {
      const chatbot = document.getElementById('chatbot');
      chatbot.style.display = (chatbot.style.display === 'none' || !chatbot.style.display) ? 'block' : 'none';
    }
    
    document.addEventListener('DOMContentLoaded', function() {
      initChatbot();
      const chatToggle = document.createElement('button');
      chatToggle.id = 'chatbot-toggle';
      chatToggle.textContent = 'Chat with Us';
      chatToggle.onclick = toggleChatbot;
      document.body.appendChild(chatToggle);
    });
    
    // --- Inject Chatbot Styles ---
    const chatbotStyles = document.createElement('style');
    chatbotStyles.innerHTML = `
      #chatbot {
        position: fixed;
        bottom: 20px;
        right: 20px;
        width: 300px;
        background: white;
        border: 1px solid #ccc;
        display: none;
        flex-direction: column;
        z-index: 3000;
      }
      #chatbot-header {
        background: #007BFF;
        color: white;
        padding: 10px;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }
      #chatbot-body {
        height: 200px;
        overflow-y: auto;
        padding: 10px;
        background: #f9f9f9;
      }
      #chatbot-input {
        border: none;
        border-top: 1px solid #ccc;
        padding: 10px;
        width: 100%;
      }
      .chat-message.user {
        text-align: right;
        margin-bottom: 5px;
        color: #007BFF;
      }
      .chat-message.ai {
        text-align: left;
        margin-bottom: 5px;
        color: #333;
      }
      #chatbot-toggle {
        position: fixed;
        bottom: 20px;
        right: 20px;
        padding: 10px 15px;
        background: #007BFF;
        color: white;
        border: none;
        cursor: pointer;
        z-index: 3001;
      }
    `;
    document.head.appendChild(chatbotStyles);
  </script>
  <!-- Embedded Google Map (No API Key Needed) -->
  <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>
</body>
</html>