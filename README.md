<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="description" content="EGJ Services Group – Leading trucking services in South Florida. We specialize in three-axle truck transportation, hauling aggregates, and more." />
  <meta name="keywords" content="trucking, construction, dump truck, hauling, aggregates, South Florida" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>EGJ Services Group</title>
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
      background: linear-gradient(to right, #003366, #336699);
      color: #333;
      margin: 0;
      padding: 0;
      transition: background 0.3s, color 0.3s;
      font-size: 12px;
      line-height: 1.5;
    }
    body.dark-mode { background: #1a1a1a; color: #f0f0f0; }
    p { text-align: justify; margin: 10px 0; }
    
    /* Header */
    header {
      background: rgba(255,255,255,0.9);
      padding: 15px;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      transition: background 0.3s;
      margin-top: 20px;
    }
    body.dark-mode header { background: rgba(18,18,18,0.9); }
    .logo { font-size: 28px; font-weight: bold; margin-bottom: 10px; color: inherit; }
    .logo img { width: 120px; height: auto; }
    .header-extras {
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      margin-bottom: 10px;
    }
    .digitalclock { font-size: 14px; font-weight: bold; }
    .company-location { font-size: 14px; font-weight: bold; }
    
    /* Dynamic Island for Navigation Buttons */
    #dynamicIsland {
      background: rgba(255,255,255,0.8);
      backdrop-filter: blur(5px);
      border-radius: 50px;
      padding: 10px 20px;
      position: fixed;
      top: 10px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 2500;
      display: flex;
      gap: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      animation: slideDown 0.5s ease-out;
    }
    @keyframes slideDown {
      from { opacity: 0; transform: translate(-50%, -30px); }
      to { opacity: 1; transform: translate(-50%, 0); }
    }
    #dynamicIsland a {
      text-decoration: none;
      color: inherit;
      font-size: 16px;
      font-weight: bold;
      padding: 5px 10px;
      transition: background 0.3s, transform 0.3s;
    }
    #dynamicIsland a:hover { background: #007BFF; color: white; transform: scale(1.05); }
    
    /* Dark mode toggle button */
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
    .darkmodetoggle:hover { background: #0056b3; }
    
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
    .hero > * { position: relative; z-index: 2; }
    .hero h1 { font-size: 48px; margin-bottom: 20px; transition: color 0.3s; }
    body.dark-mode .hero h1 { color: #fff; }
    .hero p { font-size: 24px; margin-bottom: 40px; }
    .btn {
      background: #007BFF;
      color: white;
      padding: 15px 30px;
      text-decoration: none;
      border-radius: 0;
      font-size: 20px;
      font-weight: bold;
      transition: background 0.3s, transform 0.3s;
      text-align: center;
      display: inline-block;
      margin: 10px 0;
    }
    .btn:hover { background: #0056b3; transform: translateY(-3px) scale(1.15); }
    
    /* Section Styles – Minimal, No Box Backgrounds */
    section { padding: 40px 20px; margin: 30px 0; }
    section h2 { font-size: 32px; margin-bottom: 20px; text-align: center; }
    section p { margin: 10px 0; }
    
    /* Service Cards – Minimal styling, no background boxes */
    .servicecontainer { display: flex; flex-wrap: wrap; justify-content: space-around; }
    .servicecard {
      /* Removed background & shadow for a flat design */
      padding: 20px;
      width: 30%;
      margin: 15px;
      border-bottom: 2px solid #007BFF;
      text-align: center;
      transition: transform 0.3s;
      cursor: pointer;
    }
    .servicecard:hover { transform: scale(1.05); }
    .servicecard img { max-width: 100%; margin-bottom: 15px; }
    .description { display: none; text-align: left; margin-top: 10px; border-top: 1px solid #ccc; padding-top: 10px; }
    
    /* Materials Section – Minimal styling */
    .materialscontainer { display: flex; flex-wrap: wrap; justify-content: space-around; margin-top: 20px; }
    .materialcard {
      padding: 15px;
      margin: 15px;
      width: 22%;
      text-align: center;
      transition: transform 0.3s;
    }
    .materialcard:hover { transform: scale(1.05); }
    .materialcard img { max-width: 100%; margin-bottom: 10px; }
    
    /* FAQ Section – Minimal styling */
    .faqcontainer { margin-top: 20px; text-align: justify; }
    .faqitem { padding: 20px; margin: 10px 0; transition: transform 0.3s; }
    .faqitem:hover { transform: scale(1.02); }
    .faqitem h3 { font-size: 22px; margin-bottom: 10px; }
    .faqitem p { font-size: 18px; }
    
    /* Review Section – Minimal styling */
    .reviewcontainer { margin-top: 20px; text-align: justify; }
    .reviewitem { padding: 20px; margin: 10px 0; transition: transform 0.3s; }
    .reviewitem:hover { transform: scale(1.02); }
    .reviewform { margin-top: 20px; display: flex; flex-direction: column; align-items: center; }
    .reviewform input, .reviewform textarea {
      padding: 10px;
      margin-bottom: 10px;
      width: 90%;
      max-width: 600px;
      border: 1px solid #ccc;
    }
    .reviewform button {
      padding: 10px 15px;
      border: none;
      background: #007BFF;
      color: white;
      transition: background 0.3s, transform 0.3s;
      cursor: pointer;
    }
    .reviewform button:hover { background: #0056b3; transform: scale(1.05); }
    
    /* Contact Section */
    #contact a { color: #007BFF; text-decoration: none; }
    #contact a:hover { text-decoration: underline; }
    
    /* Modal for Redirected Content */
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
    
    /* Dynamic Island for Buttons */
    #dynamicIsland {
      background: rgba(255,255,255,0.8);
      backdrop-filter: blur(5px);
      border-radius: 50px;
      padding: 10px 20px;
      position: fixed;
      top: 10px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 2500;
      display: flex;
      gap: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      animation: slideDown 0.5s ease-out;
    }
    #dynamicIsland a {
      text-decoration: none;
      color: inherit;
      font-size: 16px;
      font-weight: bold;
      padding: 5px 10px;
      transition: background 0.3s, transform 0.3s;
    }
    #dynamicIsland a:hover {
      background: #007BFF;
      color: white;
      transform: scale(1.05);
    }
    @keyframes slideDown {
      from { opacity: 0; transform: translate(-50%, -30px); }
      to { opacity: 1; transform: translate(-50%, 0); }
    }
  </style>
</head>
<body>
  <header>
    <div class="logo"><img src="images/logo.png" alt="Logo" /></div>
    <div class="header-extras">
      <div class="digitalclock" id="companyclock"></div>
      <div class="company-location">West Palm Beach, FL</div>
    </div>
    <!-- Dynamic Island for Navigation Buttons -->
    <div id="dynamicIsland">
      <a href="#services" class="redirect-button" data-target="services">Services</a>
      <a href="#about" class="redirect-button" data-target="about">About Us</a>
      <a href="#contact" class="redirect-button" data-target="contact">Contact</a>
      <a href="#map" class="redirect-button" data-target="map">Locations</a>
      <a href="#workwithus" class="redirect-button" data-target="workwithus">Work With Us</a>
    </div>
    <button class="darkmodetoggle" onclick="toggleDarkMode()">Toggle Dark Mode</button>
  </header>
  
  <section class="hero">
    <h1>Reliable Construction Transportation Services</h1>
    <p style="margin-bottom: 40px;">Serving Palm Beach, St Lucie, and Broward Counties.</p>
    <!-- Separate text from the button -->
    <a href="#" class="btn redirect-button" data-target="contact" style="margin-top:20px;">Request a Quote</a>
  </section>
  
  <section id="services">
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
  
  <section id="materials">
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
  
  <section id="map">
    <h2>Our Service Areas</h2>
    <div id="googlemap"></div>
  </section>
  
  <section id="faq">
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
  
  <section id="about">
    <h2>About Us</h2>
    <p>EGJ Services Group specializes in three axle truck transportation, hauling aggregates and excess materials across Palm Beach, St Lucie, and Broward Counties. We ensure fast deliveries, exceptional service, transparency, and competitive pricing. Trust us for efficient and reliable hauling solutions that keep your projects on track!</p>
    <p>With decades of industry experience, our state-of-the-art fleet and expert drivers guarantee timely and secure transportation. Our commitment to safety, customer satisfaction, and innovation has made us the leading trucking partner in South Florida.</p>
  </section>
  
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
  
  <!-- Optimization, Animation & AI Scripts -->
  <script>
    // --- Update Digital Clock ---
    function updateCompanyClock() {
      const clockEl = document.getElementById('companyclock');
      const now = new Date();
      clockEl.textContent = now.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit', second: '2-digit' });
    }
    updateCompanyClock();
    setInterval(updateCompanyClock, 1000);
    
    // --- Debounce Function for Optimizing Scroll Events ---
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
    
    // --- Modal Functionality for Redirect Buttons ---
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
    
    // --- Initialize Google Map ---
    function initMap() {
      const location = { lat: 26.7153, lng: -80.0534 };
      const map = new google.maps.Map(document.getElementById('googlemap'), {
        zoom: 10,
        center: location,
      });
      new google.maps.Marker({ position: location, map: map });
    }
    
    // --- Toggle Description for Service Cards ---
    function toggleDescription(card) {
      const desc = card.querySelector('.description');
      desc.style.display = (desc.style.display === "none" || desc.style.display === "") ? "block" : "none";
    }
    
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
        <input type="text" id="chatbot-input" placeholder="Ask me anything..." />
      `;
      document.body.appendChild(chatbot);
      
      // When user submits a message, simulate a proactive response
      document.getElementById('chatbot-input').addEventListener('keypress', function(e) {
        if (e.key === 'Enter') {
          const userMessage = this.value;
          this.value = '';
          addChatMessage('user', userMessage);
          // Here you could integrate with the ChatGPT API.
          // For now, we simulate a proactive answer:
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
      // Placeholder: In a real scenario, call your ChatGPT API here.
      return "I'm here to help! Could you please provide more details about your inquiry?";
    }
    
    function toggleChatbot() {
      const chatbot = document.getElementById('chatbot');
      chatbot.style.display = (chatbot.style.display === 'none' || !chatbot.style.display) ? 'block' : 'none';
    }
    
    document.addEventListener('DOMContentLoaded', function() {
      initChatbot();
      // Create a chatbot toggle button (Dynamic Island could also include this if desired)
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
        border-radius: 0;
        cursor: pointer;
        z-index: 3001;
      }
    `;
    document.head.appendChild(chatbotStyles);
  </script>
  <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>
</body>
</html>