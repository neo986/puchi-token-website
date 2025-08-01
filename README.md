
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>$PUCHI Token - La Revolución Crypto Canina</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        :root {
            --primary: #4e54c8;
            --secondary: #8f94fb;
            --accent: #ff6b6b;
            --accent2: #4cd964;
            --dark: #1a1a2e;
            --darker: #0f0f1f;
            --light: #f8f9fa;
            --gold: #ffd700;
            --gold-light: #ffec8b;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(135deg, var(--darker) 0%, var(--dark) 100%);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header */
        header {
            padding: 15px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            background: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(143, 148, 251, 0.2);
            transition: all 0.4s ease;
        }
        
        header.scrolled {
            padding: 10px 0;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo img {
            height: 50px;
            border-radius: 50%;
            border: 2px solid var(--gold);
            transition: transform 0.3s ease;
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
        }
        
        .logo:hover img {
            transform: rotate(15deg);
        }
        
        .logo h1 {
            font-size: 1.8rem;
            background: linear-gradient(to right, var(--gold), var(--gold-light));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 800;
            text-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        nav a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            position: relative;
        }
        
        nav a:hover {
            color: var(--gold);
        }
        
        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--gold);
            transition: width 0.3s ease;
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            padding: 180px 0 100px;
            position: relative;
            overflow: hidden;
            min-height: 100vh;
            display: flex;
            align-items: center;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(143,148,251,0.1) 0%, rgba(26,26,46,0) 70%);
            z-index: -1;
            animation: pulse 8s infinite ease-in-out;
        }
        
        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 50px;
            position: relative;
            z-index: 2;
        }
        
        .hero-text {
            flex: 1;
            animation: fadeInLeft 1s ease;
        }
        
        .hero-image {
            flex: 1;
            text-align: center;
            animation: fadeInRight 1s ease;
        }
        
        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero h2 span {
            background: linear-gradient(to right, var(--gold), var(--gold-light));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 30px;
            color: #e0e0ff;
        }
        
        .hero-highlight {
            color: var(--gold);
            font-weight: 600;
            position: relative;
        }
        
        .hero-highlight::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 100%;
            height: 3px;
            background: var(--gold);
            border-radius: 2px;
        }
        
        .puchi-container {
            max-width: 100%;
            position: relative;
            display: inline-block;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
            border: 3px solid var(--gold);
            animation: float 6s infinite ease-in-out;
        }
        
        .puchi-container img {
            max-width: 100%;
            display: block;
            transition: all 0.4s ease;
        }
        
        .puchi-container:hover img {
            transform: scale(1.05);
            box-shadow: 0 25px 50px rgba(255, 215, 0, 0.3);
        }
        
        .hero-buttons {
            display: flex;
            gap: 20px;
            margin-top: 40px;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            gap: 10px;
            position: relative;
            overflow: hidden;
        }
        
        .btn i {
            transition: transform 0.3s ease;
        }
        
        .btn:hover i {
            transform: translateX(5px);
        }
        
        .btn-primary {
            background: linear-gradient(to right, var(--gold), #ffa500);
            color: #1a1a2e;
            box-shadow: 0 5px 15px rgba(255, 215, 0, 0.4);
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 215, 0, 0.6);
        }
        
        .btn-outline {
            background: transparent;
            color: var(--gold);
            border: 2px solid var(--gold);
        }
        
        .btn-outline:hover {
            background: rgba(255, 215, 0, 0.1);
            transform: translateY(-3px);
        }
        
        .floating-dog {
            position: absolute;
            z-index: 1;
            opacity: 0.1;
            animation: float 6s infinite ease-in-out;
        }
        
        .floating-dog:nth-child(1) {
            top: 10%;
            left: 10%;
            width: 80px;
            animation-delay: 0s;
        }
        
        .floating-dog:nth-child(2) {
            top: 30%;
            right: 15%;
            width: 60px;
            animation-delay: 1s;
        }
        
        .floating-dog:nth-child(3) {
            bottom: 20%;
            left: 20%;
            width: 70px;
            animation-delay: 2s;
        }
        
        .floating-dog:nth-child(4) {
            bottom: 15%;
            right: 25%;
            width: 50px;
            animation-delay: 3s;
        }
        
        /* Tokenomics Section */
        .section {
            padding: 100px 0;
            position: relative;
        }
        
        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title {
            font-size: 2.5rem;
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--gold), var(--gold-light));
            border-radius: 2px;
        }
        
        .section-subtitle {
            font-size: 1.2rem;
            color: var(--gold-light);
            max-width: 700px;
            margin: 20px auto 0;
        }
        
        .tokenomics-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .token-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            transition: all 0.4s ease;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 215, 0, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .token-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--gold);
            transform: translateY(-100%);
            transition: transform 0.4s ease;
        }
        
        .token-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .token-card:hover::before {
            transform: translateY(0);
        }
        
        .token-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--gold);
            transition: transform 0.3s ease;
        }
        
        .token-card:hover .token-icon {
            transform: scale(1.2);
        }
        
        .token-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--gold);
        }
        
        .token-card p {
            color: #e0e0ff;
        }
        
        .progress-container {
            margin-top: 20px;
        }
        
        .progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
            font-size: 0.9rem;
        }
        
        .progress-bar {
            height: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            overflow: hidden;
        }
        
        .progress-fill {
            height: 100%;
            border-radius: 5px;
            width: 0;
            transition: width 1.5s ease-in-out;
        }
        
        .team-progress {
            background: linear-gradient(to right, var(--gold), #ffa500);
        }
        
        .burn-progress {
            background: linear-gradient(to right, #ff6b6b, #ff8e8e);
        }
        
        .hold-progress {
            background: linear-gradient(to right, var(--accent2), #5de887);
        }
        
        .chart-container {
            max-width: 600px;
            margin: 50px auto 0;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 215, 0, 0.1);
        }
        
        /* How to Buy */
        .howtobuy {
            background: rgba(0,0,0,0.2);
            position: relative;
            overflow: hidden;
        }
        
        .howtobuy::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(255,215,0,0.05) 0%, rgba(26,26,46,0) 70%);
            z-index: -1;
        }
        
        .steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .step {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 40px 25px 25px;
            text-align: center;
            position: relative;
            border: 1px solid rgba(255, 215, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        .step:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.08);
        }
        
        .step-number {
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 40px;
            height: 40px;
            background: linear-gradient(to right, var(--gold), #ffa500);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.2rem;
            box-shadow: 0 4px 10px rgba(255, 215, 0, 0.4);
        }
        
        .step-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--gold);
        }
        
        .step h3 {
            margin: 0 0 15px;
            font-size: 1.4rem;
            color: var(--gold);
        }
        
        /* Roadmap */
        .roadmap {
            position: relative;
            margin-top: 50px;
        }
        
        .roadmap::before {
            content: '';
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 4px;
            height: 100%;
            background: var(--gold);
        }
        
        .roadmap-item {
            display: flex;
            margin-bottom: 50px;
            position: relative;
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }
        
        .roadmap-item.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .roadmap-item:nth-child(even) {
            flex-direction: row-reverse;
        }
        
        .roadmap-content {
            width: calc(50% - 40px);
            padding: 25px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border: 1px solid rgba(255, 215, 0, 0.1);
            position: relative;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .roadmap-content::before {
            content: '';
            position: absolute;
            top: 20px;
            width: 20px;
            height: 20px;
            background: var(--gold);
            transform: rotate(45deg);
        }
        
        .roadmap-item:nth-child(odd) .roadmap-content::before {
            right: -10px;
        }
        
        .roadmap-item:nth-child(even) .roadmap-content::before {
            left: -10px;
        }
        
        .roadmap-content h3 {
            color: var(--gold);
            margin-bottom: 15px;
            font-size: 1.4rem;
        }
        
        .roadmap-content ul {
            padding-left: 20px;
            margin-top: 15px;
        }
        
        .roadmap-content li {
            margin-bottom: 10px;
            position: relative;
            padding-left: 15px;
            color: #e0e0ff;
        }
        
        .roadmap-content li::before {
            content: '?';
            position: absolute;
            left: 0;
            color: var(--accent2);
            font-weight: bold;
        }
        
        .roadmap-marker {
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 30px;
            height: 30px;
            background: var(--gold);
            border-radius: 50%;
            border: 4px solid var(--dark);
            z-index: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--dark);
            font-size: 0.8rem;
            font-weight: bold;
            box-shadow: 0 0 0 8px rgba(255, 215, 0, 0.2);
        }
        
        /* Community Section */
        .community {
            background: linear-gradient(135deg, #0a0a14 0%, #1a1a2e 100%);
            text-align: center;
            padding: 100px 0;
        }
        
        .community-stats {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 40px;
            margin: 60px 0;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            min-width: 200px;
            border: 1px solid rgba(255, 215, 0, 0.1);
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--gold), var(--gold-light));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }
        
        .stat-label {
            color: var(--gold-light);
            font-size: 1.1rem;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }
        
        .social-icon {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: var(--gold);
            font-size: 1.5rem;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .social-icon:hover {
            background: var(--gold);
            color: var(--dark);
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(255, 215, 0, 0.4);
        }
        
        /* FAQ Section */
        .faq {
            background: rgba(0,0,0,0.1);
        }
        
        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .faq-item {
            margin-bottom: 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid rgba(255, 215, 0, 0.1);
        }
        
        .faq-question {
            padding: 20px;
            font-weight: 600;
            font-size: 1.2rem;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: var(--gold);
        }
        
        .faq-question::after {
            content: '+';
            font-size: 1.5rem;
            transition: transform 0.3s ease;
        }
        
        .faq-item.active .faq-question::after {
            transform: rotate(45deg);
        }
        
        .faq-answer {
            padding: 0 20px;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease, padding 0.3s ease;
            color: #e0e0ff;
        }
        
        .faq-item.active .faq-answer {
            padding: 0 20px 20px;
            max-height: 300px;
        }
        
        /* Footer */
        footer {
            background: rgba(10, 10, 20, 0.95);
            padding: 80px 0 30px;
            position: relative;
        }
        
        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(to right, var(--gold), var(--gold-light));
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
        }
        
        .footer-logo {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .footer-logo img {
            height: 50px;
            border-radius: 50%;
            border: 2px solid var(--gold);
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.3);
        }
        
        .footer-logo h3 {
            font-size: 1.5rem;
            background: linear-gradient(to right, var(--gold), var(--gold-light));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .footer-links h4 {
            margin-bottom: 20px;
            font-size: 1.3rem;
            color: var(--gold);
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: var(--gold-light);
            text-decoration: none;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .footer-links a:hover {
            color: var(--gold);
            transform: translateX(5px);
        }
        
        .footer-links a i {
            font-size: 0.8rem;
            color: var(--gold);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            margin-top: 60px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gold-light);
            font-size: 0.9rem;
        }
        
        /* Animaciones */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeInLeft {
            from {
                opacity: 0;
                transform: translateX(-30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        @keyframes fadeInRight {
            from {
                opacity: 0;
                transform: translateX(30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        @keyframes pulse {
            0% {
                transform: scale(1);
                opacity: 0.8;
            }
            50% {
                transform: scale(1.1);
                opacity: 0.5;
            }
            100% {
                transform: scale(1);
                opacity: 0.8;
            }
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-20px) rotate(5deg);
            }
            100% {
                transform: translateY(0) rotate(0deg);
            }
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .hero-text, .hero-image {
                width: 100%;
            }
            
            .hero-buttons {
                justify-content: center;
            }
            
            .roadmap::before {
                left: 30px;
            }
            
            .roadmap-item,
            .roadmap-item:nth-child(even) {
                flex-direction: column;
                align-items: flex-start;
                padding-left: 60px;
            }
            
            .roadmap-content {
                width: 100%;
            }
            
            .roadmap-marker {
                left: 30px;
            }
            
            .roadmap-item:nth-child(odd) .roadmap-content::before,
            .roadmap-item:nth-child(even) .roadmap-content::before {
                top: -10px;
                left: 20px;
                transform: rotate(45deg);
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                gap: 15px;
            }
            
            .hero {
                padding: 150px 0 80px;
            }
            
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .section {
                padding: 70px 0;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 576px) {
            .header-content {
                flex-direction: column;
                gap: 15px;
            }
            
            nav ul {
                gap: 10px;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .logo h1 {
                font-size: 1.5rem;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .community-stats {
                gap: 20px;
            }
            
            .stat-card {
                min-width: 150px;
                padding: 20px;
            }
            
            .stat-number {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <img src="https://i.postimg.cc/56sxY4vf/puchi-token.png" alt="Puchi Token Logo">
                    <h1>$PUCHI</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#tokenomics">Tokenomics</a></li>
                        <li><a href="#howtobuy">Cómo Comprar</a></li>
                        <li><a href="#roadmap">Roadmap</a></li>
                        <li><a href="#community">Comunidad</a></li>
                        <li><a href="#faq">FAQ</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="floating-dog">
            <i class="fas fa-dog" style="color: #ffd700;"></i>
        </div>
        <div class="floating-dog">
            <i class="fas fa-paw" style="color: #ff6b6b;"></i>
        </div>
        <div class="floating-dog">
            <i class="fas fa-bone" style="color: #4cd964;"></i>
        </div>
        <div class="floating-dog">
            <i class="fas fa-dog" style="color: #8f94fb;"></i>
        </div>
        
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h2>La Revolución <span>Crypto Canina</span> ha Llegado</h2>
                    <p>Únete al movimiento token, <span class="hero-highlight">el año dorado del perro se acerca...</span></p>
                    <p>Suministro Total: <span class="hero-highlight">1,000,000,000,000 PUCHI</span></p>
                    
                    <div class="hero-buttons">
                        <a href="#" class="btn btn-primary" title="Comprar en PancakeSwap">
                            <i class="fas fa-shopping-cart"></i> Comprar Ahora
                        </a>
                        <a href="#" class="btn btn-outline" title="Ver contrato en BscScan">
                            <i class="fas fa-file-contract"></i> Ver Contrato
                        </a>
                    </div>
                </div>
                
                <div class="hero-image">
                    <div class="puchi-container">
                        <img src="https://i.postimg.cc/nhgSZ8Nm/puchi-front.jpg" alt="Puchi Token">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Tokenomics Section -->
    <section class="section" id="tokenomics">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Tokenomics</h2>
                <p class="section-subtitle">Distribución transparente diseñada para el crecimiento sostenible</p>
            </div>
            
            <div class="tokenomics-grid">
                <div class="token-card">
                    <div class="token-icon">
                        <i class="fas fa-fire"></i>
                    </div>
                    <h3>Quema Programada</h3>
                    <p>25% del suministro total será quemado automáticamente a los 30 días del lanzamiento</p>
                    <div class="progress-container">
                        <div class="progress-label">
                            <span>250B Tokens</span>
                            <span>25%</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress-fill burn-progress"></div>
                        </div>
                    </div>
                </div>
                
                <div class="token-card">
                    <div class="token-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Equipo Fundador</h3>
                    <p>20% reservado para el equipo fundador para desarrollo continuo</p>
                    <div class="progress-container">
                        <div class="progress-label">
                            <span>200B Tokens</span>
                            <span>20%</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress-fill team-progress"></div>
                        </div>
                    </div>
                </div>
                
                <div class="token-card">
                    <div class="token-icon">
                        <i class="fas fa-gift"></i>
                    </div>
                    <h3>Holding & Airdrops</h3>
                    <p>55% destinado a recompensas, airdrops y reserva estratégica</p>
                    <div class="progress-container">
                        <div class="progress-label">
                            <span>550B Tokens</span>
                            <span>55%</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress-fill hold-progress"></div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="chart-container">
                <canvas id="tokenChart"></canvas>
            </div>
        </div>
    </section>

    <!-- How to Buy Section -->
    <section class="section howtobuy" id="howtobuy">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Cómo Comprar $PUCHI</h2>
                <p class="section-subtitle">Sigue estos sencillos pasos para unirte a la revolución Puchi</p>
            </div>
            
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <div class="step-icon">
                        <i class="fab fa-metamask"></i>
                    </div>
                    <h3>Configura tu Wallet</h3>
                    <p>Instala MetaMask y configúrala para la red Binance Smart Chain</p>
                </div>
                
                <div class="step">
                    <div class="step-number">2</div>
                    <div class="step-icon">
                        <i class="fas fa-coins"></i>
                    </div>
                    <h3>Obtén BNB</h3>
                    <p>Compra BNB en un exchange y envíalo a tu wallet</p>
                </div>
                
                <div class="step">
                    <div class="step-number">3</div>
                    <div class="step-icon">
                        <i class="fas fa-exchange-alt"></i>
                    </div>
                    <h3>Conecta a PancakeSwap</h3>
                    <p>Ve a PancakeSwap y conecta tu wallet</p>
                </div>
                
                <div class="step">
                    <div class="step-number">4</div>
                    <div class="step-icon">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <h3>Compra $PUCHI</h3>
                    <p>Ingresa nuestro contrato y completa la compra</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Roadmap Section -->
    <section class="section" id="roadmap">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Roadmap</h2>
                <p class="section-subtitle">Nuestro plan estratégico para el crecimiento de $PUCHI</p>
            </div>
            
            <div class="roadmap">
                <div class="roadmap-item">
                    <div class="roadmap-content">
                        <h3>Fase 1: Lanzamiento (Q3 2025)</h3>
                        <ul>
                            <li>Despliegue del contrato inteligente</li>
                            <li>Creación de liquidez inicial</li>
                            <li>Lanzamiento de sitio web y redes sociales</li>
                            <li>Campaña de marketing inicial</li>
                        </ul>
                    </div>
                    <div class="roadmap-marker">Q3</div>
                </div>
                
                <div class="roadmap-item">
                    <div class="roadmap-content">
                        <h3>Fase 2: Crecimiento (Q4 2025)</h3>
                        <ul>
                            <li>Evento de quema del 25% de tokens</li>
                            <li>Listado en CoinGecko y CoinMarketCap</li>
                            <li>Primer airdrop masivo a holders</li>
                            <li>Alianzas estratégicas con influencers</li>
                        </ul>
                    </div>
                    <div class="roadmap-marker">Q4</div>
                </div>
                
                <div class="roadmap-item">
                    <div class="roadmap-content">
                        <h3>Fase 3: Expansión (Q1 2026)</h3>
                        <ul>
                            <li>Lanzamiento de NFTs coleccionables</li>
                            <li>Sistema de staking con recompensas</li>
                            <li>Integración con plataformas DeFi</li>
                            <li>Primer evento comunitario presencial</li>
                        </ul>
                    </div>
                    <div class="roadmap-marker">Q1</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Community Section -->
    <section class="section community" id="community">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Nuestra Comunidad</h2>
                <p class="section-subtitle">Únete a miles de holders apasionados por la revolución crypto canina</p>
            </div>
            
            <div class="community-stats">
                <div class="stat-card">
                    <div class="stat-number">12.5K</div>
                    <div class="stat-label">Holders</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">8.2K</div>
                    <div class="stat-label">Telegram</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">25.7K</div>
                    <div class="stat-label">Twitter</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">4.3K</div>
                    <div class="stat-label">Discord</div>
                </div>
            </div>
            
            <div class="social-icons">
                <a href="#" class="social-icon" title="Telegram">
                    <i class="fab fa-telegram"></i>
                </a>
                <a href="#" class="social-icon" title="Twitter">
                    <i class="fab fa-twitter"></i>
                </a>
                <a href="#" class="social-icon" title="Discord">
                    <i class="fab fa-discord"></i>
                </a>
                <a href="#" class="social-icon" title="Reddit">
                    <i class="fab fa-reddit"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="section faq" id="faq">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Preguntas Frecuentes</h2>
                <p class="section-subtitle">Encuentra respuestas a las preguntas más comunes sobre $PUCHI</p>
            </div>
            
            <div class="faq-container">
                <div class="faq-item">
                    <div class="faq-question">¿Qué es $PUCHI Token?</div>
                    <div class="faq-answer">
                        <p>$PUCHI es un token deflacionario basado en Binance Smart Chain que combina la pasión por las criptomonedas con el amor por los perros. Con un enfoque en la comunidad y utilidad real, $PUCHI busca crear una revolución en el espacio crypto.</p>
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">¿Cómo puedo comprar $PUCHI?</div>
                    <div class="faq-answer">
                        <p>Puedes comprar $PUCHI en PancakeSwap siguiendo estos pasos:</p>
                        <ol>
                            <li>Configura MetaMask para Binance Smart Chain</li>
                            <li>Compra BNB en un exchange</li>
                            <li>Envía los BNB a tu MetaMask</li>
                            <li>Conéctate a PancakeSwap</li>
                            <li>Ingresa el contrato de $PUCHI y realiza el swap</li>
                        </ol>
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">¿Qué utilidad tiene $PUCHI?</div>
                    <div class="faq-answer">
                        <p>$PUCHI tiene múltiples utilidades planificadas:</p>
                        <ul>
                            <li>Sistema de staking con recompensas</li>
                            <li>NFTs coleccionables de perros</li>
                            <li>Acceso a eventos exclusivos para holders</li>
                            <li>Plataforma de caridad para refugios caninos</li>
                            <li>Marketplace de productos para mascotas</li>
                        </ul>
                    </div>
                </div>
                
                <div class="faq-item">
                    <div class="faq-question">¿Qué hace único a $PUCHI?</div>
                    <div class="faq-answer">
                        <p>$PUCHI se diferencia por:</p>
                        <ul>
                            <li>Comunidad activa y apasionada</li>
                            <li>Tokenomics diseñada para crecimiento sostenible</li>
                            <li>Plan de desarrollo claro y transparente</li>
                            <li>Enfoque en utilidad real y adopción masiva</li>
                            <li>Compromiso con causas benéficas para animales</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-info">
                    <div class="footer-logo">
                        <img src="https://i.postimg.cc/56sxY4vf/puchi-token.png" alt="Puchi Token Logo">
                        <h3>$PUCHI Token</h3>
                    </div>
                    <p>La revolución crypto canina está aquí. El año dorado del perro se acerca...</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-telegram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-discord"></i></a>
                        <a href="#"><i class="fab fa-reddit"></i></a>
                    </div>
                </div>
                
                <div class="footer-links">
                    <h4>Enlaces Rápidos</h4>
                    <ul>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Comprar $PUCHI</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Contrato Inteligente</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Gráficos en Tiempo Real</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Documentación</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h4>Recursos</h4>
                    <ul>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> PancakeSwap</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> BscScan</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> CoinGecko</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> CoinMarketCap</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h4>Legal</h4>
                    <ul>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Términos y Condiciones</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Política de Privacidad</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Descargo de Responsabilidad</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2025 $PUCHI Token IA. Todos los derechos reservados. La inversión en criptoactivos no está regulada, puede no ser adecuada para inversores minoristas y perderse la totalidad del importe invertido.</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Sticky header
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Animate progress bars on scroll
        const progressBars = document.querySelectorAll('.progress-fill');
        progressBars.forEach(bar => {
            bar.style.width = bar.classList.contains('team-progress') ? '20%' : 
                             bar.classList.contains('burn-progress') ? '25%' : '55%';
        });
        
        // Animate roadmap items on scroll
        const roadmapItems = document.querySelectorAll('.roadmap-item');
        
        function checkScroll() {
            roadmapItems.forEach(item => {
                const position = item.getBoundingClientRect();
                if (position.top < window.innerHeight * 0.8) {
                    item.classList.add('visible');
                }
            });
        }
        
        window.addEventListener('scroll', checkScroll);
        window.addEventListener('load', checkScroll);
        
        // Tokenomics chart
        const ctx = document.getElementById('tokenChart').getContext('2d');
        const tokenChart = new Chart(ctx, {
            type: 'doughnut',
            data: {
                labels: ['Quema Programada', 'Equipo Fundador', 'Holding & Airdrops'],
                datasets: [{
                    data: [25, 20, 55],
                    backgroundColor: [
                        '#ff6b6b',
                        '#ffd700',
                        '#4cd964'
                    ],
                    borderWidth: 0,
                    hoverOffset: 15
                }]
            },
            options: {
                responsive: true,
                plugins: {
                    legend: {
                        position: 'bottom',
                        labels: {
                            color: '#e0e0ff',
                            font: {
                                size: 14,
                                family: "'Roboto', sans-serif"
                            },
                            padding: 20
                        }
                    },
                    tooltip: {
                        backgroundColor: 'rgba(26, 26, 46, 0.9)',
                        titleFont: {
                            family: "'Poppins', sans-serif"
                        },
                        bodyFont: {
                            family: "'Roboto', sans-serif"
                        },
                        padding: 12,
                        displayColors: false,
                        callbacks: {
                            label: function(context) {
                                return `${context.label}: ${context.parsed}%`;
                            }
                        }
                    }
                }
            }
        });
        
        // FAQ accordion
        const faqItems = document.querySelectorAll('.faq-item');
        
        faqItems.forEach(item => {
            const question = item.querySelector('.faq-question');
            question.addEventListener('click', () => {
                const isActive = item.classList.contains('active');
                
                // Close all items
                faqItems.forEach(i => i.classList.remove('active'));
                
                // Open clicked item if it was closed
                if (!isActive) {
                    item.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
