<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مدرسة سان الافتراضية | SAN Virtual School</title>
    <meta name="description" content="مدرسة سان الافتراضية - تعليم إلكتروني متكامل لجميع المراحل الدراسية بأحدث التقنيات">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #0056b3;
            --secondary: #00d4aa;
            --dark: #121212;
            --light: #f8f9fa;
            --gray: #6c757d;
        }
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Cairo', sans-serif; line-height: 1.7; color: #333; background: #fff; }
        .en body { font-family: 'Poppins', sans-serif; }
        
        /* Header & Navbar */
        header {
            background: linear-gradient(135deg, var(--primary), #003d82);
            color: white;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
        }
        
        .logo {
            font-size: 28px;
            font-weight: 900;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo i { color: var(--secondary); }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            transition: 0.3s;
            position: relative;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 50%;
            background: var(--secondary);
            transition: 0.3s;
            transform: translateX(-50%);
        }
        
        .nav-links a:hover::after { width: 100%; }
        
        .lang-toggle {
            background: var(--secondary);
            color: #000;
            border: none;
            padding: 8px 15px;
            border-radius: 30px;
            font-weight: bold;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            padding: 120px 5% 80px;
            background: linear-gradient(rgba(0,86,179,0.9), rgba(0,61,130,0.9)), url('https://images.unsplash.com/photo-1524178232363-1fb2b075b655?ixlib=rb-4.0.3&auto=format&fit=crop&q=80') center/cover;
            color: white;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background: var(--secondary);
            color: #000;
            padding: 14px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
            margin: 10px;
        }
        
        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,212,170,0.3);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid white;
            color: white;
        }
        
        /* Features */
        .features {
            padding: 100px 5%;
            background: #f8f9fa;
            text-align: center;
        }
        
        .section-title {
            font-size: 2.8rem;
            margin-bottom: 60px;
            color: var(--primary);
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .feature-card {
            background: white;
            padding: 40px 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }
        
        .feature-card i {
            font-size: 3.5rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }
        
        /* Stats */
        .stats {
            padding: 80px 5%;
            background: var(--primary);
            color: white;
            text-align: center;
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
        }
        
        .stat-item h3 {
            font-size: 3rem;
            margin-bottom: 10px;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 80px 5% 30px;
        }
        
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }
        
        .footer-logo {
            font-size: 2.5rem;
            font-weight: 900;
            margin-bottom: 20px;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            margin: 0 10px;
            transition: 0.3s;
        }
        
        .social-links a:hover { color: var(--secondary); }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #333;
            color: #aaa;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .navbar { flex-direction: column; padding: 1rem; }
            .nav-links { margin-top: 20px; gap: 20px; }
            .hero h1 { font-size: 2.5rem; }
            .hero p { font-size: 1.1rem; }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <nav class="navbar">
            <div class="logo">
                <i class="fas fa-graduation-cap"></i>
                <span>SAN School</span>
            </div>
            <div class="nav-links">
                <a href="#home">الرئيسية</a>
                <a href="#features">مميزاتنا</a>
                <a href="#about">عن المدرسة</a>
                <a href="#contact">تواصل معنا</a>
                <a href="login.html">تسجيل الدخول</a>
            </div>
            <button class="lang-toggle" onclick="toggleLanguage()">EN</button>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <h1>مدرسة سان الافتراضية</h1>
        <h2 class="en-title" style="display:none;">SAN Virtual School</h2>
        <p>تعلم من أي مكان وفي أي وقت مع أفضل المعلمين وأحدث التقنيات التعليمية</p>
        <p class="en-desc" style="display:none;">Learn from anywhere, anytime with the best teachers and latest educational technologies</p>
        <div>
            <a href="#register" class="btn">ابدأ الآن</a>
            <a href="#tour" class="btn btn-outline">جولة في المدرسة</a>
        </div>
    </section>

    <!-- Features -->
    <section class="features" id="features">
        <h2 class="section-title">مميزات مدرسة سان الافتراضية</h2>
        <h2 class="section-title en-title" style="display:none;">Why Choose SAN Virtual School?</h2>
        
        <div class="features-grid">
            <div class="feature-card">
                <i class="fas fa-video"></i>
                <h3>دروس مباشرة عالية الجودة</h3>
                <p>حصص يومية مباشرة مع تفاعل كامل مع المعلم والطلاب</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-book-open"></i>
                <h3>مناهج معتمدة دولياً</h3>
                <p>مناه
                </html>
