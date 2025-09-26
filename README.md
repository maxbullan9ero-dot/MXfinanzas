# MXfinanzas
MI PROYECTO
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MX Asesorías - Transforma tu Futuro Financiero</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            color: white;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(0, 0, 0, 0.9);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            height: 60px;
            width: auto;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #4CAF50;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            flex: 1;
            z-index: 2;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #2196F3, #4CAF50);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 20px rgba(33, 150, 243, 0.5)); }
            to { filter: drop-shadow(0 0 30px rgba(76, 175, 80, 0.7)); }
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            background: linear-gradient(45deg, #2196F3, #4CAF50);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1.1rem;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(33, 150, 243, 0.4);
        }

        /* Animated Background */
        .floating-numbers {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .number {
            position: absolute;
            font-size: 2rem;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
            color: #4CAF50;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        /* Stats Section */
        .stats {
            padding: 5rem 0;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            text-align: center;
        }

        .stat-item {
            padding: 2rem;
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.1), rgba(76, 175, 80, 0.1));
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            color: #4CAF50;
            margin-bottom: 0.5rem;
        }

        /* Services Section */
        .services {
            padding: 5rem 0;
        }

        .services h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #4CAF50;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.1), rgba(76, 175, 80, 0.1));
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(33, 150, 243, 0.2);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: #4CAF50;
        }

        /* Laws Section */
        .laws {
            padding: 5rem 0;
            background: rgba(0, 0, 0, 0.3);
        }

        .laws h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #2196F3;
        }

        .law-item {
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.1), rgba(76, 175, 80, 0.1));
            margin: 1rem 0;
            padding: 1.5rem;
            border-radius: 15px;
            border-left: 4px solid #4CAF50;
            transition: transform 0.3s;
        }

        .law-item:hover {
            transform: translateX(10px);
        }

        .law-number {
            font-size: 1.5rem;
            font-weight: bold;
            color: #4CAF50;
            margin-bottom: 0.5rem;
        }

        /* Contact Section */
        .contact {
            padding: 5rem 0;
            text-align: center;
        }

        .contact h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #4CAF50;
        }

        /* Footer */
        footer {
            background: rgba(0, 0, 0, 0.8);
            padding: 2rem 0;
            text-align: center;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .nav-links {
                display: none;
            }
        }

        /* Particle Effect */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: #4CAF50;
            border-radius: 50%;
            animation: particle-float 8s linear infinite;
        }

        @keyframes particle-float {
            0% {
                transform: translateY(100vh) translateX(0);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) translateX(100px);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <!-- Particles Background -->
    <div class="particles" id="particles"></div>

    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxjaXJjbGUgY3g9IjUwIiBjeT0iNTAiIHI9IjQ4IiBzdHJva2U9IiMwMDAiIHN0cm9rZS13aWR0aD0iNCIgZmlsbD0iI2ZmZiIvPgo8dGV4dCB4PSI1MCIgeT0iNDAiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIyNCIgZm9udC13ZWlnaHQ9ImJvbGQiIGZpbGw9IiMyMTk2RjMiIHRleHQtYW5jaG9yPSJtaWRkbGUiPk1YPC90ZXh0Pgo8dGV4dCB4PSI1MCIgeT0iNjUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMiIgZmlsbD0iIzY2NiIgdGV4dC1hbmNob3I9Im1pZGRsZSI+YXNlc29yw61hczwvdGV4dD4KPHN2ZyB4PSI3MCIgeT0iMjUiIHdpZHRoPSIxNSIgaGVpZ2h0PSIxNSI+CjxwYXRoIGQ9Ik0xIDEwSDEwTDUuNSA0WiIgZmlsbD0iIzRDQUY1MCIvPgo8L3N2Zz4KPHN2ZyB4PSI3NSIgeT0iMzUiIHdpZHRoPSIxMCIgaGVpZ2h0PSIxMCI+CjxwYXRoIGQ9Ik0yIDhIMEw1IDJaIiBmaWxsPSIjMjE5NkYzIi8+CjwvdGV4dD4KPC9zdmc+" alt="MX Asesorías" class="logo">
                <ul class="nav-links">
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#servicios">Servicios</a></li>
                    <li><a href="#leyes">Leyes de Finanzas</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="container">
            <div class="hero-content">
                <h1>Transforma tu Futuro Financiero</h1>
                <p>Formaliza tu negocio, entiende el mundo financiero y alcanza el crecimiento que mereces. Con MX Asesorías, tu éxito es nuestro compromiso.</p>
                <a href="#contacto" class="cta-button">Comienza tu Transformación</a>
            </div>
        </div>
        
        <!-- Animated Numbers Background -->
        <div class="floating-numbers">
            <div class="number" style="top: 20%; left: 10%; animation-delay: 0s;">$</div>
            <div class="number" style="top: 60%; left: 15%; animation-delay: 1s;">%</div>
            <div class="number" style="top: 30%; left: 80%; animation-delay: 2s;">₹</div>
            <div class="number" style="top: 70%; left: 85%; animation-delay: 3s;">€</div>
            <div class="number" style="top: 40%; left: 90%; animation-delay: 4s;">£</div>
            <div class="number" style="top: 15%; left: 70%; animation-delay: 5s;">¥</div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-item">
                    <div class="stat-number" id="clients">0</div>
                    <p>Clientes Transformados</p>
                </div>
                <div class="stat-item">
                    <div class="stat-number" id="growth">0%</div>
                    <p>Crecimiento Promedio</p>
                </div>
                <div class="stat-item">
                    <div class="stat-number" id="years">0</div>
                    <p>Años de Experiencia</p>
                </div>
                <div class="stat-item">
                    <div class="stat-number" id="success">0%</div>
                    <p>Tasa de Éxito</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="servicios">
        <div class="container">
            <h2>Nuestros Servicios</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">⚖️</div>
                    <h3>Formalización Legal</h3>
                    <p>Te ayudamos a obtener tu RUT Empresarial, registrarte en el SII y cumplir con todas las obligaciones legales para operar tu negocio de forma correcta.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">📊</div>
                    <h3>Planificación Estratégica</h3>
                    <p>Desarrollamos planes de crecimiento personalizados para tu empresa.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">💰</div>
                    <h3>Finanzas Personales</h3>
                    <p>Educación financiera desde cero. Aprende a manejar tus finanzas personales y empresariales para maximizar tu crecimiento.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🚀</div>
                    <h3>Crecimiento Empresarial</h3>
                    <p>Estrategias probadas para hacer crecer tu negocio, aumentar tus ingresos y alcanzar tus metas financieras.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Laws of Finance Section -->
    <section class="laws" id="leyes">
        <div class="container">
            <h2>Las 7 Leyes Fundamentales de las Finanzas</h2>
            <p style="text-align: center; margin-bottom: 3rem; font-size: 1.1rem;">Principios que te guiarán hacia el éxito financiero</p>
            
            <div class="law-item">
                <div class="law-number">Ley #1</div>
                <h3>Ley del Presupuesto</h3>
                <p>Controla tus gastos y vive por debajo de tus posibilidades. Un presupuesto bien planificado es la base de toda estabilidad financiera.</p>
            </div>

            <div class="law-item">
                <div class="law-number">Ley #2</div>
                <h3>Ley del Ahorro</h3>
                <p>Paga primero a ti mismo. Ahorra al menos el 10% de tus ingresos antes de cualquier gasto. Tu futuro yo te lo agradecerá.</p>
            </div>

            <div class="law-item">
                <div class="law-number">Ley #3</div>
                <h3>Ley de la Inversión</h3>
                <p>Haz que tu dinero trabaje para ti. Invierte de manera inteligente y diversificada para crear riqueza a largo plazo.</p>
            </div>

            <div class="law-item">
                <div class="law-number">Ley #4</div>
                <h3>Ley de la Educación Financiera</h3>
                <p>Nunca dejes de aprender. La educación financiera continua es la clave para tomar mejores decisiones con tu dinero.</p>
            </div>

            <div class="law-item">
                <div class="law-number">Ley #5</div>
                <h3>Ley de la Diversificación</h3>
                <p>No pongas todos los huevos en una canasta. Diversifica tus ingresos y inversiones para reducir riesgos.</p>
            </div>

            <div class="law-item">
                <div class="law-number">Ley #6</div>
                <h3>Ley del Tiempo</h3>
                <p>El tiempo es tu mayor aliado financiero. Comienza temprano y aprovecha el poder del interés compuesto.</p>
            </div>

            <div class="law-item">
                <div class="law-number">Ley #7</div>
                <h3>Ley de la Disciplina</h3>
                <p>La consistencia vence a la perfección. Mantén disciplina en tus hábitos financieros para obtener resultados extraordinarios.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contacto">
        <div class="container">
            <h2>¿Listo para Transformar tu Futuro?</h2>
            <p style="margin-bottom: 2rem; font-size: 1.2rem;">Agenda tu consultoría gratuita y descubre cómo podemos ayudarte a alcanzar tus metas financieras.</p>
            <a href="mailto:contacto@mxasesorias.com" class="cta-button">Contáctanos Ahora</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2025 MX Asesorías. Todos los derechos reservados. Transformando futuros financieros.</p>
        </div>
    </footer>

    <script>
        // Animated counters
        function animateCounters() {
            const counters = [
                { id: 'clients', target: 500, suffix: '+' },
                { id: 'growth', target: 85, suffix: '%' },
                { id: 'years', target: 5, suffix: '+' },
                { id: 'success', target: 95, suffix: '%' }
            ];

            counters.forEach(counter => {
                const element = document.getElementById(counter.id);
                let current = 0;
                const increment = counter.target / 100;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= counter.target) {
                        element.textContent = counter.target + counter.suffix;
                        clearInterval(timer);
                    } else {
                        element.textContent = Math.floor(current) + counter.suffix;
                    }
                }, 20);
            });
        }

        // Create particle effect
        function createParticles() {
            const particleContainer = document.getElementById('particles');
            for (let i = 0; i < 50; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + 'vw';
                particle.style.animationDelay = Math.random() * 8 + 's';
                particle.style.animationDuration = (Math.random() * 3 + 5) + 's';
                particleContainer.appendChild(particle);
            }
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Initialize everything when page loads
        window.addEventListener('load', function() {
            createParticles();
            
            // Trigger counter animation when stats section is visible
            const statsSection = document.querySelector('.stats');
            const observer = new IntersectionObserver((entries) => {
                if (entries[0].isIntersecting) {
                    animateCounters();
                    observer.unobserve(statsSection);
                }
            });
            observer.observe(statsSection);
        });

        // Add floating animation to service cards
        document.querySelectorAll('.service-card').forEach((card, index) => {
            card.style.animationDelay = index * 0.2 + 's';
        });
    </script>
</body>
</html>
