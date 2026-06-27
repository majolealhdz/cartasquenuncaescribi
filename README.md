<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cartas que nunca escribí - Landing Page Vintage</title>
    <style>
        /* Importación de tipografías complementarias desde Google Fonts */
        @import url('https://fonts.googleapis.com/css2?family=Courier+Prime:ital,wght@0,400;0,700;1,400&family=Special+Elite&family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=Reenie+Beanie&display=swap');

        /* NOTA SOBRE LAS TIPOGRAFÍAS DE TU PROYECTO:
           - Títulos / Subtítulos: El diseño requiere "29LTMakina" (mapeado aquí con 'Special Elite' / 'Courier Prime' como alternativa vintage).
           - Cuerpo de texto: El diseño requiere "The yougets" (mapeado con 'Cormorant Garamond' / 'Reenie Beanie' para emular el diario manuscrito nostálgico).
        */

        :root {
            /* Paleta de colores análoga, cálida, vintage y nostálgica (Café, Sepia, Pergamino, Terracota atenuado) */
            --bg-parchment: #f4eee1;
            --bg-cream: #faf6ee;
            --coffee-dark: #3e2723;
            --coffee-medium: #5d4037;
            --vintage-sepia: #8d6e63;
            --accent-terracota: #a14a38;
            --soft-border: #d7ccc8;
            --text-dark: #2d1f1e;
            --text-muted: #5c4e4c;

            --font-machina: '29LTMakina', 'Special Elite', 'Courier Prime', Courier, monospace;
            --font-yougets: 'The yougets', 'Cormorant Garamond', Georgia, serif;
            --font-script: 'Reenie Beanie', cursive;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: var(--font-yougets);
            background-color: var(--bg-parchment);
            color: var(--text-dark);
            line-height: 1.6;
            font-size: 17px;
        }

        /* Tipografías Generales */
        h1, h2, h3, h4, .font-machina {
            font-family: var(--font-machina);
            font-weight: normal;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: var(--coffee-dark);
        }

        p {
            margin-bottom: 1.2rem;
            color: var(--text-muted);
            text-align: justify;
        }

        .container {
            width: 100%;
            max-width: 1000px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* Header / Sección Inicial Estilo Rollo de Película Cinematográfica */
        header {
            background-color: #ebdcb9;
            background-image: radial-gradient(rgba(0,0,0,0.02) 1px, transparent 0);
            background-size: 24px 24px;
            padding: 80px 0 60px 0;
            text-align: center;
            border-bottom: 4px double var(--vintage-sepia);
            position: relative;
        }

        /* Simulación del rollo de película estético en la parte superior lateral */
        header::before {
            content: '';
            position: absolute;
            top: 0; left: 15px;
            width: 50px; height: 100%;
            background: linear-gradient(to bottom, #1a1a1a 70%, transparent 70%);
            background-size: 100% 20px;
            opacity: 0.15;
        }

        .hero-title {
            font-size: 2.8rem;
            line-height: 1.2;
            margin-bottom: 10px;
            color: var(--coffee-dark);
        }

        .hero-subtitle {
            font-size: 1.1rem;
            font-family: var(--font-machina);
            color: var(--vintage-sepia);
            margin-bottom: 35px;
        }

        .btn-action {
            display: inline-block;
            background-color: var(--coffee-dark);
            color: #ffffff;
            padding: 12px 45px;
            font-family: var(--font-machina);
            text-decoration: none;
            font-size: 0.95rem;
            letter-spacing: 2px;
            border: 1px solid var(--coffee-medium);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .btn-action:hover {
            background-color: var(--accent-terracota);
            transform: translateY(-1px);
        }

        /* Bloques de contenido con fondos alternados */
        .content-section {
            padding: 70px 0;
            border-bottom: 1px dashed var(--soft-border);
        }
        .bg-cream { background-color: var(--bg-cream); }
        .bg-parchment { background-color: var(--bg-parchment); }

        .section-title {
            font-size: 1.7rem;
            color: var(--coffee-dark);
            margin-bottom: 25px;
            line-height: 1.3;
            border-bottom: 1px solid var(--soft-border);
            padding-bottom: 8px;
            display: inline-block;
        }

        /* Layout de dos columnas adaptable */
        .grid-layout {
            display: block;
        }

        /* Estructura de imágenes polaroid vintage */
        .polaroid-container {
            display: flex;
            flex-direction: column;
            gap: 25px;
            align-items: center;
            margin-top: 35px;
        }

        .polaroid-card {
            background: #fbf9f5;
            padding: 14px 14px 40px 14px;
            box-shadow: 0 5px 15px rgba(40,30,20,0.08);
            border: 1px solid #e3dac9;
            width: 90%;
            max-width: 280px;
            transform: rotate(-1.5deg);
        }
        .polaroid-card:nth-child(2) {
            transform: rotate(2.5deg);
            margin-top: -10px;
        }

        .image-placeholder {
            width: 100%;
            height: 190px;
            background-color: #d7ccc8;
            background-image: repeating-linear-gradient(45deg, transparent, transparent 5px, rgba(255,255,255,.2) 5px, rgba(255,255,255,.2) 10px);
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: var(--font-machina);
            font-size: 0.75rem;
            color: var(--coffee-medium);
            text-align: center;
            padding: 10px;
        }

        /* Caja de Ilustración botánica o detalles */
        .illustration-box {
            text-align: center;
            margin-top: 30px;
        }
        .illustration-element {
            font-size: 5.5rem;
            color: #8fa89b;
            opacity: 0.75;
        }

        /* Elemento centralizado e imagen horizontal panorámica */
        .panoramic-image-box {
            width: 100%;
            max-width: 500px;
            height: 200px;
            background-color: #ccbfae;
            margin: 30px auto 0 auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: var(--font-machina);
            font-size: 0.85rem;
            color: var(--coffee-dark);
            border: 2px solid var(--soft-border);
        }

        /* Sección "Lo que encontrarás" - Hoja de nota manuscrita */
        .letter-paper {
            background: #ffffff;
            border-left: 4px solid var(--accent-terracota);
            padding: 35px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.04);
            margin: 35px auto 0 auto;
            max-width: 600px;
        }

        .letter-list {
            list-style: none;
        }

        .letter-list li {
            font-family: var(--font-machina);
            font-size: 0.95rem;
            padding: 14px 0;
            border-bottom: 1px dotted #dfd5c6;
            display: flex;
            align-items: baseline;
            color: var(--coffee-medium);
        }

        .letter-list li span {
            margin-right: 15px;
            color: var(--accent-terracota);
            font-weight: bold;
        }

        /* Bloque Epígrafe / Cita del libro */
        .quote-section {
            background-color: var(--coffee-dark);
            color: #f7f1e5;
            padding: 65px 24px;
            text-align: center;
        }

        .quote-section blockquote {
            font-family: var(--font-machina);
            font-size: 1.35rem;
            max-width: 750px;
            margin: 0 auto 25px auto;
            line-height: 1.5;
            color: #ebdcb9;
        }

        .quote-section p {
            color: #cfc0b1;
            font-size: 1.05rem;
            text-align: center;
            margin-bottom: 0;
            font-style: italic;
        }

        /* Cuadrícula para las fotografías finales del producto físico */
        .product-gallery-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-top: 35px;
        }

        .gallery-box {
            background: #ffffff;
            border: 1px solid var(--soft-border);
            padding: 8px;
        }

        .gallery-photo {
            width: 100%;
            height: 150px;
            background-color: #dfd5c6;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: var(--font-machina);
            font-size: 0.75rem;
            color: var(--coffee-medium);
            text-align: center;
        }

        /* Footer y Datos de la Autora */
        footer {
            background-color: #e5dac4;
            padding: 60px 0 40px 0;
            border-top: 2px solid var(--vintage-sepia);
        }

        .footer-layout {
            display: block;
        }

        .contact-header {
            font-size: 1.35rem;
            margin-bottom: 15px;
            color: var(--coffee-dark);
            line-height: 1.4;
        }

        .handwritten-highlight {
            font-family: var(--font-script);
            font-size: 3.2rem;
            color: var(--accent-terracota);
            display: block;
            margin: 10px 0;
        }

        .meta-list {
            list-style: none;
            margin: 25px 0;
        }

        .meta-list li {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .meta-list strong {
            font-family: var(--font-machina);
            font-size: 0.8rem;
            display: block;
            color: var(--accent-terracota);
        }

        .social-block h3 {
            font-size: 1.05rem;
            margin-bottom: 15px;
            color: var(--coffee-medium);
        }

        .social-box a {
            display: block;
            color: var(--text-dark);
            text-decoration: none;
            font-family: var(--font-machina);
            font-size: 0.9rem;
            margin-bottom: 12px;
            transition: color 0.2s ease;
        }

        .social-box a:hover {
            color: var(--accent-terracota);
        }

        .footer-bottom {
            text-align: center;
            margin-top: 45px;
            padding-top: 25px;
            border-top: 1px solid #cfc0b1;
            font-family: var(--font-machina);
            font-size: 0.75rem;
            color: var(--coffee-medium);
        }

        /* CONSULTAS DE MEDIOS (RESPONSIVO EN ESCRITORIO) */
        @media (min-width: 768px) {
            .grid-layout {
                display: grid;
                grid-template-columns: 1.2fr 0.8fr;
                gap: 50px;
                align-items: center;
            }

            .polaroid-container {
                margin-top: 0;
            }

            .illustration-box {
                margin-top: 0;
            }

            .product-gallery-grid {
                grid-template-columns: repeat(4, 1fr);
                gap: 20px;
            }

            .gallery-photo {
                height: 180px;
            }

            .footer-layout {
                display: grid;
                grid-template-columns: 1.2fr 0.8fr;
                gap: 50px;
            }

            .hero-title {
                font-size: 3.6rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container">
            <h1 class="hero-title">Cartas que nunca escribí</h1>
            <p class="hero-subtitle">De: Mí | Para: ¿?</p>
            <button class="btn-action" onclick="document.getElementById('sinopsis').scrollIntoView({behavior: 'smooth'});">EMPEZAR</button>
        </div>
    </header>

    <section class="content-section bg-cream">
        <div class="container">
            <div class="grid-layout">
                <div>
                    <h2 class="section-title">Palabras que siempre vivieron en mi corazón</h2>
                    <p>Hay sentimientos que deambulan esperando el momento correcto para ser expresados. Algunos procesos se quedan en silencio, mientras se editan ideas que de alguna manera buscan la forma de doler.</p>
                    <p>Este libro reúne esas cartas que durante mucho tiempo han estado en la lista de pensamientos, con la esperanza de que el amor, la gratitud y todo aquello que dolió de una u otra forma, pueda encontrar descanso.</p>
                </div>
                <div class="polaroid-container">
                    <div class="polaroid-card">
                        <div class="image-placeholder">[ Foto Proceso Interno ]</div>
                    </div>
                    <div class="polaroid-card">
                        <div class="image-placeholder">[ Fotografía Manuscrito ]</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="sinopsis" class="content-section bg-parchment">
        <div class="container">
            <div class="grid-layout">
                <div>
                    <h2 class="section-title">Sobre el libro</h2>
                    <p><strong>"Cartas que nunca escribí"</strong> es un compendio de correspondencias dedicadas de forma profunda a los seres más determinantes de mi existencia.</p>
                    <p>No recopila relatos de magnitudes épicas, sino los ínfimos fragmentos cotidianos que devienen en tesoros de la memoria: un abrazo inesperado, una palabra de aliento oportuna, un sacrificio silencioso o la frase exacta que jamás logramos pronunciar en vida. Es un recordatorio físico de que el amor también merece ser escuchado.</p>
                </div>
                <div class="illustration-box">
                    <div class="illustration-element">🌿</div>
                </div>
            </div>
        </div>
    </section>

    <section class="content-section bg-cream">
        <div class="container" style="max-width: 850px; text-align: center;">
            <h2 class="section-title">¿Por qué nació este libro?</h2>
            <p style="text-align: center;">Muchas veces amamos profundamente a personas sin que ellas alcancen a dimensionar lo que representan en nuestro mapa de vida. Y quizá nunca lo sepan con total certeza. Pero sostengo que todo aquello que se entrega genuinamente desde el afecto debe perdurar.</p>
            <p style="text-align: center;">Este volumen se materializó con ese propósito, gestado en un periodo cargado de incertidumbres que demandaban respuestas íntimas. Quise depositar un fragmento vivo de mi corazón en estas hojas para que, independientemente del rumbo hacia donde sople el viento, no olviden su valor.</p>
            
            <div class="panoramic-image-box">
                [ Fotografía Panorámica del Cuaderno Abierto ]
            </div>
        </div>
    </section>

    <section class="content-section bg-parchment">
        <div class="container">
            <h2 class="section-title" style="display: block; text-align: center; max-width: 300px; margin: 0 auto 30px auto;">Lo que encontrarás</h2>
            
            <div class="letter-paper">
                <ul class="letter-list">
                    <li><span>1.</span> Cartas escritas desde el absoluto desvelo.</li>
                    <li><span>2.</span> Instantes sutiles que redefinieron mi rumbo.</li>
                    <li><span>3.</span> Agradecimientos póstumos y presentes nunca antes expresados.</li>
                    <li><span>4.</span> Palabras de amor para quienes siempre permanecieron cerca.</li>
                </ul>
            </div>
        </div>
    </section>

    <div class="quote-section">
        <blockquote>
            "Hay cosas que nunca he sabido decirles de frente. Tal vez porque siempre he pensado que ya lo saben... pero el amor también merece escucharse."
        </blockquote>
        <p>Si este libro interactúa con alguien a quien amo, ruego que acaricien con fuerza sus páginas; solo así se impregnará la valía que tienen en mi vida, cumpliendo finalmente su cometido.</p>
    </div>

    <section class="content-section bg-cream">
        <div class="container">
            <h2 class="section-title">Diseño, Empaque y Muestras Físicas</h2>
            <p>El diseño de empaque y encuadernación rinde tributo a las texturas nostálgicas del papel envejecido, las costuras artesanales y la estética clásica del intercambio postal epistolar.</p>
            
            <div class="product-gallery-grid">
                <div class="gallery-box">
                    <div class="gallery-photo">[ Vista General Tomada de Lado ]</div>
                </div>
                <div class="gallery-box">
                    <div class="gallery-photo">[ Detalle de Páginas Internas ]</div>
                </div>
                <div class="gallery-box">
                    <div class="gallery-photo">[ Caligrafía a Detalle ]</div>
                </div>
                <div class="gallery-box">
                    <div class="gallery-photo">[ Cierre del Cuaderno ]</div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-layout">
                <div>
                    <h3 class="contact-header">¿Tienes alguna interrogante, comentario o deseas profundizar en el universo de este proyecto?</h3>
                    <span class="handwritten-highlight">Será un gusto leerte.</span>
                    
                    <ul class="meta-list">
                        <li>
                            <strong>Teléfono de contacto:</strong>
                            (123) 456-7890
                        </li>
                        <li>
                            <strong>Correo de correspondencia:</strong>
                            cartasquenuncaescribi@autor.com
                        </li>
                    </ul>
                </div>
                
                <div class="social-block">
                    <h3>Canales oficiales de la Autora</h3>
                    <div class="social-box">
                        <a href="#" target="_blank">📷 Instagram: @cartasquenuncaescribi</a>
                        <a href="#" target="_blank">👤 Facebook: Cartas que nunca escribí</a>
                    </div>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2026 Cartas que nunca escribí. Todos los derechos de autor reservados.</p>
            </div>
        </div>
    </footer>

</body>
</html>
