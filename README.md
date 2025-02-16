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
        /* Reset and Base Styles */
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
            color: #e0e0e0;
        }
        header {
            background: rgba(255, 255, 255, 0.9);
            padding: 15px;
            display: flex;
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
            padding: 0;
            margin: 0;
        }
        nav ul li {
            margin: 0 20px;
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
            display: flex;
            align-items: center;
        }
        .search-bar input {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            width: 200px;
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
            margin-right: 20px;
            transition: background 0.3s;
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
            content: \"\";\n            position: absolute;\n            top: 0;\n            left: 0;\n            right: 0;\n            bottom: 0;\n            background: rgba(0,0,0,0.5);\n        }\n        .hero > * {\n            position: relative;\n            z-index: 2;\n        }\n        .hero h1 {\n            font-size: 48px;\n            margin-bottom: 20px;\n            transition: color 0.3s;\n        }\n        body.dark-mode .hero h1 {\n            color: #fff;\n        }\n        .hero p {\n            font-size: 24px;\n            margin-bottom: 30px;\n        }\n        .btn {\n            background: #007BFF;\n            color: white;\n            padding: 15px 30px;\n            text-decoration: none;\n            border-radius: 8px;\n            font-size: 20px;\n            font-weight: bold;\n            box-shadow: 3px 3px 15px rgba(0,0,0,0.2);\n            transition: background 0.3s, transform 0.3s;\n        }\n        .btn:hover {\n            background: #0056b3;\n            transform: translateY(-3px);\n        }\n        /* Dynamic Boxes for Sections */\n        .dynamic-box {\n            background: rgba(255,255,255,0.8);\n            padding: 40px;\n            margin: 30px auto;\n            border-radius: 8px;\n            width: 90%;\n            max-width: 1200px;\n            box-shadow: 0 4px 12px rgba(0,0,0,0.1);\n            transition: transform 0.3s, background 0.3s;\n        }\n        .dark-mode .dynamic-box {\n            background: rgba(50,50,50,0.9);\n        }\n        .dynamic-box h2 {\n            font-size: 32px;\n            margin-bottom: 20px;\n            transition: color 0.3s;\n        }\n        body.dark-mode .dynamic-box h2 {\n            color: #fff;\n        }\n        /* Service Cards */\n        .service-container {\n            display: flex;\n            flex-wrap: wrap;\n            justify-content: space-around;\n        }\n        .service-card {\n            background: white;\n            padding: 20px;\n            border-radius: 8px;\n            width: 30%;\n            margin: 15px;\n            box-shadow: 0 4px 10px rgba(0,0,0,0.1);\n            text-align: center;\n            transition: transform 0.3s, box-shadow 0.3s;\n        }\n        .service-card:hover {\n            transform: translateY(-5px);\n            box-shadow: 0 8px 20px rgba(0,0,0,0.2);\n        }\n        .service-card img {\n            max-width: 100%;\n            border-radius: 8px;\n            margin-bottom: 15px;\n        }\n        /* Google Maps Container */\n        #google-map {\n            width: 100%;\n            height: 400px;\n            border: none;\n            border-radius: 8px;\n        }\n        /* Footer */\n        footer {\n            text-align: center;\n            padding: 20px;\n            background: #007BFF;\n            color: white;\n            transition: background 0.3s;\n        }\n        /* Responsive Adjustments */\n        @media (max-width: 768px) {\n            .service-card {\n                width: 90%;\n            }\n            nav ul li {\n                margin: 0 10px;\n            }\n        }\n    </style>\n</head>\n<body>\n    <header>\n        <div class=\"logo\">EGJ Services Group</div>\n        <nav>\n            <ul>\n                <li><a href=\"#services\">Services</a></li>\n                <li><a href=\"#about\">About Us</a></li>\n                <li><a href=\"#contact\">Contact</a></li>\n                <li><a href=\"#map\">Locations</a></li>\n            </ul>\n        </nav>\n        <button class=\"dark-mode-toggle\" onclick=\"toggleDarkMode()\">Toggle Dark Mode</button>\n        <div class=\"search-bar\">\n            <input type=\"text\" placeholder=\"Search...\">\n            <button><i class=\"fas fa-search\"></i></button>\n        </div>\n    </header>\n\n    <section class=\"hero dynamic-box\">\n        <h1>Reliable Construction Transportation Services</h1>\n        <p>Serving Palm Beach, St. Lucie, and Broward Counties.</p>\n        <a href=\"#contact\" class=\"btn\">Request a Quote</a>\n    </section>\n\n    <section id=\"services\" class=\"dynamic-box\">\n        <h2>Our Services</h2>\n        <p>We provide all kinds of aggregates, dirt, sand, trash, C&D, and hourly projects.</p>\n        <div class=\"service-container\">\n            <div class=\"service-card\">\n                <img src=\"images/dump-truck.jpg\" alt=\"Dump Truck\">\n                <h3>Material Transportation</h3>\n                <p>We transport aggregates, fill, concrete, asphalt, and more.</p>\n            </div>\n            <div class=\"service-card\">\n                <img src=\"images/construction-site.jpg\" alt=\"Construction Site\">\n                <h3>On-Site Deliveries</h3>\n                <p>Fast and efficient delivery to keep your project moving.</p>\n            </div>\n            <div class=\"service-card\">\n                <img src=\"images/machine-work.jpg\" alt=\"Machine Work\">\n                <h3>Excavation Services</h3>\n                <p>We offer excavation and land clearing services.</p>\n            </div>\n       