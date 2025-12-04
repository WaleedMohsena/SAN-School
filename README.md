<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SAN School - مدرسة التعليم عن بعد</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
        }

        /* Header */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            right: 0;
            background: #667eea;
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .cta-button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 0.7rem 1.5rem;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(102, 126, 234, 0.4);
        }

        /* Hero Section */
        .hero {
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem 5%;
            color: white;
        }

        .hero-content {
            max-width: 800px;
            animation: fadeInUp 1s ease;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.95;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn-primary {
            background: white;
            color: #667eea;
            padding: 1rem 2.5rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 25px rgba(0,0,0,0.3);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            padding: 1rem 2.5rem;
            border: 2px solid white;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s;
        }

        .btn-secondary:hover {
            background: white;
            color: #667eea;
        }

        /* Features Section */
        .features {
            padding: 5rem 5%;
            background: white;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .feature-card {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 2rem;
            border-radius: 20px;
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            color: #667eea;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        /* Courses Section */
        .courses {
            padding: 5rem 5%;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
        }

        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .course-card {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            overflow: hidden;
            transition: transform 0.3s;
            color: #333;
        }

        .course-card:hover {
            transform: scale(1.05);
        }

        .course-image {
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
        }

        .course-content {
            padding: 1.5rem;
        }

        .course-card h3 {
            color: #667eea;
            margin-bottom: 0.5rem;
            font-size: 1.5rem;
        }

        .course-meta {
            display: flex;
            justify-content: space-between;
            margin-top: 1rem;
            padding-top: 1rem;
            border-top: 1px solid #eee;
            font-size: 0.9rem;
            color: #666;
        }

        /* Stats Section */
        .stats {
            padding: 5rem 5%;
            background: white;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .stat-item {
            padding: 2rem;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-label {
            color: #666;
            margin-top: 0.5rem;
            font-size: 1.1rem;
        }

        /* Contact Section */
        .contact {
            padding: 5rem 5%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .contact-container {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-form {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 20px;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: none;
            border-radius: 10px;
            font-family: inherit;
            font-size: 1rem;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .submit-btn {
            background: white;
            color: #667eea;
            padding: 1rem 3rem;
            border: none;
            border-radius: 25px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 1rem;
            width: 100%;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(0,0,0,0.3);
        }

        /* Footer */
        footer {
            background: #2d3748;
            color: white;
            padding: 3rem 5%;
            text-align: center;
        }

        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            color: #667eea;
            margin-bottom: 1rem;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.5rem;
        }

        .footer-section a {
            color: #cbd5e0;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-section a:hover {
            color: #667eea;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-top: 1rem;
        }

        .social-links a {
            font-size: 1.5rem;
        }

        .copyright {
            padding-top: 2rem;
            border-top: 1px solid #4a5568;
            color: #cbd5e0;
        }

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

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .hero-buttons {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">🎓 SAN School</div>
            <ul class="nav-links">
                <li><a href="#home">الرئيسية</a></li>
                <li><a href="#features">المميزات</a></li>
                <li><a href="#courses">الدورات</a></li>
                <li><a href="#contact">تواصل معنا</a></li>
            </ul>
            <a href="#register" class="cta-button">سجل الآن</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>مرحبًا بك في SAN School</h1>
            <p>منصة التعليم عن بعد الأولى - تعلم في أي وقت ومن أي مكان مع أفضل المعلمين</p>
            <div class="hero-buttons">
                <a href="#courses" class="btn-primary">استكشف الدورات</a>
                <a href="#contact" class="btn-secondary">تواصل معنا</a>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <h2 class="section-title">لماذا تختار SAN School؟</h2>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">📚</div>
                <h3>محتوى تعليمي متميز</h3>
                <p>مناهج دراسية حديثة ومتطورة تواكب احتياجات العصر</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">👨‍🏫</div>
                <h3>معلمون محترفون</h3>
                <p>نخبة من أفضل المعلمين ذوي الخبرة والكفاءة العالية</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">💻</div>
                <h3>منصة تفاعلية</h3>
                <p>تقنيات حديثة للتعليم التفاعلي والمباشر</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">🏆</div>
                <h3>شهادات معتمدة</h3>
                <p>احصل على شهادات معترف بها بعد إتمام الدورات</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">⏰</div>
                <h3>مرونة في المواعيد</h3>
                <p>تعلم في الوقت الذي يناسبك دون قيود</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">📱</div>
                <h3>متاح على جميع الأجهزة</h3>
                <p>ادرس من الكمبيوتر أو الهاتف أو التابلت</p>
            </div>
        </div>
    </section>

    <!-- Courses Section -->
    <section id="courses" class="courses">
        <h2 class="section-title">الدورات المتاحة</h2>
        <div class="courses-grid">
            <div class="course-card">
                <div class="course-image">🔢</div>
                <div class="course-content">
                    <h3>الرياضيات المتقدمة</h3>
                    <p>دورة شاملة في الرياضيات لجميع المستويات الدراسية</p>
                    <div class="course-meta">
                        <span>⏱️ 40 ساعة</span>
                        <span>👥 1,234 طالب</span>
                    </div>
                </div>
            </div>
            <div class="course-card">
                <div class="course-image">🔬</div>
                <div class="course-content">
                    <h3>العلوم والكيمياء</h3>
                    <p>استكشف عالم العلوم من خلال تجارب تفاعلية مشوقة</p>
                    <div class="course-meta">
                        <span>⏱️ 35 ساعة</span>
                        <span>👥 987 طالب</span>
                    </div>
                </div>
            </div>
            <div class="course-card">
                <div class="course-image">🌍</div>
                <div class="course-content">
                    <h3>اللغة الإنجليزية</h3>
                    <p>تعلم اللغة الإنجليزية بطريقة عصرية وممتعة</p>
                    <div class="course-meta">
                        <span>⏱️ 50 ساعة</span>
                        <span>👥 2,156 طالب</span>
                    </div>
                </div>
            </div>
            <div class="course-card">
                <div class="course-image">💻</div>
                <div class="course-content">
                    <h3>البرمجة للمبتدئين</h3>
                    <p>ابدأ رحلتك في عالم البرمجة وتطوير التطبيقات</p>
                    <div class="course-meta">
                        <span>⏱️ 60 ساعة</span>
                        <span>👥 1,876 طالب</span>
                    </div>
                </div>
            </div>
            <div class="course-card">
                <div class="course-image">📖</div>
                <div class="course-content">
                    <h3>اللغة العربية</h3>
                    <p>إتقان قواعد اللغة العربية والأدب والبلاغة</p>
                    <div class="course-meta">
                        <span>⏱️ 45 ساعة</span>
                        <span>👥 1,543 طالب</span>
                    </div>
                </div>
            </div>
            <div class="course-card">
                <div class="course-image">🎨</div>
                <div class="course-content">
                    <h3>الفنون والتصميم</h3>
                    <p>اكتشف موهبتك الفنية وطور مهاراتك الإبداعية</p>
                    <div class="course-meta">
                        <span>⏱️ 30 ساعة</span>
                        <span>👥 765 طالب</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <h2 class="section-title">إنجازاتنا بالأرقام</h2>
        <div class="stats-grid">
            <div class="stat-item">
                <div class="stat-number">15,000+</div>
                <div class="stat-label">طالب نشط</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">500+</div>
                <div class="stat-label">معلم محترف</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">200+</div>
                <div class="stat-label">دورة تعليمية</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">98%</div>
                <div class="stat-label">نسبة الرضا</div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="contact-container">
            <h2 class="section-title">تواصل معنا</h2>
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">الاسم الكامل</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">البريد الإلكتروني</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="phone">رقم الهاتف</label>
                    <input type="tel" id="phone" name="phone">
                </div>
                <div class="form-group">
                    <label for="message">رسالتك</label>
                    <textarea id="message" name="message" required></textarea>
                </div>
                <button type="submit" class="submit-btn">إرسال الرسالة</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>عن SAN School</h3>
                <p>منصة تعليمية متطورة تهدف إلى توفير تعليم عالي الجودة عن بعد لجميع الطلاب</p>
                <div class="social-links">
                    <a href="#">📘</a>
                    <a href="#">📷</a>
                    <a href="#">🐦</a>
                    <a href="#">📺</a>
                </div>
            </div>
            <div class="footer-section">
                <h3>روابط سريعة</h3>
                <ul>
                    <li><a href="#home">الرئيسية</a></li>
                    <li><a href="#features">المميزات</a></li>
                    <li><a href="#courses">الدورات</a></li>
                    <li><a href="#contact">تواصل معنا</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>معلومات التواصل</h3>
                <ul>
                    <li>📧 info@sanschool.com</li>
                    <li>📱 +201100294080</li>
                    <li>📍 المنصورة، مصر</li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2024 SAN School. جميع الحقوق محفوظة</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
   