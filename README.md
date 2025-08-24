<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy 20th Birthday, My Love - Natural Image Fit</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&family=Pacifico&display=swap');
        
        :root {
            --primary-pink: #ffd1dc;
            --secondary-pink: #f8c3cd;
            --accent-lavender: #e6e6fa;
            --accent-champagne: #f7e7ce;
            --text-dark: #aa336a;
            --bg-dark-gray: #4a5568;
            --bg-medium-gray: #718096;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--bg-dark-gray);
            color: var(--text-dark);
            overflow-x: hidden;
            margin: 0;
            padding: 0;
        }
        
        .hero-title {
            font-family: 'Pacifico', cursive;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .nav-link {
            transition: all 0.3s ease;
            border-bottom: 2px solid transparent;
        }
        
        .nav-link:hover {
            color: var(--text-dark);
            border-bottom-color: var(--text-dark);
        }
        
        .heart {
            position: absolute;
            pointer-events: none;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }
        
        .photo-frame {
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            border: 8px solid white;
            transform: rotate(-2deg);
            display: inline-block;
            width: 100%;
            background: #fdf2f8;
            border-radius: 0.75rem;
            overflow: hidden;
        }
        
        .photo-frame:hover {
            transform: scale(1.05) rotate(0deg);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        /* Natural image container - no fixed aspect ratio */
        .memory-image-container {
            width: 100%;
            overflow: hidden;
            border-radius: 0.5rem;
            position: relative;
            background: #f3f4f6;
        }
        
        .memory-image {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.3s ease;
            border-radius: 0.5rem;
        }
        
        .photo-frame:hover .memory-image {
            transform: scale(1.1);
        }
        
        /* Content area styling */
        .memory-content {
            padding: 16px;
        }
        
        .memory-content h3 {
            margin-bottom: 8px;
            font-size: 1.25rem;
            font-weight: 600;
            color: var(--text-dark);
        }
        
        .memory-content p {
            margin-bottom: 16px;
            color: #6b7280;
            line-height: 1.5;
        }
        
        .memory-date {
            display: flex;
            justify-content: flex-end;
        }
        
        .memory-date span {
            font-size: 0.75rem;
            color: #f9a8d4;
        }
        
        .message-box {
            background: linear-gradient(135deg, #ffffff 0%, #fff9fb 100%);
            border-radius: 20px;
            box-shadow: 0 8px 20px rgba(170, 51, 106, 0.1);
            transition: all 0.3s ease;
        }
        
        .message-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(170, 51, 106, 0.15);
        }
        
        .btn-primary {
            background: linear-gradient(135deg, var(--primary-pink) 0%, var(--secondary-pink) 100%);
            transition: all 0.3s ease;
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(170, 51, 106, 0.2);
        }
        
        .floating {
            animation: floating 3s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        .countdown-box {
            background: white;
            border-radius: 15px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            padding: 20px;
            text-align: center;
            min-width: 80px;
        }
        
        .countdown-number {
            font-size: 2rem;
            font-weight: bold;
            color: var(--text-dark);
        }
        
        .countdown-label {
            font-size: 0.875rem;
            color: #666;
            margin-top: 5px;
        }
        
        /* Fancy message box */
        .special-message-box {
            background: linear-gradient(135deg, #fff0f5 0%, #ffeef4 100%);
            border-radius: 20px;
            border: 3px solid var(--accent-champagne);
            box-shadow: 0 15px 30px rgba(170, 51, 106, 0.1);
            padding: 30px;
            position: relative;
            overflow: hidden;
        }
        
        .special-message-box::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-pink), var(--secondary-pink), var(--accent-lavender));
        }

        /* Natural grid layout - auto-fit based on content */
        .memories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            align-items: start;
        }

        /* Section background overrides */
        .memories-section {
            background-color: var(--bg-dark-gray) !important;
        }
        
        .countdown-section {
            background-color: var(--bg-dark-gray) !important;
        }
        
        .memories-section h2,
        .countdown-section h2,
        .countdown-section p {
            color: white !important;
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .hero-title {
                font-size: 2.5rem !important;
            }
            
            .section-title {
                font-size: 1.8rem !important;
            }
            
            .memories-grid {
                grid-template-columns: 1fr;
                gap: 1.5rem;
            }
            
            .photo-frame {
                transform: rotate(-1deg);
            }
        }
        
        @media (max-width: 640px) {
            .memories-grid {
                gap: 1rem;
            }
            
            .photo-frame {
                transform: rotate(0deg);
            }
        }
    </style>
</head>
<body class="relative">
    <!-- Floating hearts background -->
    <div id="hearts-container"></div>
    
    <!-- Navigation -->
    <nav class="bg-white bg-opacity-90 backdrop-filter backdrop-blur-lg w-full shadow-md">
        <div class="container mx-auto px-6 py-3">
            <div class="flex justify-between items-center">
                <div class="text-2xl font-bold" style="color: var(--text-dark);">Happy 20th Brigitta Cecelia (Bakpao)</div>
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="nav-link">Home</a>
                    <a href="#memories" class="nav-link">Unconditional love</a>
                    <a href="#wishes" class="nav-link">My Wishes</a>
                </div>
                <button class="md:hidden focus:outline-none">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>
        </div>
    </nav>
    
    <!-- Home Section -->
    <section id="home" class="min-h-screen flex items-center justify-center px-4" style="background: linear-gradient(135deg, var(--primary-pink) 0%, var(--accent-lavender) 100%);">
        <div class="container mx-auto flex flex-col md:flex-row items-center justify-between">
            <div class="md:w-1/2 mb-12 md:mb-0 px-4">
                <h1 class="hero-title text-5xl md:text-6xl mb-6" style="color: var(--text-dark);">Happy <span class="text-6xl md:text-7xl" style="color: #d23c67;">20th</span> Birthday!</h1>
                <p class="text-lg mb-8">To the most amazing person in my life, may your special day be as wonderful as you are.</p>
                <button class="btn-primary text-white px-8 py-3 rounded-full font-semibold">Discover More</button>
            </div>
            <div class="md:w-1/2 relative">
                <img src="asset/sayangg.jpg">
                <div class="absolute -bottom-6 -right-6 bg-white p-4 rounded-full shadow-lg">
                    <div class="bg-pink-200 w-20 h-20 rounded-full flex items-center justify-center">
                        <span class="text-3xl" style="color: var(--text-dark);">20</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Memories Section -->
    <section id="memories" class="py-20 px-4 memories-section">
        <div class="container mx-auto">
            <h2 class="section-title text-3xl md:text-4xl font-bold text-center mb-16" style="color: white;">The Most Thing I Loved</h2>
            
            <div class="memories-grid mb-12">
                <!-- Memory 1 -->
                <div class="photo-frame">
                    <div class="memory-image-container">
                        <img src="asset/peluk.jpg" class="memory-image" alt="U Heal Me">
                    </div>
                    <div class="memory-content">
                        <h3>When U Heal Me</h3>
                        <p>Selalu jadi tempat pulang buat aku dan yang terbaik</p>
                        <div class="memory-date">
                            <span></span>
                        </div>
                    </div>
                </div>
                
                <!-- Memory 2 -->
                <div class="photo-frame">
                    <div class="memory-image-container">
                        <img src="asset/belajarr.jpg" class="memory-image" alt="Beach Sunset">
                    </div>
                    <div class="memory-content">
                        <h3>Ambitious Soul</h3>
                        <p>Aku suka banget lihat kamu serius belajar. Ambisimu bikin aku kagum, dan tiap nilai bagus yang kamu dapat itu bukti kalau kerja kerasmu nggak sia-sia. Semangat terus ya sayang.</p>
                        <div class="memory-date">
                            <span></span>
                        </div>
                    </div>
                </div>
                
                <!-- Memory 3 -->
                <div class="photo-frame">
                    <div class="memory-image-container">
                        <img src="asset/yapping.jpg" class="memory-image" alt="1st Anniversary">
                    </div>
                    <div class="memory-content">
                        <h3>Queen Yapping</h3>
                        <p>Aku selalu ketawa sendiri kalau kamu mulai yapping. Kadang ceritanya ngawur absurd dan kadang punya pemikiran out of the box, tapi justru itu yang bikin aku betah dengerin kamu terus. Aku suka caramu cerita, karena dari situ aku bisa lihat betapa hidupnya kamu. Jangan pernah berhenti yapping ya, soalnya itu bagian favoritku dari kamu.</p>
                        <div class="memory-date">
                            <span></span>
                        </div>
                    </div>
                </div>
                
                
                <!-- Memory 5 -->
                <div class="photo-frame">
                    <div class="memory-image-container">
                        <img src="asset/ngantuk.jpg" class="memory-image" alt="Movie Nights">
                    </div>
                    <div class="memory-content">
                        <h3>"Belum Ngantuk Seng"</h3>
                        <p>Ngeliat kamu ngantuk tuh lucu banget, apalagi pas lagi asik ngobrol tiba-tiba diam… eh ternyata udah ketiduran.padahal 5 menit yang lalu blg "blom ngantuk seng</p>
                        <div class="memory-date">
                            <span></span>
                        </div>
                    </div>
                </div>

                <!-- Memory 4 -->
                <div class="photo-frame">
                    <div class="memory-image-container">
                        <img src="asset/hadiah.jpg" class="memory-image" alt="Date Night">
                    </div>
                    <div class="memory-content">
                        <h3>Efforts And Creative</h3>
                        <p>Aku sadar kalau nggak semua orang bisa se-niat kamu. Kreativitas dan usaha kamu itu bikin aku ngerasa istimewa, dan aku nggak akan pernah anggap itu hal kecil</p>
                        <div class="memory-date">
                            <span></span>
                        </div>
                    </div>
                </div>
                
                <!-- Memory 6 -->
                <div class="photo-frame">
                    <div class="memory-image-container">
                        <img src="asset/cantik.jpg">
                    </div>
                    <div class="memory-content">
                        <h3>Above all, because you're the one.</h3>
                        <p>No matter what happens, no matter how complicated things get, at the end of it all, the reason I choose, the reason I stay, is because you're the one.</p>
                        <div class="memory-date">
                            <span></span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Wishes Section -->
    <section id="wishes" class="py-20 px-4" style="background: linear-gradient(135deg, var(--accent-lavender) 0%, var(--accent-champagne) 100%);">
        <div class="container mx-auto">
            <h2 class="section-title text-3xl md:text-4xl font-bold text-center mb-16" style="color: var(--text-dark);">My Heartfelt Wishes for You</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Wish 1 -->
                <div class="message-box p-8">
                    <div class="flex items-center mb-6">
                        <div class="bg-pink-200 w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <span class="text-xl">💖</span>
                        </div>
                        <h3 class="text-xl font-semibold">Happiness</h3>
                    </div>
                    <p class="text-gray-700">Aku cuma ingin kamu terus punya alasan untuk tersenyum, sekecil apa pun itu.
Kamu pantas untuk bahagia, bahkan di hari-hari biasa.
Kalau kamu butuh tempat untuk istirahat sejenak dari dunia, aku selalu ada.
Semoga aku bisa tetap jadi bagian dari ketenangan dan senyummu.

</p>
                </div>
                
                <!-- Wish 2 -->
                <div class="message-box p-8">
                    <div class="flex items-center mb-6">
                        <div class="bg-pink-200 w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <span class="text-xl">🌟</span>
                        </div>
                        <h3 class="text-xl font-semibold">Success</h3>
                    </div>
                    <p class="text-gray-700">Aku tahu kamu kerja keras dan nggak selalu cerita semuanya.
Tapi aku lihat usahamu, dan aku bangga.
Nggak apa-apa jalanmu pelan, yang penting tetap maju.
Aku akan tetap di sini, ngedukung kamu dengan cara paling sederhana yang aku bisa.</p>
                </div>
                
                <!-- Wish 3 -->
                <div class="message-box p-8">
                    <div class="flex items-center mb-6">
                        <div class="bg-pink-200 w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <span class="text-xl">🌷</span>
                        </div>
                        <h3 class="text-xl font-semibold">Love</h3>
                    </div>
                    <p class="text-gray-700">Mungkin caramu nunjukin cinta agak unik kadang gengsimu setinggi langit,
marahnya keliatan cuek, tapi aku tahu di balik itu kamu actually care banget.
Setiap kali kita ribut, kamu kesel sendiri, mikir sendiri, dan akhirnya… ya, mellow sendiri.
Lucu sih, tapi justru dari situ aku tahu your love is real, your love is purely genuine semoga,kamu selalu begini dan akan tetap begini, love u </p>
                </div>
                
                <!-- Wish 4 -->
                <div class="message-box p-8">
                    <div class="flex items-center mb-6">
                        <div class="bg-pink-200 w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <span class="text-xl">🌎</span>
                        </div>
                        <h3 class="text-xl font-semibold">Adventure</h3>
                    </div>
                    <p class="text-gray-700">Kamu hebat, Seng… atau lebih tepatnya, my partner in life aku tahu caramu bertahan selama ini, dan itu bukan hal yang mudah, bahkan cukup menegangkan.
Dari luar kamu tampak bercahaya, berapi-api, tapi bersamaku semuanya terbalik dan terasa lebih tenang dan jujur, aku suka sisi itu.
Aku suka caramu berkembang, berpikir, mencari solusi, dan aku percaya kamu punya potensi besar untuk mencapai tempat yang selama ini kamu tuju.
I'm totally proud of you keep going, karena apa pun yang terjadi, aku akan selalu ada di sampingmu.</p>
                </div>
            </div>
            
            <div class="mt-16 text-center">
                <div class="max-w-3xl mx-auto">
                    <h3 class="text-2xl font-semibold mb-6" style="color: var(--text-dark);">A Special Message Just For You</h3>
                    <div class="special-message-box">
                        <div class="text-center mb-6">
                            <span class="text-4xl">💌</span>
                        </div>
                        <p class="text-lg leading-relaxed italic text-gray-700">
                            "Happy birthday, Bakpao I know this year has been really heavy for you, with so many things testing your heart and mind. But I want you to always remember you're never alone in any of it. I'm here, always, to listen, to stay by your side, and to be the place you can come home to when everything feels overwhelming.

On your birthday, I hope you feel how deeply loved and cherished you are. No matter how tough things get, you're safe with me. I'll hold your hand through it all, and we'll face whatever comes together. May this new year of your life bring you more peace, warmth, and the happiness you truly deserve.


别难过啦，二十岁才刚刚开始，你还有好多冒险要去经历。想想看，以后的你会笑着说：'哇，原来二十岁那年我那么坚强！"
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Countdown Section -->
    <section id="countdown" class="py-20 px-4 countdown-section">
        <div class="container mx-auto text-center">
            <h2 class="section-title text-3xl md:text-4xl font-bold mb-6" style="color: white;">Birthday Countdown</h2>
            <p class="text-lg mb-12" style="color: white;">Until we celebrate together!</p>
            
            <div class="flex justify-center space-x-4 md:space-x-8 mb-12">
                <div class="countdown-box">
                    <div class="countdown-number" id="days">00</div>
                    <div class="countdown-label">Days</div>
                </div>
                <div class="countdown-box">
                    <div class="countdown-number" id="hours">00</div>
                    <div class="countdown-label">Hours</div>
                </div>
                <div class="countdown-box">
                    <div class="countdown-number" id="minutes">00</div>
                    <div class="countdown-label">Minutes</div>
                </div>
                <div class="countdown-box">
                    <div class="countdown-number" id="seconds">00</div>
                    <div class="countdown-label">Seconds</div>
                </div>
            </div>
            
            <div class="max-w-2xl mx-auto bg-pink-50 rounded-xl p-8">
                <h3 class="text-2xl font-semibold mb-4" style="color: var(--text-dark);">Get Ready, Our Journey is still to long!</h3>
                <p class="mb-6">Before we start let me know what would make your birthday extra special.</p>
                
                <form id="birthdayForm" class="space-y-4 text-left">
                    <div>

                    
                    <div>
                        <label class="block text-gray-700 mb-2">Special Birthday Wish</label>
                        <textarea id="birthdayWish" class="w-full px-4 py-2 rounded-lg border border-pink-200 focus:outline-none focus:ring-2 focus:ring-pink-300" rows="3" placeholder="What would make your day perfect?"></textarea>
                
                    <button type="submit" class="btn-primary text-white px-8 py-3 rounded-full font-semibold">Send</button>

        </div>

    <!-- Footer -->
    <footer class="py-12 px-4" style="background-color: var(--text-dark); color: white;">
        <div class="container mx-auto">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <h3 class="text-2xl font-bold mb-2">Happy 20th Birthday</h3>
                    <p class="opacity-80">For the most special person in my life</p>
                </div>
                
                <div class="flex space-x-6">
                    <a href="#" class="hover:text-pink-200 transition duration-300">
                        <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                        </svg>
                    </a>
                    <a href="#" class="hover:text-pink-200 transition duration-300">
                        <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z"/>
                        </svg>
                    </a>
                    <a href="#" class="hover:text-pink-200 transition duration-300">
                        <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4
