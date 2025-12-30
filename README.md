
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sayura English Academy</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
        }

        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: transparent;
            transition: background 0.3s ease-in-out;
            z-index: 1000;
        }

        header.scrolled {
            background: #ffffff;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 20px 0;
        }

        nav ul li {
            margin: 0 20px;
        }

        nav ul li a {
            color: #ffffff;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease-in-out;
        }

        header.scrolled nav ul li a {
            color: #007BFF;
        }

        #hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://cdn.lakpura.com/images/LK9499C15D-03-E.JPG') center/cover no-repeat;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #ffffff;
            padding: 0 20px;
        }

        #hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }

        #hero p {
            font-size: 1.6rem;
            margin-bottom: 40px;
        }

        .btn {
            background: #007BFF;
            color: #ffffff;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s ease-in-out;
            box-shadow: 0 4px 15px rgba(0, 123, 255, 0.3);
        }

        .btn:hover {
            background: #0056b3;
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(0, 123, 255, 0.4);
        }

        section {
            padding: 100px 20px;
        }

        h2 {
            text-align: center;
            margin-bottom: 60px;
            font-size: 2.5rem;
            color: #007BFF;
        }

        #about {
            background: #f8f9fa;
        }

        #about .container {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .gallery img {
            width: 100%;
            height: auto;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.4s ease;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        #features {
            background: #ffffff;
        }

        .features-grid {
            display: flex;
            justify-content: center;
            gap: 50px;
            flex-wrap: wrap;
            max-width: 1200px;
            margin: 0 auto;
        }

        .feature {
            text-align: center;
            max-width: 350px;
        }

        .feature i {
            font-size: 4rem;
            color: #007BFF;
            margin-bottom: 20px;
            transition: transform 0.5s ease;
        }

        .feature:hover i {
            transform: rotate(360deg);
        }

        #pricing {
            background: #f8f9fa;
        }

        .pricing-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .pricing-card {
            background: #ffffff;
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.4s ease;
        }

        .pricing-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .pricing-card.special {
            background: linear-gradient(135deg, #007BFF, #0056b3);
            color: #ffffff;
            transform: scale(1.05);
        }

        .pricing-card.special:hover {
            transform: translateY(-15px) scale(1.1);
        }

        .pricing-card .price {
            font-size: 2.5rem;
            font-weight: 700;
            margin: 20px 0;
        }

        .pricing-card .original-price {
            text-decoration: line-through;
            opacity: 0.7;
            font-size: 1.2rem;
        }

        .discount-badge {
            background: #ff4757;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: inline-block;
            margin: 10px 0;
        }

        footer {
            background: #222;
            color: #ffffff;
            padding: 60px 20px 30px;
            text-align: center;
        }

        .contact-info {
            margin: 20px 0;
            font-size: 1.2rem;
        }

        .contact-info p {
            margin: 10px 0;
        }

        .social-icons a {
            color: #ffffff;
            margin: 0 15px;
            font-size: 1.8rem;
            transition: all 0.3s ease;
        }

        .social-icons a:hover {
            color: #007BFF;
            transform: translateY(-5px);
        }

        @media (max-width: 768px) {
            #hero h1 { font-size: 2.5rem; }
            #hero p { font-size: 1.2rem; }
            nav ul { flex-direction: column; }
            nav ul li { margin: 10px 0; }
        }
    </style>
</head>
<body>
    <header id="header">
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#pricing">Classes & Fees</a></li>
                <li><a href="#footer">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="hero" data-aos="fade-down">
        <h1>Sayura English Academy</h1>
        <p>Expert English Classes for All Grades & Levels<br>Physical & Online Classes Available</p>
        <a href="#pricing" class="btn">View Classes & Enroll</a>
    </section>

    <section id="about">
        <div class="container" data-aos="fade-up">
            <h2>About Sayura English Academy</h2>
            <p>Founded and led by experienced educator <strong>Mr. Tusitha Jayawardhena</strong>, Sayura English Academy is located in the serene surroundings of Dehiattakandiya. We provide high-quality, affordable English education for students of all ages through engaging physical classes and convenient online sessions via Zoom.</p>
            
            <h3 style="margin: 40px 0 20px;">Our Classroom Environment & Surroundings</h3>
            <div class="gallery">
                <img src="https://lookaside.instagram.com/seo/google_widget/crawler/?media_id=3469062618852170074" alt="Happy students in English class" data-aos="zoom-in">
                <img src="https://srilanka.un.org/sites/default/files/styles/large/public/2023-10/Students%20lined%20up%20and%20ready%20for%20classroom%20activities.jpg?h=b49a4b0e&itok=O6oYHbKH" alt="Students ready for class" data-aos="zoom-in" data-aos-delay="100">
                <img src="https://images.squarespace-cdn.com/content/v1/60c71940484f1a0d167f4151/af04e7e4-5d75-42fb-88f7-b02114799bf1/IMG_0813.jpg" alt="Modern classroom learning" data-aos="zoom-in" data-aos-delay="200">
                <img src="https://lookaside.fbsbx.com/lookaside/crawler/media/?media_id=10231396642031972" alt="Beautiful paddy fields in Dehiattakandiya" data-aos="zoom-in" data-aos-delay="300">
                <img src="https://bunny-wp-pullzone-3xue3q6yzy.b-cdn.net/wp-content/uploads/2024/10/iStock-1150384596-2.jpg" alt="Online Zoom English class" data-aos="zoom-in" data-aos-delay="400">
                <img src="https://lanquill.com/static/media/How%20Modern%20English%20Language%20Labs%20Are%20Transforming%20Communication%20Skills%20in%20Classrooms.578f9910c41edc955f89.webp" alt="Modern English language lab" data-aos="zoom-in" data-aos-delay="500">
            </div>
        </div>
    </section>

    <section id="features">
        <h2 data-aos="fade-up">Why Choose Us?</h2>
        <div class="features-grid">
            <div class="feature" data-aos="fade-up" data-aos-delay="100">
                <i class="fas fa-chalkboard-teacher"></i>
                <h3>Expert Tutoring</h3>
                <p>Personalized guidance by Mr. Tusitha Jayawardhena and qualified teachers</p>
            </div>
            <div class="feature" data-aos="fade-up" data-aos-delay="200">
                <i class="fas fa-rupee-sign"></i>
                <h3>Affordable Fees</h3>
                <p>Monthly fees up to only Rs. 700 with special first-month discount</p>
            </div>
            <div class="feature" data-aos="fade-up" data-aos-delay="300">
                <i class="fas fa-video"></i>
                <h3>Online via Zoom</h3>
                <p>Flexible online classes available for remote learning</p>
            </div>
            <div class="feature" data-aos="fade-up" data-aos-delay="400">
                <i class="fas fa-users"></i>
                <h3>All Levels Covered</h3>
                <p>From Grade 1 to Higher Education, O/L & A/L exam preparation</p>
            </div>
        </div>
    </section>

    <section id="pricing">
        <h2 data-aos="fade-up">Our Classes & Monthly Fees</h2>
        <p style="text-align:center; max-width:800px; margin:0 auto 50px;" data-aos="fade-up">
            <strong>Special Offer:</strong> <span style="color:#ff4757; font-size:1.2rem;">20% Discount on First Month Fees!</span><br>
            Available for both Physical and Online (Zoom) classes
        </p>
        <div class="pricing-container">
            <div class="pricing-card" data-aos="zoom-in" data-aos-delay="100">
                <h3>Grades 1-5</h3>
                <div class="price">Rs. 500/month</div>
                <span class="discount-badge">First Month: Rs. 400</span>
                <ul style="list-style:none; margin:20px 0;">
                    <li>✓ Fun & interactive learning</li>
                    <li>✓ Basic grammar & speaking</li>
                    <li>✓ Small group classes</li>
                </ul>
                <a href="#" class="btn">Enroll Now</a>
            </div>

            <div class="pricing-card" data-aos="zoom-in" data-aos-delay="200">
                <h3>Grades 6-9</h3>
                <div class="price">Rs. 600/month</div>
                <span class="discount-badge">First Month: Rs. 480</span>
                <ul style="list-style:none; margin:20px 0;">
                    <li>✓ School syllabus coverage</li>
                    <li>✓ Writing & reading skills</li>
                    <li>✓ Exam preparation</li>
                </ul>
                <a href="#" class="btn">Enroll Now</a>
            </div>

            <div class="pricing-card special" data-aos="zoom-in" data-aos-delay="300">
                <h3>O/L & A/L Preparation</h3>
                <div class="price">Rs. 700/month</div>
                <span class="discount-badge">First Month: Rs. 560</span>
                <ul style="list-style:none; margin:20px 0;">
                    <li>✓ Intensive exam-focused classes</li>
                    <li>✓ Past papers & mock tests</li>
                    <li>✓ Individual attention</li>
                    <li>✓ Proven results</li>
                </ul>
                <a href="#" class="btn" style="background:#fff; color:#007BFF;">Enroll Now</a>
            </div>

            <div class="pricing-card" data-aos="zoom-in" data-aos-delay="400">
                <h3>Higher Education / Adults</h3>
                <div class="price">Rs. 700/month</div>
                <span class="discount-badge">First Month: Rs. 560</span>
                <ul style="list-style:none; margin:20px 0;">
                    <li>✓ Spoken English & fluency</li>
                    <li>✓ Professional communication</li>
                    <li>✓ Flexible timings</li>
                </ul>
                <a href="#" class="btn">Enroll Now</a>
            </div>
        </div>
    </section>

    <footer id="footer">
        <p><strong>Sayura English Academy</strong><br>No 19, Sadunpura, Dehiattakandiya</p>
        <div class="contact-info">
            <p><i class="fas fa-phone"></i> Contact: 075-5252241</p>
            <p><i class="fab fa-whatsapp"></i> WhatsApp: 072-5762091</p>
            <p><i class="fas fa-video"></i> Online Classes Available via Zoom</p>
        </div>
        <div class="social-icons" style="margin:30px 0;">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-whatsapp"></i></a>
            <a href="#"><i class="fas fa-phone"></i></a>
        </div>
        <p>&copy; 2025 Sayura English Academy. All rights reserved.</p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
    <script>
        AOS.init({
            duration: 1000,
            once: true
        });

        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
    </script>
</body>
</html>
