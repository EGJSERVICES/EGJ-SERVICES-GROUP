<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EGJ SERVICES GROUP - Professional Trucking Services</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        html, body {
            width: 100%;
            height: 100%;
            font-family: Arial, sans-serif;
            background: linear-gradient(to bottom, #1a1a1a, #4b0000);
            color: #f0f0f0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            overflow-x: hidden;
        }
        .container {
            width: 100%;
            max-width: 1400px;
            padding: 40px;
            background: rgba(20, 20, 20, 0.9);
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
        .header-container {
            text-align: center;
            width: 100%;
            margin-bottom: 20px;
        }
        .header-container h1 {
            font-size: 48px;
            font-weight: bold;
            color: #FFD700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.7);
            animation: slideIn 1s ease-in-out;
        }
        @keyframes slideIn {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }
        .header-container img {
            width: 100%;
            max-width: 600px;
            animation: zoomIn 1.2s ease-in-out;
        }
        @keyframes zoomIn {
            from { transform: scale(0.8); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }
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
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s ease-in-out;
        }
        .section:hover {
            transform: scale(1.05);
        }
        h2 {
            color: #FFA500;
            text-align: center;
        }
        p, ul {
            font-size: 18px;
            line-height: 1.8;
            text-align: center;
        }
        ul {
            padding-left: 0;
            list-style-position: inside;
        }
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
            display: block;
            width: 100%;
            max-width: 300px;
            margin-left: auto;
            margin-right: auto;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #FF8C00;
        }
        .footer {
            text-align: center;
            padding: 20px;
            width: 100%;
        }
        @media (max-width: 768px) {
            .section {
                width: 100%;
                max-width: 90%;
            }
            .header-container img {
                width: 100%;
            }
            .header-container h1 {
                font-size: 36px;
            }
            p, ul {
                font-size: 16px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header-container">
            <h1>EGJ SERVICES GROUP</h1>
            <img src="tri-axle-dump-truck.jpg" alt="Tri Axle Dump Truck">
        </div>
        <div class="content">
            <section class="section contact">
                <h2>Contact Us</h2>
                <p>Email: <a href="mailto:egjttrucking@gmail.com">egjttrucking@gmail.com</a></p>
                <p>Phone: <a href="tel:5615068932">561-506-8932</a></p>
                <p>Address: PO BOX 17017, West Palm Beach, FL 33416</p>
            </section>
            <section class="section services">
                <h2>Our Services</h2>
                <p>EGJ Services Group specializes in high-quality trucking and hauling services using top-tier tri axle dump trucks.</p>
                <button onclick="alert('Request a Service Coming Soon!')">Request a Service</button>
                <button onclick="alert('FAQ Coming Soon!')">Frequently Asked Questions</button>
            </section>
            <section class="section tri-axle-info">
                <h2>Tri Axle Dump Truck Services</h2>
                <p>Our fleet of tri axle dump trucks is equipped to handle a variety of heavy-duty transportation needs, ensuring efficiency and reliability.</p>
                <h3>Key Benefits:</h3>
                <ul>
                    <li>Superior load capacity for transporting bulk materials</li>
                    <li>Highly maneuverable, making them ideal for construction sites</li>
                    <li>Cost-effective and time-saving for large-scale projects</li>
                </ul>
            </section>
        </div>
        <div class="footer">
            <p>&copy; 2025 EGJ SERVICES GROUP. All rights reserved.</p>
        </div>
    </div>
</body>
</html>
