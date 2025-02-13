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
        body {
            font-family: Arial, sans-serif;
            background: #f4f4f9;
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
        }
        .container {
            width: 100%;
            max-width: 1200px;
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            animation: fadeIn 1.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .header {
            background: #4b79a1;
            background: linear-gradient(to right, #283e51, #4b79a1);
            color: #fff;
            text-align: center;
            padding: 40px 20px;
        }
        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            animation: slideIn 1s ease-in-out;
        }
        @keyframes slideIn {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .header p {
            font-size: 1.2em;
            margin-bottom: 20px;
        }
        .header img {
            width: 100%;
            max-width: 600px;
            border-radius: 10px;
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
            padding: 20px;
        }
        .section {
            flex: 1 1 300px;
            margin: 20px;
            padding: 20px;
            background: #f9f9f9;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease-in-out;
        }
        .section:hover {
            transform: scale(1.05);
        }
        .section h2 {
            color: #4b79a1;
            margin-bottom: 15px;
        }
        .section p {
            font-size: 1em;
            line-height: 1.6;
            margin-bottom: 15px;
        }
        .section img {
            width: 100%;
            border-radius: 10px;
            margin-bottom: 15px;
            transition: transform 0.3s ease-in-out;
        }
        .section img:hover {
            transform: scale(1.05);
        }
        .section ul {
            list-style-type: disc;
            padding-left: 20px;
            text-align: left;
        }
        .section ul li {
            margin-bottom: 10px;
        }
        .button {
            display: inline-block;
            background-color: #4b79a1;
            color: #fff;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }
        .button:hover {
            background-color: #283e51;
        }
        .footer {
            text-align: center;
            padding: 20px;
            background: #fff;
            margin-top: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2em;
            }
            .header p {
                font-size: 1em;
            }
            .section {
                margin: 10px;
                padding: 15px;
            }
            .section h2 {
                font-size: 1.5em;
            }
            
