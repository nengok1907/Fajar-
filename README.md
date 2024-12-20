<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil Keren</title>
    <style>
        /* Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #1e3c72, #2a5298);
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .profile-container {
            max-width: 800px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.4);
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 20px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .profile-container:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.6);
        }

        /* Kolom Kiri: Foto Profil */
        .profile-image {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .profile-image img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 5px solid #fff;
            transition: transform 0.3s ease;
        }

        .profile-image img:hover {
            transform: scale(1.1);
        }

        /* Kolom Kanan: Info Profil */
        .profile-info {
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .profile-info h1 {
            font-size: 2em;
            margin-bottom: 10px;
        }

        .profile-info .subtitle {
            font-size: 1.2em;
            color: #ddd;
            margin-bottom: 20px;
        }

        .profile-info p {
            font-size: 1em;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        /* Progress Bar untuk Skill */
        .skills {
            margin-top: 20px;
        }

        .skill {
            margin-bottom: 15px;
        }

        .skill-name {
            font-size: 0.9em;
            margin-bottom: 5px;
        }

        .progress {
            background: #333;
            border-radius: 20px;
            overflow: hidden;
            position: relative;
        }

        .progress-bar {
            height: 10px;
            background: #4caf50;
            width: 0;
            transition: width 1.5s ease-in-out;
        }

        .progress-bar.visible {
            width: var(--progress-width);
        }

        /* Tombol Sosial Media */
        .social-links {
            display: flex;
            justify-content: start;
            gap: 15px;
            margin-top: 20px;
        }

        .social-link {
            width: 50px;
            height: 50px;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transition: transform 0.3s ease, background-color 0.3s ease;
            text-decoration: none;
        }

        .social-link img {
            width: 24px;
            height: 24px;
        }

        .social-link:hover {
            transform: scale(1.2);
            background-color: #fff;
        }

        .social-link.instagram:hover {
            background-color: #e4405f;
        }

        .social-link.linkedin:hover {
            background-color: #0077b5;
        }

        .social-link.email:hover {
            background-color: #ea4335;
        }

        /* Media Query */
        @media (max-width: 768px) {
            .profile-container {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .social-links {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="profile-container">
        <!-- Kolom Kiri: Foto Profil -->
        <div class="profile-image">
            <img src="https://via.placeholder.com/180" alt="Foto Profil">
        </div>

        <!-- Kolom Kanan: Info Profil -->
        <div class="profile-info">
            <h1>Nama Anda</h1>
            <p class="subtitle">Web Developer | Designer | Enthusiast</p>
            <p>Saya seorang pengembang web yang fokus pada desain modern dan solusi teknologi. Selalu bersemangat untuk belajar dan mengembangkan keterampilan baru.</p>

            <!-- Progress Bar untuk Skill -->
            <div class="skills">
                <div class="skill">
                    <p class="skill-name">HTML</p>
                    <div class="progress">
                        <div class="progress-bar" style="--progress-width: 90%;"></div>
                    </div>
                </div>
                <div class="skill">
                    <p class="skill-name">CSS</p>
                    <div class="progress">
                        <div class="progress-bar" style="--progress-width: 85%;"></div>
                    </div>
                </div>
                <div class="skill">
                    <p class="skill-name">JavaScript</p>
                    <div class="progress">
                        <div class="progress-bar" style="--progress-width: 75%;"></div>
                    </div>
                </div>
            </div>

            <!-- Tombol Sosial Media -->
            <div class="social-links">
                <a href="https://www.instagram.com/usernameanda" target="_blank" class="social-link instagram">
                    <img src="https://cdn-icons-png.flaticon.com/512/2111/2111463.png" alt="Instagram">
                </a>
                <a href="https://www.linkedin.com/in/usernameanda" target="_blank" class="social-link linkedin">
                    <img src="https://cdn-icons-png.flaticon.com/512/145/145807.png" alt="LinkedIn">
                </a>
                <a href="mailto:emailanda@example.com" class="social-link email">
                    <img src="https://cdn-icons-png.flaticon.com/512/732/732200.png" alt="Email">
                </a>
            </div>
        </div>
    </div>

    <script>
        // Animasi Progress Bar saat scroll
        const progressBars = document.querySelectorAll('.progress-bar');
        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.5 });

        progressBars.forEach(bar => observer.observe(bar));
    </script>
</body>
</html>
