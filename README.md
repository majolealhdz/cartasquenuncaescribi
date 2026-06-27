<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cartas que nunca escribí - Landing Page</title>
    <style>
        /* Importación de fuentes de Google Fonts que simulan los estilos requeridos */
        @import url('https://fonts.googleapis.com/css2?family=Courier+Prime:ital,wght@0,400;0,700;1,400&family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Caveat:wght@400..700&display=swap');

        /* NOTAS SOBRE TIPOGRAFÍAS DE LA MAQUETA:
          - Títulos y subtítulos: Reemplazar el fallback ('Courier Prime') por tu fuente local '29LTMakina' si dispones del archivo webfont (.woff2).
          - Cuerpo de texto: Reemplazar el fallback ('Playfair Display') por tu fuente local 'The yougets'.
        */

        :root {
            /* Paleta de colores: Vibrante cálida con armonía análoga (Terracota, Coral, Ocre, Arena) */
            --bg-base: #f9f4ed;
            --primary-warm: #d96b43;   /* Terracota vibrante */
            --secondary-warm: #e8a75a; /* Ocre cálido */
            --accent-coral: #e25b5b;   /* Coral / Rosa vibrante de la maqueta */
            --text-dark: #3a2e2b;
            --text-muted: #6e5d58;
            --card-bg: #ffffff;
            
            --font-titles: '29LTMakina', 'Courier Prime', Courier, monospace;
            --font-body: 'The yougets', 'Playfair Display', Georgia, serif;
            --font-handwritten: 'Caveat', cursive;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: var(--font-body);
            background-color: var(--bg-base);
            color: var(--text-dark);
            line-height: 1.6;
            font-size: 16px;
        }

        /* Estilos de Textos y Títulos */
        h1, h2, h3, h4, .font-machina {
            font-family: var(--font-titles);
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            color: var(--text-muted);
        }

        .highlight-text {
            font-family: var(--font-handwritten);
            font-size: 2.2rem;
            color: var(--accent-coral);
            line-height: 1.2;
        }

        /* Contenedores */
        .container {
            width: 100%;
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header / Hero Section */
        header {
            background: linear-gradient(135deg, #fdfaf6 0%, #f3ede2 100%);
            padding: 80px 0 60px 0;
            text-align: center;
            border-bottom: 2px dashed var(--secondary-warm);
            position: relative;
        }

        header::before {
            content: "★ ★ ★";
            position: absolute;
            top: 25px;
            left: 50%;
            transform: translateX(-50%);
            color: var(--secondary-warm);
            font-size: 1.2rem;
            letter-spacing: 10px;
        }

        .hero-title {
            font-size: 2.8rem;
            color: var(--text-dark);
            margin-top: 20px;
            margin-bottom: 5px;
            line-height: 1.2;
        }

        .hero-subtitle {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-bottom: 35px;
            font-family: var(--font-titles);
        }

        .btn-start {
            display: inline-block;
            background-color: var(--text-dark);
            color: #ffffff;
            padding: 12px 40px;
            font-family: var(--font-titles);
            text-decoration: none;
            font-size: 0.9rem;
            letter-spacing: 2px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .btn-start:hover {
            background-color: var(--primary-warm);
            transform: translateY(-2px);
        }

        /* Sección Introductoria (Palabras que siempre vivieron...) */
        .intro-section {
            padding: 60px 0;
            background-color: #faf6f0;
        }

        .grid-intro {
            display: block;
        }

        .section-title {
            font-size: 1.8rem;
            color: var(--primary-warm);
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background-color: var(--accent-coral);
        }

        /* Fotos tipo Polaroid decorativas */
        .photo-gallery-preview {
            display: flex;
            flex-direction: column;
            gap: 20px;
            align-items: center;
            margin-top: 30px;
        }

        .polaroid {
            background: #ffffff;
            padding: 15px 15px 35px 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            border: 1px solid #e2ded8;
            transform: rotate(-2deg);
            width: 85%;
            max-width: 260px;
            transition: transform 0.3s ease;
        }

        .polaroid:nth-child(2) {
            transform: rotate(3deg);
            margin-top: -15px;
        }

        .polaroid:hover {
            transform: rotate(0deg) scale(1.03);
        }

        .polaroid-img-placeholder {
            width: 100%;
            height: 180px;
            background-color: #e2ded8;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: var(--font-titles);
            font-size: 0.8rem;
            color: #8c8581;
        }

        /* Bloques de Contenido Generales */
        .content-block {
            padding: 60px 0;
            border-top: 1px solid #ebdcd0;
        }

        .bg-white { background-color: #ffffff; }
        .bg-warm-light { background-color: #fdf9f3; }

        /* Estilo para Sinopsis y Elementos con Ilustración Lateral */
        .grid-two-columns {
            display: block;
        }

        .decorative-illustration {
            text-align: center;
            padding: 20px;
            margin-top: 20px;
        }

        .plant-icon {
            font-size: 5rem;
            color: #8fa89b; /* Color sage/hoja de la maqueta original */
            opacity: 0.8;
        }

        /* Sección "Lo que encontrarás" - Estilo Nota Torn */
        .notebook-page {
            background: #ffffff;
            border-left: 5px solid var(--accent-coral);
            padding: 30px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.05);
            margin: 30px auto;
            max-width: 650px;
            position: relative;
        }

        .notebook-page::before {
            content: '';
            position: absolute;
            top: 0; right: 20px;
            width: 30px; height: 30px;
            background-color: var(--secondary-warm);
            opacity: 0.3;
            clip-path: polygon(0 0, 100% 0, 100% 100%);
        }

        .notebook-list {
            list-style: none;
        }

        .notebook-list li {
            font-family: var(--font-titles);
            font-size: 1rem;
            padding: 12px 0;
            border-bottom: 1px dashed #e2ded8;
            display: flex;
            align-items: baseline;
        }

        .notebook-list li span {
            margin-right: 15px;
            color: var(--primary-warm);
            font-weight: bold;
        }

        /* Bloque de Cita Destacada */
        .quote-banner {
            background-color: var(--primary-warm);
            color: #ffffff;
            padding: 60px 20px;
            text-align: center;
        }

        .quote-banner blockquote {
            font-family: var(--font-titles);
            font-size: 1.4rem;
            max-width: 800px;
            margin: 0 auto 20px auto;
            line-height: 1.5;
        }

        .quote-banner p {
            color: #ffe6dd;
            font-size: 1.1rem;
            margin-bottom: 0;
        }

        /* Galería de Fotografías del Producto y Proceso */
        .product-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .gallery-item {
            background: #ffffff;
            border: 1px solid #ebdcd0;
            padding: 12px;
            text-align: center;
            box-shadow: 0 2px 8px rgba(0,0,0,0.02);
        }

        .gallery-img-box {
            width: 100%;
            height: 220px;
            background-color: #f0e6dc;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: var(--font-titles);
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 12px;
        }

        .gallery-item h4 {
            font-size: 0.9rem;
            color: var(--text-dark);
            margin-top: 5px;
        }

        /* Footer / Contacto y Redes Sociales */
        footer {
            background-color: #ede5da;
            padding: 60px 0 40px 0;
            border-top: 3px solid var(--secondary-warm);
        }

        .footer-grid {
            display: block;
        }

        .contact-info h3 {
            font-size: 1.4rem;
            color: var(--text-dark);
            margin-bottom: 15px;
        }

        .contact-details {
            list-style: none;
            margin-top: 25px;
            margin-bottom: 30px;
        }

        .contact-details li {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .contact-details strong {
            font-family: var(--font-titles);
            display: block;
            font-size: 0.85rem;
            color: var(--primary-warm);
            margin-bottom: 2px;
        }

        .social-links a {
            display: block;
            color: var(--text-dark);
            text-decoration: none;
            font-family: var(--font-titles);
            margin-bottom: 12px;
            font-size: 0.95rem;
            transition: color 0.2s ease;
        }

        .social-links a:hover {
            color: var(--accent-coral);
        }

        .copyright {
            text-align: center;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 1px solid #dbcfc2;
            font-family: var(--font-titles);
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        /* MEDIA QUERIES PARA RESPONSIVIDAD (DESKTOP) */
        @media (min-width: 768px) {
            .grid-intro {
                display: grid;
                grid-template-columns: 1.2fr 0.8fr;
                gap: 50px;
                align-items: center;
            }

            .photo-gallery-preview {
                flex-direction: column;
                margin-top: 0;
            }

            .grid-two-columns {
                display: grid;
                grid-template-columns: 1fr 1fr;
                gap: 50px;
                align-items: center;
            }

            .footer-grid {
                display: grid;
                grid-template-columns: 1.2fr 0.8fr;
                gap: 60px;
            }

            .contact-details {
                margin-bottom: 0;
            }

            .hero-title {
                font-size: 3.8rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container">
            <h1 class="hero-title">Cartas que nunca escribí</h1>
            <p class="hero-subtitle">De: Mí | Para: ¿?</p>
            <button class="btn-start" onclick="document.getElementById('sinopsis').scrollIntoView({behavior: 'smooth'});">EMPEZAR</button>
        </div>
    </header>

    <section class="intro-section">
        <div class="container">
            <div class="grid-intro">
                <div>
                    <h2 class="section-title">Palabras que siempre vivieron en mi corazón</h2>
                    <p>Hay sentimientos que deambulan esperando el momento correcto para ser expresados. Algunos procesos se quedan en silencio, mientras se editan ideas que de alguna manera buscan la forma de doler.</p>
                    <p>Este libro reúne esas cartas que durante mucho tiempo han estado en la lista de pensamientos, con la esperanza de que el amor, la gratitud y todo aquello que dolió, de una u otra manera, pueda sanar.</p>
                </div>
                <div class="photo-gallery-preview">
                    <div class="polaroid">
                        <div class="polaroid-img-placeholder">[ Fotografía del Proceso ]</div>
                    </div>
                    <div class="polaroid">
                        <div class="polaroid-img-placeholder">[ Vista del Libro ]</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="sinopsis" class="content-block bg-white">
        <div class="container">
            <div class="grid-two-columns">
                <div>
                    <h2 class="section-title">Sobre el libro</h2>
                    <p><strong>"Cartas que nunca escribí"</strong> es un libro de cartas dedicadas a las personas más importantes de mi vida.</p>
                    <p>No habla de grandes historias, sino de los pequeños momentos que terminan convirtiéndose en los recuerdos más valiosos: un abrazo, una palabra de aliento, un sacrificio que pasó desapercibido o una frase que nunca se dijo en vida. Es un recordatorio de que el amor también merece escribirse.</p>
                </div>
                <div class="decorative-illustration">
                    <span class="plant-icon">🌿</span>
                </div>
            </div>
        </div>
    </section>

    <section class="content-block bg-warm-light">
        <div class="container" style="max-width: 800px; text-align: center;">
            <h2 class="section-title" style="margin: 0 auto 25px auto; display: inline-block;">¿Por qué nació este libro?</h2>
            <p>Muchas veces amamos profundamente a personas sin saber lo que representan para ellas. Y quizá no se enteren. Pero también creo que lo que se da con amor tiene que quedarse para siempre. Este libro nació con ese fin, en un tiempo de muchas dudas y que requería de una respuesta. Quise dejar un pedacito de mi corazón en estas páginas para que, sin importar a dónde las lleve el viento, recuerden qué significan para mí.</p>
        </div>
    </section>

    <section class="content-block bg-white">
        <div class="container">
            <h2 class="section-title" style="text-align: center; margin: 0 auto 30px auto; display: block; max-width: 320px;">Lo que encontrarás</h2>
            
            <div class="notebook-page">
                <ul class="notebook-list">
                    <li><span>1.</span> Cartas escritas desde el corazón.</li>
                    <li><span>2.</span> Instantes que marcaron mi vida.</li>
                    <li><span>3.</span> Agradecimientos que nunca había expresado.</li>
                    <li><span>4.</span> Palabras de amor para quienes siempre estuvieron conmigo.</li>
                </ul>
            </div>
        </div>
    </section>

    <div class="quote-banner">
        <blockquote>
            "Hay cosas que nunca he sabido decirles de frente. Tal vez porque siempre he pensado que ya lo saben... pero el amor también merece escucharse."
        </blockquote>
        <p>Si este libro llega a alguien que amo, pasen más fuerte a sus páginas para que se quede grabado un pedacito de lo que valen en mi vida, y entonces habrá cumplido su propósito.</p>
    </div>

    <section class="content-block bg-warm-light">
        <div class="container">
            <h2 class="section-title">Proceso Creativo, Empaque y Diseño</h2>
            <p>Cada elemento visual y táctil de este libro ha sido diseñado minuciosamente para reflejar la intimidad de una carta manuscrita. El empaque rescata texturas orgánicas artesanales con detalles únicos pensados en la experiencia del lector.</p>
            
            <div class="product-gallery">
                <div class="gallery-item">
                    <div class="gallery-img-box">[ Concepto e Ideas ]</div>
                    <h4>Proceso Creativo</h4>
                </div>
                <div class="gallery-item">
                    <div class="gallery-img-box">[ Retículas y Tipografía ]</div>
                    <h4>Proceso de Diseño</h4>
                </div>
                <div class="gallery-item">
                    <div class="gallery-img-box">[ Caja / Envoltura ]</div>
                    <h4>El Empaque</h4>
                </div>
                <div class="gallery-item">
                    <div class="gallery-img-box">[ Fotografía de Producto ]</div>
                    <h4>Producto Terminado</h4>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="contact-info">
                    <h3>¿Tienes alguna pregunta, comentario o te gustaría conocer más sobre Cartas que nunca escribí?</h3>
                    <p class="highlight-text">Será un gusto leerte.</p>
                    
                    <ul class="contact-details">
                        <li>
                            <strong>Teléfono:</strong>
                            (123) 456-7890
                        </li>
                        <li>
                            <strong>Correo electrónico:</strong>
                            cartasquenuncaescribi@autor.com
                        </li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="font-machina" style="font-size: 1.1rem; margin-bottom: 20px; color: var(--primary-warm);">Redes Sociales de la Autora</h3>
                    <div class="social-links">
                        <a href="#" target="_blank">📷 Instagram: @cartasquenuncaescribi</a>
                        <a href="#" target="_blank">👤 Facebook: Cartas que nunca escribí</a>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2026 Cartas que nunca escribí. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

</body>
</html>
