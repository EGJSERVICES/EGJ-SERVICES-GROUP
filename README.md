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
        /* Base Styles */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
            transition: background-color 0.3s, color 0.3s;
        }
        header {
            background: rgba(255, 255, 255, 0.9);
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .logo {
            font-size: 24px;
            font-weight: bold;
        }
        nav ul {
            list-style: none;
            display: flex;
            padding: 0;
            margin: 0;
        }
        nav ul li {
            margin: 0 15px;
        }
        nav ul li a {
            text-decoration: none;
            color: inherit;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: #007BFF;
        }
        .search-bar input {
            padding: 5px;
            width: 200px;
            border: 1px solid #ccc;
            border-radius: 3px;
        }
        .search-bar button {
            padding: 5px 10px;
            border: none;
            background-color: #007BFF;
            color: white;
            cursor: pointer;
            border-radius: 3px;
            margin-left: 5px;
            transition: background-color 0.3s;
        }
        .search-bar button:hover {
            background-color: #0056b3;
        }
        .hero {
            text-align: center;
            padding: 100px 20px;
            background-image: url('images/construction-site-background.jpg');
            background-size: cover;
            background-position: center;
            color: white;
            position: relative;
        }
        .hero::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            z-index: 1;
        }
        .hero h1, .hero p, .hero .btn {
            position: relative;
            z-index: 2;
        }
        .btn {
            background: #007BFF;
            color: white;
            padding: 15px 30px;
            text-decoration: none;
            border-radius: 5px;
            display: inline-block;
            margin-top: 20px;
            transition: background-color 0.3s, transform 0.3s;
        }
        .btn:hover {
            background-color: #0056b3;
            transform: translateY(-2px);
        }
        .service-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            padding: 50px 20px;
        }
        .service-card {
            background: white;
            padding: 20px;
            border-radius: 5px;
            width: 30%;
            margin: 15px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        .service-card:hover {
            transform: translateY(-5px);
        }
        .service-card img {
            max-width: 100%;
            border-radius: 5px;
        }
        footer {
            text-align: center;
            padding: 20px;
            background: #007BFF;
            color: white;
        }
        .dark-mode {
            background-color: #121212;
            color: #e0e0e0;
        }
        .dark-mode header {
            background: rgba(18, 18, 18, 0.9);
        }
        .dark-mode .btn {
            background: #1e88e5;
        }
        .dark-mode .btn:hover {
            background: #1565c0;
        }
        .dark-mode footer {
            background: #1e88e5;
        }
        .dark-mode nav ul li a:hover {
            color: #1e88e5;
        }
        .toggle-switch {
            position: absolute;
            top: 20px;
            right: 20px;
            display: flex;
            align-items: center;
            cursor: pointer;
        }
        .toggle-switch input {
            display: none;
        }
        .toggle-switch label {
            background-color: #ccc;
            border-radius: 50px;
            padding: 5px;
            width: 50px;
            height: 25px;
            position: relative;
            transition: background-color 0.3s;
        }
        .toggle-switch label::after {
            content: '';
            background-color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            position: absolute;
            top: 2.5px;
            left: 2.5px;
            transition: transform 0.3s;
        }
        . 
