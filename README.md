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
            text-align: center;
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
            display: flex;
            align-items: center;
            justify-content: center;
            height: 20vh;
        }
        @keyframes slideIn {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
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
        }
        p, ul {
            font-size: 18px;
            line-height: 1.8;
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
            <img src="construction-materials.jpg" alt="Construction Materials">
        </div>
        <div class="content">
            <section class="section contact">
                <h2>Contact Us</h2>
                <p>Email: <a href="mailto:egjttrucking@gmail.com">egjttrucking@gmail.com</a></p>
                <p>Phone: <a href="tel:5615068932">561-506-8932</a></p>
                <p>Address: PO BOX 
