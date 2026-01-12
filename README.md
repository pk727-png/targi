<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	
<style>
        /* ===== RESETOWANIE STYLÓW ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* ===== GŁÓWNE STYLE STRONY ===== */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
        }
        /* ===== SEKCJA NAGŁÓWKA (HERO) ===== */
        /* To jest główna sekcja na górze strony z najważniejszymi informacjami */
        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); /* Zmień kolory gradientu tutaj */
            color: white;
            text-align: center;
            padding: 100px 20px;
            min-height: 500px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        .hero h1 {
            font-size: 3rem; /* Rozmiar głównego tytułu */
            margin-bottom: 20px;
            font-weight: 700;
        }
        .hero .subtitle {
            font-size: 1.5rem; /* Rozmiar podtytułu */
            margin-bottom: 30px;
            opacity: 0.95;
        }
        .hero .event-details {
            font-size: 1.2rem;
            margin-bottom: 40px;
        }
        .hero .event-details span {
            margin: 0 15px;
            display: inline-block;
        }
        /* ===== PRZYCISKI ===== */
        .btn {
            display: inline-block;
            padding: 15px 40px;
            background-color: #ff6b6b; /* Kolor przycisku - zmień tutaj */
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            transition: transform 0.3s, box-shadow 0.3s;
            border: none;
            cursor: pointer;
        }
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }
        /* ===== KONTENER (ogranicza szerokość treści) ===== */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        /* ==== SEKCJA O WYDARZENIU ===== */
        .about-section {
            padding: 80px 20px;
            background-color: #f8f9fa; /* Jasnoszare tło */
        }
        .about-section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            color: #333;
        }
        .about-content {
            max-width: 800px;
            margin: 0 auto;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        /* ===== SEKCJA Z KORZYŚCIAMI/CECHAMI ===== */
        .features-section {
            padding: 80px 20px;
            background-color: white;
        }
        .features-section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 60px;
            color: #333;
        }
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Automatyczne dostosowanie kolumn */
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .feature-card {
            text-align: center;
            padding: 30px;
            border-radius: 10px;
            transition: transform 0.3s;
        }
        .feature-card:hover {
            transform: translateY(-10px);
        }
        .feature-icon {
            font-size: 3rem; /* Rozmiar ikony (emoji) */
            margin-bottom: 20px;
        }
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #667eea;
        }
        .feature-card p {
            font-size: 1rem;
            color: #666;
            line-height: 1.6;
        }
        /* ===== SEKCJA HARMONOGRAMU ===== */
        .schedule-section {
            padding: 80px 20px;
            background-color: #f8f9fa;
        }
        .schedule-section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 60px;
            color: #333;
        }
        .schedule-timeline {
            max-width: 800px;
            margin: 0 auto;
        }
        .schedule-item {
            background: white;
            padding: 25px;
            margin-bottom: 20px;
            border-radius: 10px;
            border-left: 5px solid #667eea;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .schedule-time {
            font-weight: 700;
            color: #667eea;
            font-size: 1.2rem;
            margin-bottom: 10px;
        }
        .schedule-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 10px;
        }
        .schedule-description {
            color: #666;
            font-size: 1rem;
        }
        /* ===== SEKCJA LOKALIZACJI ===== */
        .location-section {
            padding: 80px 20px;
            background-color: white;
        }
        .location-section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 40px;
            color: #333;
        }
        .location-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }
        .location-details {
            font-size: 1.2rem;
            margin-bottom: 30px;
            line-height: 1.8;
        }
        /* Jeśli chcesz dodać mapę Google Maps, użyj tego kontenera */
        .map-container {
            width: 100%;
            height: 400px;
            margin-top: 30px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }
        /* ===== SEKCJA REJESTRACJI (CTA) ===== */
        .cta-section {
            padding: 100px 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }
        .cta-section h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        .cta-section p {
            font-size: 1.2rem;
            margin-bottom: 40px;
            opacity: 0.95;
        }
        /* ===== FORMULARZ REJESTRACJI ===== */
        .registration-form {
            max-width: 500px;
            margin: 0 auto;
            background: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
        }
        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: #333;
            font-weight: 600;
        }
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 2px solid #e0e0e0;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #667eea;
        }
        .form-group textarea {
            resize: vertical;
            min-height: 100px;
        }
        /* ===== STOPKA ===== */
        .footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 40px 20px;
        }
        .footer p {
            margin-bottom: 15px;
        }
        .footer a {
            color: #667eea;
            text-decoration: none;
        }
        .footer a:hover {
            text-decoration: underline;
        }
        /* ===== RESPONSYWNOŚĆ (wygląd na telefonach) ===== */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            .hero .subtitle {
                font-size: 1.2rem;
            }
            .hero .event-details {
                font-size: 1rem;
            }
            .hero .event-details span {
                display: block;
                margin: 10px 0;
            }
            .about-section h2,
            .features-section h2,
            .schedule-section h2,
            .location-section h2,
            .cta-section h2 {
                font-size: 2rem;
            }
            .features-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- ===== SEKCJA HERO (GŁÓWNA) ===== -->
    <!-- Tutaj zmień: tytuł, podtytuł, datę, godzinę i lokalizację -->
    <section class="hero">
        <div class="container">
            <h1>Konferencja Technologii 2026</h1>
            <!-- ↑ Zmień nazwę swojego wydarzenia tutaj -->
            <p class="subtitle">Poznaj najnowsze trendy w świecie technologii</p>
            <!-- ↑ Zmień opis wydarzenia tutaj -->
            <div class="event-details">
                <span>📅 15 marca 2026</span>
                <!-- ↑ Zmień datę tutaj -->
                <span>🕐 10:00 - 18:00</span>
                <!-- ↑ Zmień godzinę tutaj -->
                <span>📍 Warszawa, Centrum Konferencyjne</span>
                <!-- ↑ Zmień lokalizację tutaj -->
            </div>
            <a href="#register" class="btn">Zarejestruj się teraz</a>
            <!-- ↑ Ten przycisk przewija stronę do formularza rejestracji -->
        </div>
    </section>
    <!-- ===== SEKCJA O WYDARZENIU ===== -->
    <!-- Tutaj opisz szczegółowo swoje wydarzenie -->
    <section class="about-section">
        <div class="container">
            <h2>O Wydarzeniu</h2>
            <div class="about-content">
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor 
                    incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud 
                    exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                </p>
                <!-- ↑ Zmień ten tekst na opis swojego wydarzenia -->
                <p style="margin-top: 20px;">
                    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu 
                    fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in 
                    culpa qui officia deserunt mollit anim id est laborum.
                </p>
                <!-- ↑ Możesz dodać więcej akapitów według potrzeb -->
            </div>
        </div>
    </section>
    <!-- ===== SEKCJA KORZYŚCI/FUNKCJI ===== -->
    <!-- Tutaj wymień 3 główne korzyści lub cechy wydarzenia -->
    <section class="features-section">
        <div class="container">
            <h2>Dlaczego warto wziąć udział?</h2>
            <div class="features-grid">
                <!-- KARTA 1 -->
                <div class="feature-card">
                    <div class="feature-icon">🎤</div>
                    <!-- ↑ Zmień emoji na odpowiednią ikonę -->
                    <h3>Inspirujący prelegenci</h3>
                    <!-- ↑ Zmień tytuł korzyści -->
                    <p>Posłuchaj ekspertów branżowych, którzy podzielą się swoją wiedzą i doświadczeniem z pierwszej ręki.</p>
                    <!-- ↑ Zmień opis korzyści -->
                </div>
                <!-- KARTA 2 -->
                <div class="feature-card">
                    <div class="feature-icon">🤝</div>
                    <h3>Networking</h3>
                    <p>Poznaj innych uczestników, nawiąż cenne kontakty biznesowe i rozwijaj swoją sieć zawodową.</p>
                </div>
                <!-- KARTA 3 -->
                <div class="feature-card">
                    <div class="feature-icon">💡</div>
                    <h3>Praktyczna wiedza</h3>
                    <p>Zdobądź konkretne narzędzia i strategie, które możesz wdrożyć natychmiast po wydarzeniu.</p>
                </div>
                <!-- Możesz dodać więcej kart kopiując strukturę powyżej -->
            </div>
        </div>
    </section>
    <!-- ===== SEKCJA HARMONOGRAMU ===== -->
    <!-- Tutaj umieść plan wydarzenia z godzinami -->
    <section class="schedule-section">
        <div class="container">
            <h2>Harmonogram</h2>
            <div class="schedule-timeline">
                <!-- POZYCJA HARMONOGRAMU 1 -->
                <div class="schedule-item">
                    <div class="schedule-time">10:00 - 10:30</div>
                    <!-- ↑ Zmień godzinę -->
                    <div class="schedule-title">Rejestracja i powitalna kawa</div>
                    <!-- ↑ Zmień tytuł aktywności -->
                    <div class="schedule-description">
                        Odbiór pakietów uczestnika, networking przy porannej kawie
                    </div>
                    <!-- ↑ Zmień opis aktywności -->
                </div>
                <!-- POZYCJA HARMONOGRAMU 2 -->
                <div class="schedule-item">
                    <div class="schedule-time">10:30 - 12:00</div>
                    <div class="schedule-title">Keynote: Przyszłość technologii</div>
                    <div class="schedule-description">
                        Główne wystąpienie od eksperta branżowego o trendach technologicznych na najbliższe lata
                    </div>
                </div>
                <!-- POZYCJA HARMONOGRAMU 3 -->
                <div class="schedule-item">
                    <div class="schedule-time">12:00 - 13:00</div>
                    <div class="schedule-title">Przerwa obiadowa</div>
                    <div class="schedule-description">
                        Lunch i swobodny networking
                    </div>
                </div>
                <!-- POZYCJA HARMONOGRAMU 4 -->
                <div class="schedule-item">
                    <div class="schedule-time">13:00 - 15:00</div>
                    <div class="schedule-title">Warsztaty praktyczne</div>
                    <div class="schedule-description">
                        Hands-on sesje w małych grupach - wybierz warsztat, który Cię interesuje
                    </div>
                </div>
                <!-- POZYCJA HARMONOGRAMU 5 -->
                <div class="schedule-item">
                    <div class="schedule-time">15:00 - 18:00</div>
                    <div class="schedule-title">Panel dyskusyjny i Q&A</div>
                    <div class="schedule-description">
                        Dyskusja z ekspertami, pytania od publiczności i podsumowanie
                    </div>
                </div>
                <!-- Dodaj więcej pozycji kopiując strukturę powyżej -->
            </div>
        </div>
    </section>
    <!-- ===== SEKCJA LOKALIZACJI ===== -->
    <!-- Tutaj podaj szczegóły dotyczące miejsca wydarzenia -->
    <section class="location-section">
        <div class="container">
            <h2>Lokalizacja</h2>
            <div class="location-content">
                <div class="location-details">
                    <strong>Centrum Konferencyjne "Nowa Era"</strong><br>
                    <!-- ↑ Zmień nazwę miejsca -->
                    ul. Przykładowa 123<br>
                    00-001 Warszawa<br>
                    Polska
                    <!-- ↑ Zmień adres -->
                </div>
                <p>Dogodna lokalizacja w centrum miasta, 5 minut spacerem od stacji metra.</p>
                <!-- ↑ Zmień dodatkowe informacje o lokalizacji -->
                <!-- OPCJONALNIE: Dodaj Google Maps -->
                <!-- Odkomentuj poniższy kod i wklej swój link z Google Maps -->
                <!--
                <div class="map-container">
                    <iframe 
                        src="TUTAJ_WKLEJ_LINK_DO_GOOGLE_MAPS"
                        width="100%" 
                        height="400" 
                        style="border:0;" 
                        allowfullscreen="" 
                        loading="lazy">
                    </iframe>
                </div>
                -->
                <!-- Jak uzyskać link do Google Maps:
                     1. Wejdź na maps.google.com
                     2. Znajdź swoją lokalizację
                     3. Kliknij "Udostępnij" -> "Osadź mapę"
                     4. Skopiuj link z iframe src="" i wklej powyżej
                -->
            </div>
        </div>
    </section>
    <!-- ===== SEKCJA REJESTRACJI (CTA) ===== -->
    <!-- Tutaj znajduje się formularz rejestracyjny -->
    <section class="cta-section" id="register">
        <div class="container">
            <h2>Zarejestruj się już dziś!</h2>
            <p>Liczba miejsc ograniczona. Nie przegap tej wyjątkowej okazji!</p>
            <!-- ↑ Zmień zachętę do rejestracji -->
            <!-- FORMULARZ REJESTRACJI -->
            <form class="registration-form" action="#" method="POST">
                <!-- ↑ WAŻNE: Zmień action="#" na adres swojego skryptu do obsługi formularza
                     Możesz użyć usług takich jak Formspree.io, Google Forms, lub własnego backendu --> 
                <div class="form-group">
                    <label for="name">Imię i nazwisko *</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Adres e-mail *</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="phone">Numer telefonu</label>
                    <input type="tel" id="phone" name="phone">
                </div>
                <div class="form-group">
                    <label for="company">Firma/Organizacja</label>
                    <input type="text" id="company" name="company">
                </div>
                <div class="form-group">
                    <label for="message">Dodatkowe informacje</label>
                    <textarea id="message" name="message" placeholder="Czy masz jakieś pytania lub specjalne wymagania?"></textarea>
                </div>
                <button type="submit" class="btn">Wyślij rejestrację</button>
            </form>
        </div>
    </section>
    <!-- ===== STOPKA ===== -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2026 Nazwa Twojej Organizacji. Wszelkie prawa zastrzeżone.</p>
            <!-- ↑ Zmień nazwę organizacji i rok -->
            <p>
                Kontakt: <a href="mailto:kontakt@example.com">kontakt@example.com</a> | 
                Tel: +48 123 456 789
            </p>
            <!-- ↑ Zmień dane kontaktowe -->
            <p>
                <a href="#">Polityka prywatności</a> | 
                <a href="#">Regulamin</a>
            </p>
            <!-- ↑ Możesz dodać linki do dodatkowych stron -->
        </div>
		</footer>
    <!-- ===== SKRYPT DO PŁYNNEGO PRZEWIJANIA ===== -->
    <script>
        // Ten skrypt sprawia, że kliknięcie w przycisk "Zarejestruj się" 
        // płynnie przewija stronę do formularza
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
        // OPCJONALNIE: Obsługa formularza
        // Możesz tutaj dodać kod JavaScript do walidacji lub wysyłania formularza
        document.querySelector('.registration-form').addEventListener('submit', function(e) {
            // e.preventDefault(); // Odkomentuj jeśli chcesz obsługiwać formularz przez JavaScript  
            // Tutaj możesz dodać własną logikę, np.:
            // - Walidację pól
            // - Wysyłanie danych przez AJAX
            // - Integrację z zewnętrznymi usługami
            // Przykład prostego alertu po wysłaniu:
            // alert('Dziękujemy za rejestrację!');
        });
    </script>
</head>
</html>
