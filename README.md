<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Protección Digital UVM</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-dark: #0A3C6F;
            --primary-light: #4A90E2;
            --accent: #6BA8F5;
            --background: #E6ECF0;
            --white: #FFFFFF;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Inter', sans-serif; background: var(--background); color: var(--primary-dark); scroll-behavior: smooth; }
        header { 
            background: linear-gradient(rgba(10, 60, 111, 0.8), rgba(10, 60, 111, 0.8)), url('https://via.placeholder.com/1920x600'); 
            background-size: cover; background-position: center; color: var(--white); text-align: center; padding: 5rem 2rem; 
            position: relative;
        }
        .logo { position: absolute; left: 2rem; top: 2rem; width: 100px; }
        header h1 { font-size: 2.8rem; margin-bottom: 1.5rem; }
        header p { font-size: 1.3rem; max-width: 700px; margin: 0 auto; }
        nav { 
            background: var(--primary-dark); padding: 1.2rem; position: sticky; top: 0; z-index: 1000; 
            display: flex; justify-content: center; gap: 2.5rem; 
        }
        nav a { color: var(--white); text-decoration: none; font-weight: 600; font-size: 1.2rem; transition: color 0.3s; }
        nav a:hover { color: var(--accent); }
        section { display: none; padding: 4rem 2rem; max-width: 1200px; margin: 2rem auto; animation: fadeIn 0.5s; }
        section.active { display: block; }
        .hero-button { 
            display: inline-block; margin-top: 2rem; padding: 1rem 2.5rem; background: var(--accent); color: var(--white); 
            text-decoration: none; border-radius: 6px; font-weight: 600; transition: background 0.3s; 
        }
        .hero-button:hover { background: #5a97e0; }
        .post { 
            background: var(--white); margin-bottom: 2rem; padding: 2rem; border-radius: 10px; 
            box-shadow: 0 4px 12px rgba(0,0,0,0.1); transition: transform 0.3s; cursor: pointer; 
        }
        .post:hover { transform: translateY(-5px); }
        .post-content { display: none; margin-top: 1rem; padding: 1rem; background: #f5f7fa; border-radius: 6px; }
        .post-content.active { display: block; }
        .carousel { position: relative; overflow: hidden; }
        .carousel-container { display: flex; transition: transform 0.5s; }
        .carousel-item { flex: 0 0 100%; padding: 1rem; }
        .carousel-buttons { text-align: center; margin-top: 1.5rem; }
        .carousel-buttons button { 
            background: var(--primary-light); color: var(--white); border: none; padding: 0.6rem 1.2rem; 
            margin: 0 0.5rem; cursor: pointer; border-radius: 6px; 
        }
        footer { 
            background: var(--primary-dark); color: var(--white); text-align: center; padding: 3rem; 
        }
        footer a { color: var(--accent); text-decoration: none; }
        footer a:hover { color: var(--white); }
        .contact-info { 
            display: flex; align-items: center; gap: 1rem; margin-top: 2rem; justify-content: center; 
        }
        .contact-info img { width: 40px; }
        .ig-button { 
            position: fixed; bottom: 30px; right: 30px; background: var(--accent); color: var(--white); 
            padding: 1rem; border-radius: 50%; box-shadow: 0 4px 8px rgba(0,0,0,0.2); 
            text-decoration: none; font-size: 1.5rem; z-index: 1000; 
        }
        .ig-button:hover { background: #5a97e0; }
        .team-member { 
            display: flex; gap: 1.5rem; margin-bottom: 2rem; padding: 1.5rem; background: var(--white); 
            border-radius: 10px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); 
        }
        .team-member img { width: 120px; height: 120px; border-radius: 50%; object-fit: cover; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @media (max-width: 768px) { 
            header h1 { font-size: 2rem; } 
            nav { flex-wrap: wrap; gap: 1.5rem; } 
            section { padding: 3rem 1rem; margin: 1rem auto; } 
            .logo { width: 80px; left: 1rem; top: 1rem; }
            .team-member { flex-direction: column; align-items: center; text-align: center; }
        }
    </style>
</head>
<body>
    <header>
        <img src="https://287524.fs1.hubspotusercontent-na1.net/hubfs/287524/Logo-UVM_300x900_Mesa%20de%20trabajo%201.png" class="logo">
        <h1>Protección Digital UVM</h1>
        <p>Tu aliado para navegar seguro en la era de la inteligencia artificial. Aprende a proteger tus datos y descubre cómo la tecnología puede ser tu mejor defensa.</p>
        <a href="#contacto" class="hero-button" onclick="mostrarSeccion('contacto')">Contáctanos</a>
    </header>

    <nav>
        <a onclick="mostrarSeccion('inicio')">Inicio</a>
        <a onclick="mostrarSeccion('quienes')">Quiénes Somos</a>
        <a onclick="mostrarSeccion('objetivo')">Objetivo</a>
        <a onclick="mostrarSeccion('publicaciones')">Publicaciones</a>
        <a onclick="mostrarSeccion('contacto')">Contáctanos</a>
    </nav>

    <main>
        <section id="inicio" class="active">
            <h2>Bienvenidos a Protección Digital UVM</h2>
            <p>En un mundo donde la inteligencia artificial transforma nuestra forma de vivir, la seguridad digital es más importante que nunca. En Protección Digital UVM, nos dedicamos a empoderar a la comunidad universitaria y al público general con herramientas, conocimientos y prácticas para proteger datos personales y navegar de forma segura.</p>
            <p>La inteligencia artificial ofrece oportunidades increíbles, pero también plantea desafíos en la protección de datos. Desde algoritmos que analizan tu comportamiento en línea hasta aplicaciones que recopilan información personal, estar informado es la clave para mantener el control de tu privacidad. Nuestro proyecto, impulsado por estudiantes de la Universidad del Valle de México, busca cerrar la brecha entre la tecnología y la seguridad, ofreciendo recursos prácticos y accesibles.</p>
            <p>En la UVM, creemos que la educación es la base para un futuro digital seguro. A través de talleres, publicaciones y campañas, trabajamos para que estudiantes, profesores y la comunidad en general comprendan los riesgos del mundo digital y adopten prácticas responsables. Desde aprender a crear contraseñas seguras hasta entender cómo la IA usa tus datos, estamos aquí para guiarte.</p>
            <p>Únete a nosotros en esta misión para construir un entorno digital ético, seguro y accesible para todos. Explora nuestras publicaciones y descubre cómo puedes proteger tu privacidad hoy.</p>
            <a href="#publicaciones" class="hero-button" onclick="mostrarSeccion('publicaciones')">Ver Publicaciones</a>
        </section>

        <section id="quienes">
            <h2>¿Quiénes Somos?</h2>
            <p>Somos un equipo de estudiantes de la Universidad del Valle de México (UVM), comprometidos con la educación y la ética digital. Nuestra misión es promover el uso responsable de la inteligencia artificial y proteger la privacidad en línea. Conoce a los miembros de nuestro equipo, quienes combinan su pasión por la tecnología con un fuerte compromiso social.</p>
            <div class="team-member">
                <img src="https://via.placeholder.com/120" alt="Patricio Cortés">
                <div>
                    <h3>Patricio Cortés</h3>
                    <p>Estudiante de Ingeniería en Ciberseguridad en UVM. Apasionado por desarrollar soluciones para proteger datos en entornos digitales. Participa activamente en hackathons y talleres para promover la seguridad en línea entre estudiantes.</p>
                </div>
            </div>
            <div class="team-member">
                <img src="https://via.placeholder.com/120" alt="Diego Cabrera">
                <div>
                    <h3>Diego Cabrera</h3>
                    <p>Estudiante de Tecnologías de la Información en UVM. Enfocado en la educación sobre el uso seguro de la inteligencia artificial. Ha liderado campañas en redes sociales para concienciar sobre los riesgos digitales.</p>
                </div>
            </div>
            <div class="team-member">
                <img src="https://via.placeholder.com/120" alt="Gael Aguado">
                <div>
                    <h3>Gael Aguado</h3>
                    <p>Estudiante de Ingeniería en Sistemas en UVM. Interesado en la ética digital y la prevención de ciberataques. Colabora en la creación de guías prácticas para estudiantes sobre protección de datos.</p>
                </div>
            </div>
            <div class="team-member">
                <img src="https://via.placeholder.com/120" alt="Alejandro Núñez">
                <div>
                    <h3>Alejandro Núñez</h3>
                    <p>Estudiante de Ciberseguridad en UVM. Comprometido con enseñar buenas prácticas para proteger la privacidad en línea. Organiza charlas en la UVM para fomentar una cultura de seguridad digital.</p>
                </div>
            </div>
        </section>

        <section id="objetivo">
            <h2>Nuestros Objetivos</h2>
            <p>En Protección Digital UVM, trabajamos para transformar la forma en que la comunidad interactúa con la tecnología. Nuestros objetivos son:</p>
            <ul>
                <li>Educar sobre los riesgos de la exposición en línea y proporcionar herramientas para mitigarlos.</li>
                <li>Promover el uso seguro y ético de plataformas digitales impulsadas por inteligencia artificial.</li>
                <li>Fomentar una cultura de protección de datos en la comunidad universitaria y más allá.</li>
                <li>Desarrollar recursos prácticos, como guías y talleres, para proteger la privacidad en redes sociales, aplicaciones y servicios en línea.</li>
                <li>Colaborar con expertos y organizaciones para fortalecer la ciberseguridad en México.</li>
            </ul>
            <p>Nuestra visión es un futuro donde todos puedan aprovechar la tecnología sin comprometer su seguridad. Creemos que la educación y la conciencia son los primeros pasos para lograrlo, y en la UVM estamos comprometidos con liderar este cambio.</p>
        </section>

        <section id="publicaciones">
            <h2>Últimas Publicaciones</h2>
            <div class="carousel">
                <div class="carousel-container" id="carousel">
                    <!-- Publicaciones se cargan dinámicamente -->
                </div>
                <div class="carousel-buttons">
                    <button onclick="moveCarousel(-1)">←</button>
                    <button onclick="moveCarousel(1)">→</button>
                </div>
            </div>
        </section>

        <section id="contacto">
            <h2>Contáctanos</h2>
            <p>¿Tienes preguntas, sugerencias o quieres colaborar con nosotros? Estamos aquí para ayudarte. Contáctanos a través de nuestro correo institucional y únete a la conversación sobre seguridad digital.</p>
            <div class="contact-info">
                <img src="https://via.placeholder.com/40?text=📧" alt="Correo">
                <p>Correo institucional: <a href="mailto:contacto@protecciondigitaluvm.mx">contacto@protecciondigitaluvm.mx</a></p>
            </div>
            <p>Envíanos un mensaje con tus dudas o ideas, y nuestro equipo te responderá lo antes posible. ¡Tu privacidad y seguridad son nuestra prioridad!</p>
        </section>
    </main>

    <footer>
        <p>© 2025 Protección Digital UVM. Todos los derechos reservados.</p>
        <p>Síguenos en <a href="https://www.instagram.com/proteccion_digitaluvm/" target="_blank">Instagram</a> para más consejos de seguridad digital.</p>
        <p>Visita el sitio oficial de la <a href="https://uvm.mx/" target="_blank">Universidad del Valle de México</a> para conocer más sobre nuestra institución.</p>
    </footer>

    <a href="https://www.instagram.com/proteccion_digitaluvm/" target="_blank" class="ig-button">📸</a>

    <script>
        function mostrarSeccion(id) {
            document.querySelectorAll('section').forEach(sec => sec.classList.remove('active'));
            document.getElementById(id).classList.add('active');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        const publicaciones = [
            { 
                titulo: "¿Por qué proteger tus datos?", 
                resumen: "En la era de la IA, tus datos son un activo valioso. Aprende cómo el robo de identidad y las filtraciones pueden afectarte y qué medidas tomar para protegerte.", 
                contenido: "La protección de datos es crucial en un mundo donde la inteligencia artificial analiza constantemente información personal. El robo de identidad puede llevar a pérdidas financieras, daño a tu reputación y problemas legales. Para protegerte, usa contraseñas seguras, evita compartir información sensible en sitios no seguros y revisa regularmente tus cuentas en busca de actividad sospechosa. Además, aprende sobre las leyes de protección de datos, como el RGPD, que establecen estándares para el manejo de información personal."
            },
            { 
                titulo: "Peligros en redes sociales", 
                resumen: "Cada publicación en redes sociales puede ser una puerta a tu privacidad. Descubre cómo configurar tus cuentas para minimizar riesgos.", 
                contenido: "Las redes sociales son una herramienta poderosa, pero también un campo minado para tu privacidad. Publicar información personal, como tu ubicación o datos de contacto, puede ser aprovechado por ciberdelincuentes. Configura tus cuentas para que solo tus contactos cercanos vean tus publicaciones, desactiva el etiquetado automático y revisa las políticas de privacidad de las plataformas. Además, evita hacer clic en enlaces sospechosos compartidos en redes, ya que podrían ser intentos de phishing."
            },
            { 
                titulo: "IA y tus datos personales", 
                resumen: "Las IAs procesan grandes cantidades de datos. Conoce cómo limitar la información que compartes con aplicaciones impulsadas por IA.", 
                contenido: "La inteligencia artificial impulsa muchas aplicaciones modernas, desde asistentes virtuales hasta redes sociales. Sin embargo, estas tecnologías recopilan datos para personalizar experiencias, lo que puede comprometer tu privacidad. Para protegerte, revisa los permisos de las aplicaciones, desactiva el acceso a datos innecesarios (como tu ubicación o contactos) y usa configuraciones de privacidad estrictas. También considera usar servicios que prioricen la privacidad, como navegadores enfocados en la seguridad."
            },
            { 
                titulo: "Consejos de seguridad digital", 
                resumen: "Usa contraseñas seguras, habilita la autenticación en dos pasos y revisa los permisos de las aplicaciones que instalas.", 
                contenido: "La seguridad digital comienza con hábitos simples pero efectivos. Crea contraseñas únicas y complejas para cada cuenta, usando una combinación de letras, números y símbolos. Habilita la autenticación en dos pasos (2FA) para añadir una capa adicional de protección. Revisa regularmente los permisos de las aplicaciones en tu teléfono o computadora, y elimina el acceso a aquellas que no necesites. Por último, mantén tu software actualizado para protegerte contra vulnerabilidades conocidas."
            },
            { 
                titulo: "Phishing: Cómo detectarlo", 
                resumen: "El phishing es una técnica común para robar datos. Aprende a identificar correos y mensajes sospechosos.", 
                contenido: "El phishing es un tipo de ciberataque donde los delincuentes se hacen pasar por entidades confiables para robar tus datos. Los correos o mensajes de phishing suelen incluir enlaces maliciosos o solicitudes de información personal. Para detectarlos, verifica la dirección del remitente, busca errores gramaticales o de formato, y nunca hagas clic en enlaces sospechosos. Usa software antivirus y aprende a reconocer las señales de alerta, como ofertas demasiado buenas para ser verdad."
            },
            { 
                titulo: "El impacto de la IA en la privacidad", 
                resumen: "Explora cómo la inteligencia artificial puede tanto proteger como amenazar tu privacidad en línea.", 
                contenido: "La inteligencia artificial tiene un doble papel en la privacidad. Por un lado, puede mejorar la seguridad mediante la detección de fraudes o la autenticación biométrica. Por otro, su capacidad para analizar grandes volúmenes de datos plantea riesgos si no se regula adecuadamente. Para proteger tu privacidad, infórmate sobre cómo las empresas usan la IA, limita la cantidad de datos que compartes y apoya iniciativas que promuevan regulaciones éticas en el uso de la inteligencia artificial."
            }
        ];

        let currentIndex = 0;

        function cargarPublicaciones() {
            const carousel = document.getElementById('carousel');
            publicaciones.forEach((pub, index) => {
                const item = document.createElement('div');
                item.className = 'carousel-item';
                item.innerHTML = `
                    <div class="post" onclick="toggleContent(${index})">
                        <h3>${pub.titulo}</h3>
                        <p>${pub.resumen}</p>
                        <div class="post-content" id="content-${index}">
                            <p>${pub.contenido}</p>
                        </div>
                    </div>`;
                carousel.appendChild(item);
            });
            updateCarousel();
        }

        function toggleContent(index) {
            const content = document.getElementById(`content-${index}`);
            content.classList.toggle('active');
        }

        function moveCarousel(direction) {
            currentIndex = (currentIndex + direction + publicaciones.length) % publicaciones.length;
            updateCarousel();
        }

        function updateCarousel() {
            const carousel = document.getElementById('carousel');
            carousel.style.transform = `translateX(-${currentIndex * 100}%)`;
        }

        window.onload = cargarPublicaciones;
    </script>
</body>
</html>
