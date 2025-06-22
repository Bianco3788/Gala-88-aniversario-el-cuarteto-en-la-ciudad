<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gala Aniversario: 88 Años de Escuela Bianco</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Inter Font -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(to bottom right, #fef2f2, #fecaca); /* Lighter red gradient for radiance */
            color: #262626; /* Darker gray for better contrast */
        }
        .container {
            max-width: 1200px;
        }
        .section-title {
            position: relative;
            display: inline-block;
            padding-bottom: 8px;
            margin-bottom: 24px;
            color: #b91c1c; /* Deeper red for titles */
        }
        .section-title::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 50%;
            height: 5px; /* Slightly thicker line */
            background-color: #dc2626; /* red-600 */
            border-radius: 2px;
        }
        .memory-box {
            background-color: #fff;
            border-left: 5px solid #ef4444; /* red-500 */
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15); /* More prominent shadow */
            border-radius: 0.75rem; /* Rounded corners */
        }
        .modal {
            display: none; /* Hidden by default */
            position: fixed; /* Stay in place */
            z-index: 1000; /* Sit on top */
            left: 0;
            top: 0;
            width: 100%; /* Full width */
            height: 100%; /* Full height */
            overflow: auto; /* Enable scroll if needed */
            background-color: rgba(0,0,0,0.6); /* Darker overlay */
            justify-content: center;
            align-items: center;
        }
        .modal-content {
            background-color: #fefefe;
            margin: auto;
            padding: 30px; /* More padding */
            border-radius: 12px; /* More rounded */
            box-shadow: 0 8px 20px rgba(0,0,0,0.4); /* Stronger shadow */
            width: 90%;
            max-width: 550px;
            position: relative;
            animation: fadeIn 0.3s ease-out; /* Fade in animation */
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .close-button {
            color: #737373; /* Gray-600 */
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 32px; /* Larger */
            font-weight: bold;
            cursor: pointer;
            transition: color 0.2s ease-in-out;
        }
        .close-button:hover,
        .close-button:focus {
            color: #ef4444; /* red-500 */
        }
        /* Custom styles for the timeline/history section */
        .timeline-item {
            display: flex;
            margin-bottom: 2.5rem; /* More spacing */
            position: relative;
        }
        .timeline-item:nth-child(odd) {
            flex-direction: row-reverse;
        }
        .timeline-date {
            min-width: 130px; /* Slightly wider */
            text-align: center;
            font-weight: 800; /* Extra bold */
            color: #dc2626; /* red-600 */
            font-size: 1.35rem; /* Slightly larger */
            line-height: 1.2;
        }
        .timeline-content {
            flex-grow: 1;
            background-color: #fff;
            padding: 1.75rem; /* More padding */
            border-radius: 0.85rem; /* More rounded */
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.15); /* Improved shadow */
            position: relative;
            margin: 0 1.25rem; /* More margin */
        }
        .timeline-content::before {
            content: '';
            position: absolute;
            top: 1.75rem;
            width: 0;
            height: 0;
            border-style: solid;
        }
        .timeline-item:nth-child(even) .timeline-content::before {
            left: -18px; /* Adjusted for larger arrow */
            border-width: 12px 18px 12px 0;
            border-color: transparent #fff transparent transparent;
        }
        .timeline-item:nth-child(odd) .timeline-content::before {
            right: -18px; /* Adjusted for larger arrow */
            border-width: 12px 0 12px 18px;
            border-color: transparent transparent transparent #fff;
        }
        .timeline-line {
            position: absolute;
            left: 50%;
            width: 5px; /* Thicker line */
            background-color: #dc2626; /* red-600 */
            top: 0;
            bottom: 0;
            transform: translateX(-50%);
        }
        .timeline-dot {
            width: 24px; /* Larger dot */
            height: 24px;
            background-color: #dc2626; /* red-600 */
            border: 3px solid #fef2f2; /* Light border */
            border-radius: 50%;
            position: absolute;
            left: 50%;
            top: 1.5rem; /* Adjusted position */
            transform: translateX(-50%);
            z-index: 10;
            box-shadow: 0 0 0 5px rgba(220, 38, 38, 0.3); /* Pulsing effect */
        }
        @media (max-width: 768px) {
            .timeline-item {
                flex-direction: column !important;
                align-items: flex-start;
            }
            .timeline-date {
                text-align: left;
                margin-bottom: 0.75rem;
            }
            .timeline-content {
                margin: 0;
                width: calc(100% - 30px); /* Adjust for dot and line */
                margin-left: 30px; /* Space for the line and dot */
            }
            .timeline-content::before {
                left: -18px;
                border-width: 12px 18px 12px 0;
                border-color: transparent #fff transparent transparent;
                top: 1.75rem;
            }
            .timeline-line {
                left: 12px; /* Adjusted position */
                transform: translateX(0);
            }
            .timeline-dot {
                left: 0;
                transform: translateX(0);
                top: 1.75rem; /* Adjusted position */
            }
        }
    </style>
</head>
<body class="bg-red-50 text-neutral-800">

    <!-- Header Section -->
    <header class="bg-white shadow-lg py-6 sticky top-0 z-50 border-b-4 border-red-700">
        <div class="container mx-auto px-6 flex flex-col md:flex-row justify-between items-center">
            <h1 class="text-3xl font-extrabold text-red-700 mb-4 md:mb-0 flex items-center">
                <!-- Logo de la Gala Aniversario (SVG) -->
                <svg width="250" height="60" viewBox="0 0 250 60" fill="none" xmlns="http://www.w3.org/2000/svg" class="mr-3">
                    <rect x="0" y="0" width="250" height="60" fill="white"/>
                    <text x="10" y="45" font-family="Inter" font-weight="900" font-size="40" fill="#dc2626">88</text>
                    <text x="75" y="30" font-family="Inter" font-weight="700" font-size="20" fill="#a16207">Años</text>
                    <text x="75" y="50" font-family="Inter" font-weight="700" font-size="20" fill="#262626">Escuela Bianco</text>
                    <path d="M210 20C205 25 200 30 200 35C200 40 205 45 210 50" stroke="#facc15" stroke-width="4" stroke-linecap="round"/>
                    <circle cx="210" cy="20" r="5" fill="#facc15"/>
                    <circle cx="210" cy="50" r="5" fill="#facc15"/>
                    <path d="M225 35L235 35L240 30L245 35L240 40L235 35Z" fill="#a16207"/>
                </svg>
                <span class="sr-only">Gala Aniversario: 88 Años de Escuela Bianco</span>
            </h1>
            <nav>
                <ul class="flex space-x-6">
                    <li><a href="#about" class="text-neutral-600 hover:text-red-700 font-semibold transition duration-300">Sobre la Gala</a></li>
                    <li><a href="#program" class="text-neutral-600 hover:text-red-700 font-semibold transition duration-300">Programa</a></li>
                    <li><a href="#history" class="text-neutral-600 hover:text-red-700 font-semibold transition duration-300">Historia del Cuarteto</a></li>
                    <li><a href="#gallery" class="text-neutral-600 hover:text-red-700 font-semibold transition duration-300">Galería</a></li>
                    <li><a href="#interactive" class="text-neutral-600 hover:text-red-700 font-semibold transition duration-300">Interactúa</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative bg-cover bg-center h-96 flex items-center justify-center text-white" style="background-image: url('https://placehold.co/1200x500/B91C1C/FFFFFF?text=Gala+Aniversario+Escuela+Bianco');">
        <div class="absolute inset-0 bg-black opacity-65"></div>
        <div class="z-10 text-center px-6">
            <h2 class="text-5xl font-extrabold mb-4 animate-fade-in-down drop-shadow-lg">¡Celebra con Nosotros 88 Años de Historia y Ritmo!</h2>
            <p class="text-xl mb-8 animate-fade-in-up drop-shadow-md">Un viaje musical por el cuarteto cordobés y la trayectoria de la Escuela Bianco.</p>
            <a href="#about" class="bg-red-700 hover:bg-red-800 text-white font-bold py-3 px-8 rounded-full shadow-xl transition duration-300 transform hover:scale-105 active:scale-95 inline-flex items-center group">
                Descubre Más <i class="fas fa-arrow-down ml-3 group-hover:translate-y-1 transition-transform duration-300"></i>
            </a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-16 bg-white shadow-inner">
        <div class="container mx-auto px-6 text-center">
            <h3 class="text-4xl font-extrabold mb-8 section-title mx-auto">Sobre la Gala</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="bg-red-50 p-6 rounded-lg shadow-xl flex flex-col items-center border-b-4 border-red-400 transform hover:scale-105 transition duration-300">
                    <i class="fas fa-calendar-alt text-5xl text-red-600 mb-4"></i>
                    <h4 class="text-2xl font-bold mb-2 text-red-700">Fecha y Hora</h4>
                    <p class="text-lg text-neutral-700">28 de noviembre de 2025</p>
                    <p class="text-lg text-neutral-700">21:30 hs</p>
                </div>
                <div class="bg-red-50 p-6 rounded-lg shadow-xl flex flex-col items-center border-b-4 border-red-400 transform hover:scale-105 transition duration-300">
                    <i class="fas fa-map-marker-alt text-5xl text-red-600 mb-4"></i>
                    <h4 class="text-2xl font-bold mb-2 text-red-700">Lugar</h4>
                    <p class="text-lg text-neutral-700">Nuevo Salón de los Deportes de Villa María</p>
                </div>
                <div class="bg-red-50 p-6 rounded-lg shadow-xl flex flex-col items-center border-b-4 border-red-400 transform hover:scale-105 transition duration-300">
                    <i class="fas fa-music text-5xl text-red-600 mb-4"></i>
                    <h4 class="text-2xl font-bold mb-2 text-red-700">Eje Temático</h4>
                    <p class="text-lg text-neutral-700">Historia sincrónica del cuarteto cordobés y los 88 años de la Escuela Bianco, explorando su evolución.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Program Section -->
    <section id="program" class="py-16 bg-gradient-to-br from-red-100 to-red-200">
        <div class="container mx-auto px-6">
            <h3 class="text-4xl font-extrabold mb-12 text-center section-title mx-auto">Cronograma del Evento</h3>

            <!-- Pre-Gala and Immersive Reception -->
            <div class="bg-white p-8 rounded-lg shadow-2xl mb-10 border-l-8 border-red-600">
                <h4 class="text-3xl font-bold text-red-700 mb-4 flex items-center"><i class="fas fa-cocktail mr-3 text-red-500"></i> Pre-Gala y Recepción Inmersiva <span class="ml-auto text-neutral-600 text-xl">(20:00 - 21:30 hs)</span></h4>
                <ul class="list-disc list-inside text-lg space-y-3 text-neutral-700">
                    <li><strong class="text-neutral-900">Ambiente "Callejero Cordobés":</strong> Un pasillo que simula una calle típica de Córdoba con fachadas y grafitis alusivos al cuarteto.</li>
                    <li><strong class="text-neutral-900">Música de Fondo Evolutiva:</strong> Desde tangos y pasodobles hasta los primeros cuartetos y clásicos.</li>
                    <li><strong class="text-neutral-900">Exposición Interactiva "88 Años de Historia y Ritmo":</strong>
                        <ul class="list-circle list-inside ml-6 mt-2 space-y-2">
                            <li>Galería Fotográfica Digital con proyecciones y códigos QR.</li>
                            <li>Línea de Tiempo Sensorial del Cuarteto con auriculares y fragmentos de canciones.</li>
                            <li>"Tu Cuarteto, Tu Historia": Photobooth interactivo con atrezzo y hashtag <span class="text-red-600 font-mono">#BiancoCuarteto88</span>.</li>
                        </ul>
                    </li>
                </ul>
            </div>

            <!-- Gala Start -->
            <div class="bg-white p-8 rounded-lg shadow-2xl mb-10 border-l-8 border-red-600">
                <h4 class="text-3xl font-bold text-red-700 mb-4 flex items-center"><i class="fas fa-bullhorn mr-3 text-red-500"></i> Inicio de la Gala: El Telón se Abre <span class="ml-auto text-neutral-600 text-xl">(21:30 - 21:50 hs)</span></h4>
                <ul class="list-disc list-inside text-lg space-y-3 text-neutral-700">
                    <li><strong class="text-neutral-900">Apertura Oficial y "El Latido de la Ciudad":</strong> Cortometraje que combina imágenes históricas de Villa María y la Escuela Bianco con bailes de cuarteto.</li>
                    <li><strong class="text-neutral-900">Palabras del Director/a:</strong> Breve reseña de los 88 años de la escuela y su vínculo con la identidad cultural cordobesa.</li>
                    <li><strong class="text-neutral-900">Narradores del Evento: "Cronistas del Tunga-Tunga":</strong> Dos estudiantes de sexto grado introducirán cada bloque con datos curiosos y anécdotas.</li>
                </ul>
            </div>

            <!-- Grade Presentations -->
            <div class="bg-white p-8 rounded-lg shadow-2xl mb-10 border-l-8 border-red-600">
                <h4 class="text-3xl font-bold text-red-700 mb-4 flex items-center"><i class="fas fa-users-class mr-3 text-red-500"></i> Presentaciones por Grado: Un Viaje en el Tiempo <span class="ml-auto text-neutral-600 text-xl">(21:50 - 23:00 hs)</span></h4>
                <p class="text-lg mb-4 text-neutral-700">Cada bloque será una "cápsula del tiempo" con narración contextual, baile representativo y transición "Puente Temporal".</p>
                <div class="overflow-x-auto">
                    <table class="min-w-full bg-white rounded-lg shadow-md border border-gray-200">
                        <thead class="bg-red-700 text-white">
                            <tr>
                                <th class="py-3 px-4 text-left rounded-tl-lg">Grado</th>
                                <th class="py-3 px-4 text-left">Época Representada</th>
                                <th class="py-3 px-4 text-left">Grupos Musicales</th>
                                <th class="py-3 px-4 text-left">Vestuario y Baile</th>
                                <th class="py-3 px-4 text-left rounded-tr-lg">Duración</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr class="border-b border-gray-200 hover:bg-red-50">
                                <td class="py-3 px-4 text-neutral-800 font-semibold">1º Grado</td>
                                <td class="py-3 px-4 text-neutral-700">Década de 1940 (Orígenes)</td>
                                <td class="py-3 px-4 text-neutral-700">Cuarteto Leo, La Leo</td>
                                <td class="py-3 px-4 text-neutral-700">Trajes elegantes, pasos básicos de cuarteto primitivo.</td>
                                <td class="py-3 px-4 text-neutral-700">21:50-22:00 hs</td>
                            </tr>
                            <tr class="border-b border-gray-200 hover:bg-red-50">
                                <td class="py-3 px-4 text-neutral-800 font-semibold">2º Grado</td>
                                <td class="py-3 px-4 text-neutral-700">Década de 1950-1960 (Consolidación)</td>
                                <td class="py-3 px-4 text-neutral-700">Cuarteto Berna, Cuarteto Carusso</td>
                                <td class="py-3 px-4 text-neutral-700">Estilo "vintage", movimientos rítmicos con giros suaves.</td>
                                <td class="py-3 px-4 text-neutral-700">22:00-22:10 hs</td>
                            </tr>
                            <tr class="border-b border-gray-200 hover:bg-red-50">
                                <td class="py-3 px-4 text-neutral-800 font-semibold">3º Grado</td>
                                <td class="py-3 px-4 text-neutral-700">Década de 1970 (Revolución "Mona")</td>
                                <td class="py-3 px-4 text-neutral-700">Carlos "La Mona" Jiménez, Cuarteto de Oro</td>
                                <td class="py-3 px-4 text-neutral-700">Pantalones campana, camisas psicodélicas, saltos y zapateos enérgicos.</td>
                                <td class="py-3 px-4 text-neutral-700">22:10-22:20 hs</td>
                            </tr>
                            <tr class="border-b border-gray-200 hover:bg-red-50">
                                <td class="py-3 px-4 text-neutral-800 font-semibold">4º Grado</td>
                                <td class="py-3 px-4 text-neutral-700">Década de 1980 (Explosión popular y "Tunga-Tunga")</td>
                                <td class="py-3 px-4 text-neutral-700">Rodrigo (primeros años), Chébere, Tru-la-lá</td>
                                <td class="py-3 px-4 text-neutral-700">Jeans ajustados, remeras holgadas, "Tunga-tunga" rápido.</td>
                                <td class="py-3 px-4 text-neutral-700">22:20-22:30 hs</td>
                            </tr>
                            <tr class="border-b border-gray-200 hover:bg-red-50">
                                <td class="py-3 px-4 text-neutral-800 font-semibold">5º Grado</td>
                                <td class="py-3 px-4 text-neutral-700">Década de 1990 (Época dorada y Expansión)</td>
                                <td class="py-3 px-4 text-neutral-700">La Barra, Tru-la-lá, Jean Carlos</td>
                                <td class="py-3 px-4 text-neutral-700">Camisas floreadas, chalecos, minifaldas, coreografías grupales.</td>
                                <td class="py-3 px-4 text-neutral-700">22:30-22:40 hs</td>
                            </tr>
                            <tr class="border-b border-gray-200 hover:bg-red-50">
                                <td class="py-3 px-4 text-neutral-800 font-semibold">6º Grado</td>
                                <td class="py-3 px-4 text-neutral-700">2000-Actualidad (Fusión, Globalización y Redes)</td>
                                <td class="py-3 px-4 text-neutral-700">Ulises Bueno, La Banda XXI, Konga, Q' Lokura</td>
                                <td class="py-3 px-4 text-neutral-700">Estilo urbano, coreografía moderna con pasos virales.</td>
                                <td class="py-3 px-4 text-neutral-700">22:40-22:50 hs</td>
                            </tr>
                            <tr class="border-b border-gray-200 hover:bg-red-50">
                                <td class="py-3 px-4 text-neutral-800 font-semibold">Intervención Especial</td>
                                <td class="py-3 px-4 text-neutral-700">Docentes y Staff</td>
                                <td class="py-3 px-4 text-neutral-700">Sorpresa</td>
                                <td class="py-3 px-4 text-neutral-700">Coreografía de sorpresa, generando un momento divertido y emotivo.</td>
                                <td class="py-3 px-4 text-neutral-700">22:50-23:00 hs</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>

            <!-- Grand Finale -->
            <div class="bg-white p-8 rounded-lg shadow-2xl mb-10 border-l-8 border-red-600">
                <h4 class="text-3xl font-bold text-red-700 mb-4 flex items-center"><i class="fas fa-fire-alt mr-3 text-red-500"></i> Gran Final: La Fiesta de la Ciudad <span class="ml-auto text-neutral-600 text-xl">(23:00 - 23:20 hs)</span></h4>
                <ul class="list-disc list-inside text-lg space-y-3 text-neutral-700">
                    <li><strong class="text-neutral-900">"El Gran Baile de la Ciudad":</strong> Todos los grados bailan juntos un popurrí de hits del cuarteto.</li>
                    <li><strong class="text-neutral-900">Impacto Visual:</strong> Cañones de confeti, serpentinas, luces estroboscópicas y efectos de humo.</li>
                    <li><strong class="text-neutral-900">Proyección Mapeada:</strong> Imágenes dinámicas y abstractas que reaccionan a la música.</li>
                    <li><strong class="text-neutral-900">Homenaje a los 88 Años y Legado:</strong> Pastel Gigante de Luces (proyección), Canción Emotiva, Acto Simbólico "El Legado Continúa" formando el número "88" y el logo de la escuela.</li>
                </ul>
            </div>

            <!-- Closing and Thanks -->
            <div class="bg-white p-8 rounded-lg shadow-2xl border-l-8 border-red-600">
                <h4 class="text-3xl font-bold text-red-700 mb-4 flex items-center"><i class="fas fa-handshake mr-3 text-red-500"></i> Cierre y Agradecimientos: La Noche No Termina <span class="ml-auto text-neutral-600 text-xl">(23:20 - 23:40 hs)</span></h4>
                <ul class="list-disc list-inside text-lg space-y-3 text-neutral-700">
                    <li><strong class="text-neutral-900">Palabras Finales:</strong> Docentes y directivos destacan el trabajo colaborativo y el valor educativo del proyecto.</li>
                    <li><strong class="text-neutral-900">Invitación al "Baile Abierto en la Ciudad":</strong> Pista de baile abierta con DJ profesional y mini-clase de cuarteto.</li>
                    <li><strong class="text-neutral-900">Detalle Conmemorativo "Recuerdo del Tunga":</strong> Entrega de imanes con forma de "tunga" y pequeños dulces regionales.</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- History of Cuarteto Section -->
    <section id="history" class="py-16 bg-gradient-to-tl from-gray-50 to-gray-100">
        <div class="container mx-auto px-6">
            <h3 class="text-4xl font-extrabold mb-12 text-center section-title mx-auto">La Historia del Cuarteto Cordobés</h3>
            <div class="relative">
                <div class="timeline-line"></div>
                <div class="timeline-item">
                    <div class="timeline-date">1943</div>
                    <div class="timeline-content">
                        <h4 class="text-2xl font-bold text-red-700 mb-2">Orígenes con el Cuarteto Leo</h4>
                        <p class="text-neutral-700">El cuarteto nace en Córdoba con el Cuarteto Leo, liderado por Leonor Marzano y Augusto Marzano. Su instrumentación (piano, acordeón, bajo y violín) y ritmo "tunga-tunga" marcan el inicio de un género que definiría la identidad musical de Córdoba.</p>
                        <div class="timeline-dot"></div>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">1970s</div>
                    <div class="timeline-content">
                        <h4 class="text-2xl font-bold text-red-700 mb-2">La Revolución de "La Mona" Jiménez</h4>
                        <p class="text-neutral-700">Carlos "La Mona" Jiménez emerge como una figura icónica, llevando el cuarteto a nuevas alturas con su carisma, energía y estilo único. Consolida el género y lo populariza masivamente, trascendiendo las fronteras de Córdoba.</p>
                        <div class="timeline-dot"></div>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">1990s</div>
                    <div class="timeline-content">
                        <h4 class="text-2xl font-bold text-red-700 mb-2">La Era de Rodrigo y la Expansión Nacional</h4>
                        <p class="text-neutral-700">Rodrigo "El Potro" Bueno revoluciona el cuarteto con su estilo fresco y enérgico, llevando el género al estrellato nacional. Sus shows masivos y temas pegadizos lo convierten en un fenómeno cultural en toda Argentina.</p>
                        <div class="timeline-dot"></div>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-date">Actualidad</div>
                    <div class="timeline-content">
                        <h4 class="text-2xl font-bold text-red-700 mb-2">Fusión, Globalización y Redes</h4>
                        <p class="text-neutral-700">El cuarteto actual se fusiona con otros géneros musicales, incorpora elementos urbanos y se difunde globalmente a través de las redes sociales. Artistas como Ulises Bueno, La Banda XXI, Konga y Q' Lokura mantienen vivo el ritmo y lo adaptan a las nuevas generaciones.</p>
                        <div class="timeline-dot"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Photo Gallery Section -->
    <section id="gallery" class="py-16 bg-white shadow-inner">
        <div class="container mx-auto px-6 text-center">
            <h3 class="text-4xl font-extrabold mb-12 section-title mx-auto">Galería de Momentos</h3>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                <!-- Placeholder Images -->
                <div class="rounded-lg overflow-hidden shadow-xl transform hover:scale-105 transition duration-300 border-2 border-red-200">
                    <img src="https://placehold.co/400x300/EF4444/FFFFFF?text=Escuela+Bianco+1950" alt="Imagen de Escuela Bianco 1950" class="w-full h-48 object-cover">
                    <p class="p-4 text-neutral-700 font-semibold text-sm">Alumnos de la Escuela Bianco, década de 1950.</p>
                </div>
                <div class="rounded-lg overflow-hidden shadow-xl transform hover:scale-105 transition duration-300 border-2 border-red-200">
                    <img src="https://placehold.co/400x300/EF4444/FFFFFF?text=La+Mona+Jimenez" alt="Imagen de La Mona Jimenez" class="w-full h-48 object-cover">
                    <p class="p-4 text-neutral-700 font-semibold text-sm">"La Mona" Jiménez en vivo, un ícono del cuarteto.</p>
                </div>
                <div class="rounded-lg overflow-hidden shadow-xl transform hover:scale-105 transition duration-300 border-2 border-red-200">
                    <img src="https://placehold.co/400x300/EF4444/FFFFFF?text=Rodrigo+El+Potro" alt="Imagen de Rodrigo El Potro" class="w-full h-48 object-cover">
                    <p class="p-4 text-neutral-700 font-semibold text-sm">Rodrigo "El Potro" Bueno en uno de sus recordados conciertos.</p>
                </div>
                <div class="rounded-lg overflow-hidden shadow-xl transform hover:scale-105 transition duration-300 border-2 border-red-200">
                    <img src="https://placehold.co/400x300/EF4444/FFFFFF?text=Baile+de+Cuarteto" alt="Imagen de Baile de Cuarteto" class="w-full h-48 object-cover">
                    <p class="p-4 text-neutral-700 font-semibold text-sm">La pasión del baile de cuarteto en Villa María.</p>
                </div>
                <div class="rounded-lg overflow-hidden shadow-xl transform hover:scale-105 transition duration-300 border-2 border-red-200">
                    <img src="https://placehold.co/400x300/EF4444/FFFFFF?text=Antigua+Escuela" alt="Imagen de Antigua Escuela" class="w-full h-48 object-cover">
                    <p class="p-4 text-neutral-700 font-semibold text-sm">Vista de la antigua fachada de la Escuela Bianco.</p>
                </div>
                <div class="rounded-lg overflow-hidden shadow-xl transform hover:scale-105 transition duration-300 border-2 border-red-200">
                    <img src="https://placehold.co/400x300/EF4444/FFFFFF?text=Estudiantes+Bailando" alt="Imagen de Estudiantes Bailando" class="w-full h-48 object-cover">
                    <p class="p-4 text-neutral-700 font-semibold text-sm">Estudiantes de la Escuela Bianco ensayando para la gala.</p>
                </div>
                <div class="rounded-lg overflow-hidden shadow-xl transform hover:scale-105 transition duration-300 border-2 border-red-200">
                    <img src="https://placehold.co/400x300/EF4444/FFFFFF?text=Nuevo+Salon" alt="Imagen de Nuevo Salon" class="w-full h-48 object-cover">
                    <p class="p-4 text-neutral-700 font-semibold text-sm">El Nuevo Salón de los Deportes, sede de la gala.</p>
                </div>
                <div class="rounded-lg overflow-hidden shadow-xl transform hover:scale-105 transition duration-300 border-2 border-red-200">
                    <img src="https://placehold.co/400x300/EF4444/FFFFFF?text=Grupo+de+Cuarteto" alt="Imagen de Grupo de Cuarteto" class="w-full h-48 object-cover">
                    <p class="p-4 text-neutral-700 font-semibold text-sm">Un grupo de cuarteto contemporáneo en acción.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Interactive Section (AI integration concept) -->
    <section id="interactive" class="py-16 bg-gradient-to-br from-red-50 to-red-100">
        <div class="container mx-auto px-6 text-center">
            <h3 class="text-4xl font-extrabold mb-12 section-title mx-auto">Interactúa con la Comunidad Educativa</h3>

            <!-- Share Your Memory Section -->
            <div class="bg-white p-8 rounded-lg shadow-2xl mb-12 border-t-8 border-red-600">
                <h4 class="text-3xl font-bold text-red-700 mb-6 flex items-center justify-center"><i class="fas fa-comment-dots mr-3 text-red-500"></i> Comparte Tu Recuerdo</h4>
                <p class="text-lg mb-6 max-w-2xl mx-auto text-neutral-700">¿Tienes una anécdota especial sobre la Escuela Bianco o un recuerdo inolvidable relacionado con el cuarteto? ¡Compártelo con nosotros! Tus historias formarán parte de nuestro mural digital conmemorativo.</p>
                <textarea id="memoryInput" class="w-full max-w-xl h-32 p-4 border border-red-300 rounded-lg focus:outline-none focus:ring-4 focus:ring-red-200 mb-4 text-neutral-800 placeholder-neutral-500 transition-all duration-300" placeholder="Escribe tu recuerdo aquí..."></textarea>
                <button id="submitMemory" class="bg-red-700 hover:bg-red-800 text-white font-bold py-3 px-8 rounded-full shadow-lg transition duration-300 transform hover:scale-105 active:scale-95 inline-flex items-center group">
                    Enviar Recuerdo <i class="fas fa-paper-plane ml-2 group-hover:translate-x-1 transition-transform duration-300"></i>
                </button>
                <div id="memoryMessage" class="mt-4 text-lg font-semibold text-neutral-700"></div>
                <div id="memoriesDisplay" class="mt-8 grid grid-cols-1 md:grid-cols-2 gap-6">
                    <!-- Memories will be displayed here -->
                </div>
            </div>

            <!-- Cuarteto Quiz Section -->
            <div class="bg-white p-8 rounded-lg shadow-2xl border-t-8 border-red-600">
                <h4 class="text-3xl font-bold text-red-700 mb-6 flex items-center justify-center"><i class="fas fa-question-circle mr-3 text-red-500"></i> ¿Cuánto Sabes de Cuarteto? ¡Pon a Prueba tus Conocimientos!</h4>
                <div id="quizContainer" class="max-w-xl mx-auto text-left">
                    <div id="question" class="text-xl font-extrabold mb-4 text-neutral-800"></div>
                    <div id="options" class="flex flex-col space-y-3"></div>
                    <button id="nextQuestion" class="bg-red-700 hover:bg-red-800 text-white font-bold py-3 px-8 rounded-full shadow-lg transition duration-300 transform hover:scale-105 active:scale-95 mt-6 inline-flex items-center group">
                        Siguiente Pregunta <i class="fas fa-arrow-right ml-2 group-hover:translate-x-1 transition-transform duration-300"></i>
                    </button>
                    <div id="quizResult" class="mt-6 text-xl font-bold text-neutral-700"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer Section -->
    <footer class="bg-red-900 text-white py-8 mt-12">
        <div class="container mx-auto px-6 text-center">
            <p class="mb-4 text-red-100">&copy; 2025 Escuela Bianco. Todos los derechos reservados.</p>
            <div class="flex justify-center space-x-6">
                <a href="#" class="text-red-300 hover:text-white transition duration-300 transform hover:scale-110"><i class="fab fa-facebook-f text-2xl"></i></a>
                <a href="#" class="text-red-300 hover:text-white transition duration-300 transform hover:scale-110"><i class="fab fa-instagram text-2xl"></i></a>
                <a href="#" class="text-red-300 hover:text-white transition duration-300 transform hover:scale-110"><i class="fab fa-youtube text-2xl"></i></a>
            </div>
            <p class="mt-4 text-red-200 text-sm">Gala Aniversario: "88 Años de Escuela Bianco: El Cuarteto en la Ciudad"</p>
        </div>
    </footer>

    <!-- Success Modal -->
    <div id="successModal" class="modal">
        <div class="modal-content">
            <span class="close-button" onclick="closeModal('successModal')">&times;</span>
            <div class="text-center">
                <i class="fas fa-check-circle text-green-600 text-7xl mb-4 animate-bounce-in"></i>
                <h3 class="text-3xl font-extrabold text-neutral-800 mb-2">¡Recuerdo Enviado con Éxito!</h3>
                <p class="text-lg text-neutral-700">Gracias por compartir tu historia. ¡Tu recuerdo enriquece nuestra celebración!</p>
            </div>
        </div>
    </div>

    <!-- Error Modal -->
    <div id="errorModal" class="modal">
        <div class="modal-content">
            <span class="close-button" onclick="closeModal('errorModal')">&times;</span>
            <div class="text-center">
                <i class="fas fa-times-circle text-red-600 text-7xl mb-4 animate-shake"></i>
                <h3 class="text-3xl font-extrabold text-neutral-800 mb-2">¡Error al Enviar!</h3>
                <p class="text-lg text-neutral-700">No se pudo enviar tu recuerdo. Por favor, inténtalo de nuevo.</p>
            </div>
        </div>
    </div>

    <script>
        // Modal functions
        function openModal(modalId) {
            document.getElementById(modalId).style.display = "flex";
        }

        function closeModal(modalId) {
            document.getElementById(modalId).style.display = "none";
        }

        window.onclick = function(event) {
            const successModal = document.getElementById('successModal');
            const errorModal = document.getElementById('errorModal');
            if (event.target == successModal) {
                successModal.style.display = "none";
            }
            if (event.target == errorModal) {
                errorModal.style.display = "none";
            }
        }

        // Simulating Generative AI API call for memory submission
        document.getElementById('submitMemory').addEventListener('click', async () => {
            const memoryInput = document.getElementById('memoryInput');
            const memory = memoryInput.value.trim();
            const memoryMessage = document.getElementById('memoryMessage');
            const memoriesDisplay = document.getElementById('memoriesDisplay');

            if (memory) {
                memoryMessage.textContent = 'Enviando tu recuerdo...';
                try {
                    // Simulate API call to a generative AI
                    // In a real application, you would replace this with your actual Gemini API call
                    // For instance:
                    /*
                    let chatHistory = [];
                    chatHistory.push({ role: "user", parts: [{ text: `Generate a short, evocative summary (max 20 words) for this memory about Escuela Bianco or cuarteto: "${memory}"` }] });
                    const payload = { contents: chatHistory };
                    const apiKey = ""; // Canvas will provide this in runtime
                    const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${apiKey}`;
                    const response = await fetch(apiUrl, {
                                method: 'POST',
                                headers: { 'Content-Type': 'application/json' },
                                body: JSON.stringify(payload)
                            });
                    const result = await response.json();
                    let aiGeneratedSummary = memory; // Fallback to original memory
                    if (result.candidates && result.candidates.length > 0 &&
                        result.candidates[0].content && result.candidates[0].content.parts &&
                        result.candidates[0].content.parts.length > 0) {
                        aiGeneratedSummary = result.candidates[0].content.parts[0].text;
                    }
                    */

                    // For demonstration, we'll just use the original memory after a delay
                    await new Promise(resolve => setTimeout(resolve, 1500)); // Simulate network delay

                    const aiGeneratedSummary = memory; // Using original memory for demo purposes

                    // Display the memory
                    const memoryDiv = document.createElement('div');
                    memoryDiv.className = 'memory-box p-4 rounded-lg';
                    memoryDiv.innerHTML = `<p class="italic text-neutral-700">"${aiGeneratedSummary}"</p>`;
                    memoriesDisplay.prepend(memoryDiv); // Add to the top

                    memoryInput.value = ''; // Clear input
                    memoryMessage.textContent = '¡Recuerdo enviado! Desplázate para ver los recuerdos compartidos.';
                    openModal('successModal');

                } catch (error) {
                    console.error('Error submitting memory:', error);
                    memoryMessage.textContent = 'Error al enviar el recuerdo. Por favor, inténtalo de nuevo.';
                    openModal('errorModal');
                }
            } else {
                memoryMessage.textContent = 'Por favor, escribe tu recuerdo antes de enviarlo.';
            }
        });

        // Quiz Logic
        const quizQuestions = [
            {
                question: "¿Cuál fue el grupo que se considera el origen del cuarteto cordobés?",
                options: ["Chébere", "Cuarteto Leo", "La Mona Jiménez", "Tru-la-lá"],
                answer: "Cuarteto Leo"
            },
            {
                question: "¿Qué instrumentación es característica del cuarteto original?",
                options: ["Guitarra eléctrica, batería, bajo", "Piano, acordeón, bajo, violín", "Flauta, clarinete, percusión", "Saxo, trompeta, contrabajo"],
                answer: "Piano, acordeón, bajo, violín"
            },
            {
                question: "¿Qué artista es conocido como 'El Potro' del cuarteto?",
                options: ["Jean Carlos", "Ulises Bueno", "Rodrigo", "La Banda XXI"],
                answer: "Rodrigo"
            },
            {
                question: "¿Qué década marcó la consolidación de 'La Mona' Jiménez como ícono?",
                options: ["1950s", "1960s", "1970s", "1980s"],
                answer: "1970s"
            },
            {
                question: "¿Cómo se le conoce al ritmo característico del cuarteto?",
                options: ["Cumbia", "Salsa", "Tunga-tunga", "Chamamé"],
                answer: "Tunga-tunga"
            }
        ];

        let currentQuestionIndex = 0;
        let score = 0;

        const questionEl = document.getElementById('question');
        const optionsEl = document.getElementById('options');
        const nextQuestionBtn = document.getElementById('nextQuestion');
        const quizResultEl = document.getElementById('quizResult');

        function loadQuestion() {
            if (currentQuestionIndex < quizQuestions.length) {
                const q = quizQuestions[currentQuestionIndex];
                questionEl.textContent = q.question;
                optionsEl.innerHTML = '';
                q.options.forEach(option => {
                    const button = document.createElement('button');
                    button.textContent = option;
                    button.className = 'bg-gray-200 hover:bg-red-300 text-neutral-800 font-semibold py-3 px-5 rounded-lg transition duration-200 text-lg shadow-sm hover:shadow-md';
                    button.onclick = () => selectAnswer(option, q.answer);
                    optionsEl.appendChild(button);
                });
                nextQuestionBtn.style.display = 'none'; // Hide next button until answer is selected
                quizResultEl.textContent = ''; // Clear result
            } else {
                showQuizResult();
            }
        }

        function selectAnswer(selectedOption, correctAnswer) {
            // Disable all options after selection
            Array.from(optionsEl.children).forEach(button => {
                button.disabled = true;
                if (button.textContent === correctAnswer) {
                    button.classList.remove('bg-gray-200', 'hover:bg-red-300');
                    button.classList.add('bg-green-600', 'text-white', 'shadow-lg');
                } else if (button.textContent === selectedOption) {
                    button.classList.remove('bg-gray-200', 'hover:bg-red-300');
                    button.classList.add('bg-red-600', 'text-white', 'shadow-lg');
                }
            });

            if (selectedOption === correctAnswer) {
                score++;
                quizResultEl.textContent = '¡Correcto!';
                quizResultEl.classList.remove('text-red-500');
                quizResultEl.classList.add('text-green-600');
            } else {
                quizResultEl.textContent = `Incorrecto. La respuesta correcta era: ${correctAnswer}`;
                quizResultEl.classList.remove('text-green-500');
                quizResultEl.classList.add('text-red-600');
            }

            nextQuestionBtn.style.display = 'inline-flex'; // Show next button
        }

        function showQuizResult() {
            questionEl.textContent = `¡Cuestionario Completado!`;
            optionsEl.innerHTML = '';
            quizResultEl.textContent = `Obtuviste ${score} de ${quizQuestions.length} respuestas correctas.`;
            quizResultEl.classList.remove('text-green-600', 'text-red-600');
            quizResultEl.classList.add('text-blue-700');
            nextQuestionBtn.textContent = 'Reiniciar Cuestionario';
            nextQuestionBtn.onclick = resetQuiz;
            nextQuestionBtn.style.display = 'inline-flex';
        }

        function resetQuiz() {
            currentQuestionIndex = 0;
            score = 0;
            nextQuestionBtn.textContent = 'Siguiente Pregunta';
            nextQuestionBtn.onclick = () => {
                currentQuestionIndex++;
                loadQuestion();
            };
            loadQuestion();
        }

        // Initialize quiz on page load
        document.addEventListener('DOMContentLoaded', loadQuestion);
    </script>
</body>
</html>
