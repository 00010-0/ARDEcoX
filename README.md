<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARDECO | Inmobiliaria - Tu hogar ideal</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --rojo-principal: #c62828;
            --rojo-oscuro: #8e0000;
            --rojo-claro: #ff5f52;
            --gris-oscuro: #333333;
            --gris-medio: #666666;
            --gris-claro: #f5f5f5;
            --blanco: #ffffff;
            --sombra: 0 4px 12px rgba(0, 0, 0, 0.1);
            --sombra-intensa: 0 8px 24px rgba(198, 40, 40, 0.2);
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            color: var(--gris-oscuro);
            line-height: 1.6;
            font-family: 'Open Sans', sans-serif;
        }  
        h1, h2, h3, h4 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
        }       
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }      
        h1 {
            font-size: 2.8rem;
            line-height: 1.2;
            margin-bottom: 1rem;
        }   
        h2 {
            font-size: 2.2rem;
            text-align: center;
            margin-bottom: 2.5rem;
            position: relative;
        }        
        h2:after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background-color: var(--rojo-principal);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }        
        p {
            margin-bottom: 1.2rem;
            font-size: 1.05rem;
        }
        .btn {
            display: inline-block;
            background-color: var(--rojo-principal);
            color: var(--blanco);
            padding: 14px 32px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-family: 'Montserrat', sans-serif;
            font-size: 1rem;
            letter-spacing: 0.5px;
        }
        .btn:hover {
            background-color: var(--rojo-oscuro);
            transform: translateY(-3px);
            box-shadow: var(--sombra-intensa);
        }
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--rojo-principal);
            color: var(--rojo-principal);
        }
        .btn-outline:hover {
            background-color: var(--rojo-principal);
            color: var(--blanco);
        }
        /* Header y Navegación */
        header {
            background-color: var(--blanco);
            box-shadow: var(--sombra);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }
        .logo h1 {
            color: var(--rojo-principal);
            font-size: 2.2rem;
            margin-bottom: 0;
            letter-spacing: 1px;
        }
        .logo span {
            color: var(--gris-oscuro);
            font-weight: 300;
        }
        .logo i {
            color: var(--rojo-principal);
            font-size: 2.2rem;
            margin-right: 12px;
        }
        nav ul {
            display: flex;
            list-style: none;
        }
        nav li {
            margin-left: 30px;
        }
        nav a {
            text-decoration: none;
            color: var(--gris-oscuro);
            font-weight: 600;
            font-size: 1.05rem;
            transition: color 0.3s;
            font-family: 'Montserrat', sans-serif;
        }
        nav a:hover {
            color: var(--rojo-principal);
        }
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.8rem;
            color: var(--rojo-principal);
            cursor: pointer;
        }
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1560518883-ce09059eeffa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1473&q=80');
            background-size: cover;
            background-position: center;
            color: var(--blanco);
            text-align: center;
            padding: 140px 0;
        }
        .hero h1 {
            color: var(--blanco);
            margin-bottom: 20px;
            font-size: 3.5rem;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }
        .hero p {
            font-size: 1.4rem;
            max-width: 700px;
            margin: 0 auto 40px;
            font-weight: 300;
        }
        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        /* Propiedades Destacadas */
        .propiedades {
            padding: 90px 0;
            background-color: var(--gris-claro);
        }
        .section-subtitle {
            text-align: center;
            color: var(--gris-medio);
            max-width: 700px;
            margin: 0 auto 50px;
            font-size: 1.1rem;
        }
        .propiedades-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 35px;
            margin-top: 20px;
        }
        .propiedad-card {
            background-color: var(--blanco);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--sombra);
            transition: transform 0.3s ease;
        }
        .propiedad-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--sombra-intensa);
        }
        .propiedad-img {
            height: 240px;
            overflow: hidden;
            position: relative;
        }
        .propiedad-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        .propiedad-card:hover .propiedad-img img {
            transform: scale(1.08);
        }
        .propiedad-tipo {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--rojo-principal);
            color: var(--blanco);
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
        }
        .propiedad-info {
            padding: 25px;
        }
        .propiedad-info h3 {
            margin-bottom: 10px;
            font-size: 1.5rem;
        }
        .propiedad-ubicacion {
            color: var(--gris-medio);
            font-size: 0.95rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        .propiedad-ubicacion i {
            margin-right: 8px;
            color: var(--rojo-principal);
        }
        .propiedad-precio {
            color: var(--rojo-principal);
            font-size: 1.7rem;
            font-weight: 700;
            margin-bottom: 20px;
        }
        .propiedad-desc {
            color: var(--gris-medio);
            margin-bottom: 25px;
            font-size: 0.95rem;
            line-height: 1.7;
        }
        .propiedad-caract {
            display: flex;
            justify-content: space-between;
            margin-bottom: 25px;
            font-size: 0.9rem;
            border-top: 1px solid #eee;
            padding-top: 20px;
        }
        .propiedad-caract span {
            display: flex;
            align-items: center;
        }
        .propiedad-caract i {
            color: var(--rojo-principal);
            margin-right: 8px;
            font-size: 1.1rem;
        }
        /* Servicios */
        .servicios {
            padding: 90px 0;
        }
        .servicios-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 35px;
            margin-top: 40px;
        }
        .servicio-card {
            text-align: center;
            padding: 40px 25px;
            border-radius: 10px;
            background-color: var(--blanco);
            box-shadow: var(--sombra);
            transition: all 0.3s ease;
        }
        .servicio-card:hover {
            background-color: var(--rojo-principal);
            color: var(--blanco);
            transform: translateY(-8px);
            box-shadow: var(--sombra-intensa);
        }
        .servicio-card:hover h3,
        .servicio-card:hover p,
        .servicio-card:hover .servicio-icon {
            color: var(--blanco);
        }
        .servicio-icon {
            font-size: 3.2rem;
            color: var(--rojo-principal);
            margin-bottom: 25px;
            transition: color 0.3s ease;
        }
        .servicio-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            transition: color 0.3s ease;
        }
        .servicio-card p {
            color: var(--gris-medio);
            transition: color 0.3s ease;
        }
        /* Sobre Nosotros */
        .sobre-nosotros {
            padding: 90px 0;
            background-color: var(--gris-claro);
        }
        .sobre-contenido {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }
        .sobre-texto h2 {
            text-align: left;
        }
        .sobre-texto h2:after {
            left: 0;
            transform: none;
        }
        .sobre-texto p {
            margin-bottom: 25px;
        }
        .sobre-estadisticas {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-top: 40px;
        }
        .estadistica {
            text-align: center;
            padding: 20px;
            background-color: var(--blanco);
            border-radius: 8px;
            box-shadow: var(--sombra);
        }
        .estadistica-numero {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--rojo-principal);
            margin-bottom: 5px;
        }
        .estadistica-texto {
            font-size: 0.95rem;
            color: var(--gris-medio);
        }
        .sobre-imagen img {
            width: 100%;
            border-radius: 10px;
            box-shadow: var(--sombra);
        }
        /* Contacto */
        .contacto {
            padding: 90px 0;
        }
        .contacto-contenido {
            display: grid;
            grid-template-columns: 1fr 1.5fr;
            gap: 60px;
        }
        .contacto-info h2 {
            text-align: left;
        }
        .contacto-info h2:after {
            left: 0;
            transform: none;
        }
        .contacto-datos {
            margin-top: 30px;
        }
        .contacto-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 25px;
        }
        .contacto-icon {
            background-color: var(--rojo-principal);
            color: var(--blanco);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-size: 1.2rem;
            flex-shrink: 0;
        }
        .contacto-texto h4 {
            margin-bottom: 5px;
            font-size: 1.2rem;
        }
        .contacto-form {
            background-color: var(--gris-claro);
            padding: 40px;
            border-radius: 10px;
            box-shadow: var(--sombra);
        }
        .form-group {
            margin-bottom: 25px;
        }
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--gris-oscuro);
        }
        .form-control {
            width: 100%;
            padding: 14px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
            font-family: 'Open Sans', sans-serif;
            transition: border-color 0.3s;
        }
        .form-control:focus {
            outline: none;
            border-color: var(--rojo-principal);
        }
        /* Footer */
        footer {
            background-color: var(--gris-oscuro);
            color: var(--blanco);
            padding: 60px 0 30px;
        }
        .footer-contenido {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 40px;
            margin-bottom: 50px;
        }
        .footer-logo h2 {
            color: var(--blanco);
            text-align: left;
            margin-bottom: 20px;
        }
        .footer-logo h2:after {
            display: none;
        }
        .footer-logo p {
            color: #ccc;
        }
        .footer-titulo {
            font-size: 1.3rem;
            margin-bottom: 25px;
            color: var(--blanco);
        }
        .footer-links ul {
            list-style: none;
        }
        .footer-links li {
            margin-bottom: 12px;
        }
        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        .footer-links a:hover {
            color: var(--rojo-claro);
        }
        .footer-redes {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        .footer-redes a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: #444;
            color: var(--blanco);
            border-radius: 50%;
            text-decoration: none;
            transition: all 0.3s;
        }
        .footer-redes a:hover {
            background-color: var(--rojo-principal);
            transform: translateY(-3px);
        }
        .footer-copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #444;
            color: #aaa;
            font-size: 0.9rem;
        }
        /* Responsive */
        @media (max-width: 992px) {
            .sobre-contenido, .contacto-contenido {
                grid-template-columns: 1fr;
                gap: 40px;
            }
            .sobre-texto h2, .contacto-info h2 {
                text-align: center;
            }
            .sobre-texto h2:after, .contacto-info h2:after {
                left: 50%;
                transform: translateX(-50%);
            }
            .footer-contenido {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            h2 {
                font-size: 1.8rem;
            }
            .hero {
                padding: 100px 0;
            }
            .hero h1 {
                font-size: 2.5rem;
            }
            .hero p {
                font-size: 1.2rem;
            }
            nav ul {
                display: none;
            }
            .mobile-menu-btn {
                display: block;
            }
            .propiedades-grid, .servicios-grid {
                grid-template-columns: 1fr;
            }
            .sobre-estadisticas {
                grid-template-columns: 1fr;
            }
        }
        @media (max-width: 576px) {
            .footer-contenido {
                grid-template-columns: 1fr;
            }
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            .btn {
                width: 100%;
                max-width: 280px;
                text-align: center;
            }
        }
        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .fade-in {
            animation: fadeIn 0.8s ease forwards;
        }
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">
                <i class="fas fa-building"></i>
                <h1>ARDECO <span>| Inmobiliaria</span></h1>
            </a>
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
            <nav>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#propiedades">Propiedades</a></li>
                    <li><a href="#servicios">Servicios</a></li>
                    <li><a href="#nosotros">Nosotros</a></li>
                    <li><a href="#contacto" class="btn">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>
    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="container">
            <h1 class="fade-in">ENCUENTRA TU HOGAR IDEAL CON ARDECO</h1>
            <p class="fade-in delay-1">Más de 15 años ayudando a familias y empresas a encontrar la propiedad perfecta. Tu satisfacción es nuestra prioridad.</p>
            <div class="hero-btns fade-in delay-2">
                <a href="#propiedades" class="btn">Ver Propiedades</a>
                <a href="#contacto" class="btn btn-outline">Contactar Ahora</a>
            </div>
        </div>
    </section>
    <!-- Propiedades Destacadas -->
    <section class="propiedades" id="propiedades">
        <div class="container">
            <h2>Propiedades Destacadas</h2>
            <p class="section-subtitle">Explora nuestra selección de las mejores propiedades disponibles en el mercado. Desde modernos apartamentos hasta lujosas villas, tenemos lo que buscas.</p>
            <div class="propiedades-grid">
                <!-- Propiedad 1 -->
                <div class="propiedad-card fade-in">
                    <div class="propiedad-img">
                        <img src="https://images.unsplash.com/photo-1613490493576-7fde63acd811?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80" alt="Apartamento moderno en centro">
                        <div class="propiedad-tipo">VENTA</div>
                    </div>
                    <div class="propiedad-info">
                        <h3>Apartamento Moderno en Centro</h3>
                        <div class="propiedad-ubicacion">
                            <i class="fas fa-map-marker-alt"></i> Zona Centro, Madrid
                        </div>
                        <div class="propiedad-precio">€ 425,000</div>
                        <p class="propiedad-desc">Luminoso apartamento de 3 habitaciones con acabados de lujo y vistas panorámicas al centro histórico.</p>
                        <div class="propiedad-caract">
                            <span><i class="fas fa-bed"></i> 3 Habitaciones</span>
                            <span><i class="fas fa-bath"></i> 2 Baños</span>
                            <span><i class="fas fa-ruler-combined"></i> 120 m²</span>
                        </div>
                        <a href="#contacto" class="btn" style="width: 100%; text-align: center;">Solicitar Información</a>
                    </div>
                </div>
                <!-- Propiedad 2 -->
                <div class="propiedad-card fade-in delay-1">
                    <div class="propiedad-img">
                        <img src="https://images.unsplash.com/photo-1518780664697-55e3ad937233?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Chalet con jardín">
                        <div class="propiedad-tipo">ALQUILER</div>
                    </div>
                    <div class="propiedad-info">
                        <h3>Chalet con Jardín Amplio</h3>
                        <div class="propiedad-ubicacion">
                            <i class="fas fa-map-marker-alt"></i> Zona Norte, Barcelona
                        </div>
                        <div class="propiedad-precio">€ 2,200/mes</div>
                        <p class="propiedad-desc">Exclusivo chalet independiente con amplio jardín, piscina y garaje para 2 coches. Ideal para familias.</p>
                        <div class="propiedad-caract">
                            <span><i class="fas fa-bed"></i> 4 Habitaciones</span>
                            <span><i class="fas fa-bath"></i> 3 Baños</span>
                            <span><i class="fas fa-ruler-combined"></i> 280 m²</span>
                        </div>
                        <a href="#contacto" class="btn" style="width: 100%; text-align: center;">Solicitar Información</a>
                    </div>
                </div>
                <!-- Propiedad 3 -->
                <div class="propiedad-card fade-in delay-2">
                    <div class="propiedad-img">
                        <img src="https://images.unsplash.com/photo-1545324418-cc1a3fa10c00?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" alt="Ático con terraza">
                        <div class="propiedad-tipo">VENTA</div>
                    </div>
                    <div class="propiedad-info">
                        <h3>Ático con Terraza Panorámica</h3>
                        <div class="propiedad-ubicacion">
                            <i class="fas fa-map-marker-alt"></i> Zona Este, Valencia
                        </div>
                        <div class="propiedad-precio">€ 650,000</div>
                        <p class="propiedad-desc">Espectacular ático completamente reformado con terraza de 60m² y vistas al mar. Incluye plaza de garaje.</p>
                        <div class="propiedad-caract">
                            <span><i class="fas fa-bed"></i> 3 Habitaciones</span>
                            <span><i class="fas fa-bath"></i> 2 Baños</span>
                            <span><i class="fas fa-ruler-combined"></i> 150 m²</span>
                        </div>
                        <a href="#contacto" class="btn" style="width: 100%; text-align: center;">Solicitar Información</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Servicios -->
    <section class="servicios" id="servicios">
        <div class="container">
            <h2>Nuestros Servicios</h2>
            <p class="section-subtitle">En ARDECO ofrecemos una amplia gama de servicios inmobiliarios para satisfacer todas tus necesidades, ya sea que busques comprar, vender o alquilar.</p>
            <div class="servicios-grid">
                <div class="servicio-card fade-in">
                    <div class="servicio-icon">
                        <i class="fas fa-home"></i>
                    </div>
                    <h3>Compra y Venta</h3>
                    <p>Te ayudamos a encontrar la propiedad perfecta para comprar o a vender tu inmueble al mejor precio del mercado.</p>
                </div>
                <div class="servicio-card fade-in delay-1">
                    <div class="servicio-icon">
                        <i class="fas fa-key"></i>
                    </div>
                    <h3>Alquileres</h3>
                    <p>Gestión completa de alquileres residenciales y comerciales. Encontramos el inquilino ideal para tu propiedad.</p>
                </div>
                <div class="servicio-card fade-in delay-2">
                    <div class="servicio-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Valoraciones</h3>
                    <p>Análisis exhaustivo del mercado para ofrecerte la valoración más precisa de tu propiedad.</p>
                </div>
                <div class="servicio-card fade-in delay-1">
                    <div class="servicio-icon">
                        <i class="fas fa-handshake"></i>
                    </div>
                    <h3>Asesoría Legal</h3>
                    <p>Te acompañamos en todos los trámites legales y administrativos con nuestro equipo de expertos.</p>
                </div>
                <div class="servicio-card fade-in delay-2">
                    <div class="servicio-icon">
                        <i class="fas fa-search-dollar"></i>
                    </div>
                    <h3>Estudios de Mercado</h3>
                    <p>Análisis detallado de las tendencias del mercado para ayudarte a tomar las mejores decisiones.</p>
                </div>
                <div class="servicio-card fade-in delay-3">
                    <div class="servicio-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Gestión de Comunidades</h3>
                    <p>Administración profesional de comunidades de propietarios para garantizar su correcto funcionamiento.</p>
                </div>
            </div>
        </div>
    </section>
    <!-- Sobre Nosotros -->
    <section class="sobre-nosotros" id="nosotros">
        <div class="container">
            <div class="sobre-contenido">
                <div class="sobre-texto fade-in">
                    <h2>Sobre ARDECO</h2>
                    <p>Con más de 15 años de experiencia en el sector inmobiliario, en ARDECO nos especializamos en ofrecer un servicio personalizado y de calidad a cada uno de nuestros clientes.</p>
                    <p>Nuestro equipo de profesionales está comprometido con ayudarte a encontrar la propiedad que se adapte a tus necesidades, ya sea para vivir, invertir o desarrollar tu negocio.</p>
                    <p>La transparencia, honestidad y dedicación son los pilares fundamentales de nuestra filosofía de trabajo. Tu satisfacción es nuestro mayor éxito.</p>
                    <div class="sobre-estadisticas">
                        <div class="estadistica">
                            <div class="estadistica-numero">15+</div>
                            <div class="estadistica-texto">Años de Experiencia</div>
                        </div>
                        <div class="estadistica">
                            <div class="estadistica-numero">1,200+</div>
                            <div class="estadistica-texto">Propiedades Vendidas</div>
                        </div>
                        <div class="estadistica">
                            <div class="estadistica-numero">98%</div>
                            <div class="estadistica-texto">Clientes Satisfechos</div>
                        </div>
                    </div>
                </div>
                <div class="sobre-imagen fade-in delay-1">
                    <img src="https://images.unsplash.com/photo-1560520031-3a4dc4e9de0c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1467&q=80" alt="Equipo ARDECO">
                </div>
            </div>
        </div>
    </section>

    <!-- Contacto -->
     <!-- Busca esta sección en tu código (línea ~394) -->
<div class="contacto-form fade-in delay-1">
    <form id="form-contacto" action="https://formsubmit.co/tu-correo@gmail.com" method="POST">
        <!-- Campos ocultos para FormSubmit -->
        <input type="hidden" name="_subject" value="📧 Nuevo mensaje de ARDECO Inmobiliaria">
        <input type="hidden" name="_template" value="table">
        <input type="hidden" name="_next" value="https://tu-dominio.com/gracias.html">
        <input type="hidden" name="_captcha" value="false">
        <input type="text" name="_honey" style="display:none">
        <div class="form-group">
            <label for="nombre">Nombre Completo *</label>
            <input type="text" id="nombre" name="nombre" class="form-control" required>
        </div>
        <div class="form-group">
            <label for="email">Correo Electrónico *</label>
            <input type="email" id="email" name="email" class="form-control" required>
        </div>
        <div class="form-group">
            <label for="telefono">Teléfono *</label>
            <input type="tel" id="telefono" name="telefono" class="form-control" required>
        </div>
        <div class="form-group">
            <label for="mensaje">Mensaje *</label>
            <textarea id="mensaje" name="mensaje" class="form-control" rows="5" placeholder="¿En qué podemos ayudarte?" required></textarea>
        </div>
        <button type="submit" class="btn" style="width: 100%;">Enviar Mensaje</button>
    </form>
</div>
    <section class="contacto" id="contacto">
        <div class="container">
            <div class="contacto-contenido">
                <div class="contacto-info fade-in">
                    <h2>Contacta con Nosotros</h2>
                    <p>¿Tienes preguntas sobre alguna propiedad o necesitas asesoramiento personalizado? No dudes en contactarnos. Nuestro equipo estará encantado de ayudarte.</p>
                    <div class="contacto-datos">
                        <div class="contacto-item">
                            <div class="contacto-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div class="contacto-texto">
                                <h4>Dirección</h4>
                                <p>Calle Gran Vía, 28, 28013 Madrid</p>
                            </div>
                        </div>
                        <div class="contacto-item">
                            <div class="contacto-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div class="contacto-texto">
                                <h4>Teléfono</h4>
                                <p>+34 91 123 45 67</p>
                            </div>
                        </div>
                        <div class="contacto-item">
                            <div class="contacto-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div class="contacto-texto">
                                <h4>Email</h4>
                                <p>info@ardeco-inmobiliaria.com</p>
                            </div>
                        </div>
                        <div class="contacto-item">
                            <div class="contacto-icon">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div class="contacto-texto">
                                <h4>Horario</h4>
                                <p>Lunes a Viernes: 9:00 - 19:00<br>Sábados: 10:00 - 14:00</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="contacto-form fade-in delay-1">
                    <form id="form-contacto">
                        <div class="form-group">
                            <label for="nombre">Nombre Completo</label>
                            <input type="text" id="nombre" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Correo Electrónico</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="telefono">Teléfono</label>
                            <input type="tel" id="telefono" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="mensaje">Mensaje</label>
                            <textarea id="mensaje" class="form-control" rows="5" placeholder="¿En qué podemos ayudarte?" required></textarea>
                        </div>
                        <button type="submit" class="btn" style="width: 100%;">Enviar Mensaje</button>
                    </form>
                </div>
            </div>
        </div>
    </section>
    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-contenido">
                <div class="footer-logo">
                    <h2>ARDECO</h2>
                    <p>Tu inmobiliaria de confianza. Más de 15 años ayudando a familias y empresas a encontrar su hogar ideal.</p>
                    <div class="footer-redes">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-links">
                    <h3 class="footer-titulo">Enlaces Rápidos</h3>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#propiedades">Propiedades</a></li>
                        <li><a href="#servicios">Servicios</a></li>
                        <li><a href="#nosotros">Sobre Nosotros</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h3 class="footer-titulo">Servicios</h3>
                    <ul>
                        <li><a href="#">Compra y Venta</a></li>
                        <li><a href="#">Alquileres</a></li>
                        <li><a href="#">Valoraciones</a></li>
                        <li><a href="#">Asesoría Legal</a></li>
                        <li><a href="#">Gestión de Comunidades</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h3 class="footer-titulo">Legal</h3>
                    <ul>
                        <li><a href="#">Política de Privacidad</a></li>
                        <li><a href="#">Aviso Legal</a></li>
                        <li><a href="#">Términos y Condiciones</a></li>
                        <li><a href="#">Política de Cookies</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-copyright">
                <p>&copy; 2023 ARDECO Inmobiliaria. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>
    <script>
        // Menú móvil
        document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
            const nav = document.querySelector('nav ul');
            nav.style.display = nav.style.display === 'flex' ? 'none' : 'flex';
        });
        // Formulario de contacto
        document.getElementById('form-contacto').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('¡Gracias por contactar con ARDECO! Nos pondremos en contacto contigo en breve.');
            this.reset();
        });
        // Animación al hacer scroll
        const observerOptions = {
            threshold: 0.1
        };
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);
        // Observar elementos con clase fade-in pero que aún no tienen la animación
        document.addEventListener('DOMContentLoaded', function() {
            const elements = document.querySelectorAll('.propiedad-card, .servicio-card, .sobre-texto, .sobre-imagen, .contacto-info, .contacto-form');
            elements.forEach(el => {
                observer.observe(el);
            });
        });
        // Suavizar scroll a secciones
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    // Cerrar menú móvil si está abierto
                    if (window.innerWidth <= 768) {
                        document.querySelector('nav ul').style.display = 'none';
                    }
                }
            });
        });
    </script>
</body>
</html>
