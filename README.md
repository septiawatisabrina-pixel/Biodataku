<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Biodata | Sabrina Septiawati</title>
    <!-- Font Google & Ikon sederhana -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #f9f3e6 0%, #ffe6d5 100%);
            font-family: 'Inter', sans-serif;
            padding: 2rem 1.5rem;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Kartu utama */
        .card {
            max-width: 750px;
            width: 100%;
            background: #ffffffdd;
            backdrop-filter: blur(2px);
            background: #fffef7;
            border-radius: 2.5rem;
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.25), 0 4px 12px rgba(0, 0, 0, 0.05);
            overflow: hidden;
            transition: transform 0.2s ease;
        }

        .card:hover {
            transform: scale(1.01);
        }

        /* Header / profil */
        .profile-header {
            background: #c2492d;
            background: linear-gradient(135deg, #b23c1e, #d95b39);
            padding: 1.8rem 2rem 2rem 2rem;
            color: white;
            text-align: center;
        }

        .avatar {
            background: #ffecb3;
            width: 100px;
            height: 100px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1rem auto;
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
            border: 3px solid #fff2cf;
        }

        .avatar i {
            font-size: 3.5rem;
            color: #bc4e2c;
        }

        .profile-header h1 {
            font-size: 1.9rem;
            font-weight: 700;
            letter-spacing: -0.3px;
            margin-bottom: 0.25rem;
        }

        .profile-header .tagline {
            font-size: 0.9rem;
            opacity: 0.9;
            background: #00000020;
            display: inline-block;
            padding: 0.2rem 1rem;
            border-radius: 30px;
            backdrop-filter: blur(2px);
        }

        /* konten biodata */
        .biodata-content {
            padding: 2rem 2rem 1.5rem 2rem;
        }

        .info-grid {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .info-item {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
            background: #fef6ef;
            padding: 0.9rem 1.2rem;
            border-radius: 1.5rem;
            transition: all 0.2s;
            border: 1px solid #ffddc4;
        }

        .info-icon {
            font-size: 1.6rem;
            min-width: 2.2rem;
            color: #c2492d;
        }

        .info-text {
            flex: 1;
        }

        .info-label {
            font-size: 0.75rem;
            text-transform: uppercase;
            font-weight: 600;
            letter-spacing: 0.5px;
            color: #b45a3e;
            margin-bottom: 0.25rem;
        }

        .info-value {
            font-weight: 600;
            font-size: 1.1rem;
            color: #2d2a24;
            line-height: 1.4;
        }

        .hobi-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
            margin-top: 0.3rem;
        }

        .hobi-tag {
            background: #ffffff;
            border-radius: 50px;
            padding: 0.25rem 1rem;
            font-size: 0.85rem;
            font-weight: 500;
            color: #bc4e2c;
            border: 1px solid #ffcdb0;
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
        }

        /* makanan favorit dengan gaya lucu */
        .food-note {
            font-size: 0.75rem;
            color: #a75f41;
            background: #ffefde;
            border-radius: 20px;
            padding: 0.2rem 0.7rem;
            display: inline-block;
            margin-top: 0.4rem;
        }

        /* kotak motivasi */
        .motivation-box {
            background: #f9e2cf;
            border-left: 5px solid #c2492d;
            padding: 1rem 1.4rem;
            border-radius: 1.2rem;
            margin: 1rem 0 1.8rem 0;
        }

        .motivation-box i {
            color: #c2492d;
            margin-right: 0.4rem;
        }

        .motivation-text {
            font-size: 1rem;
            font-weight: 500;
            color: #37251b;
            font-style: italic;
        }

        /* tombol proyek */
        .project-button {
            text-align: center;
            margin: 0 0 2rem 0;
        }

        .btn-proyek {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background: #1e2a2f;
            background: linear-gradient(100deg, #2a3b3f, #1d2c30);
            color: white;
            padding: 0.9rem 2rem;
            border-radius: 60px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.3s;
            box-shadow: 0 8px 18px rgba(0,0,0,0.1);
            border: none;
            cursor: pointer;
        }

        .btn-proyek i {
            font-size: 1.2rem;
            transition: transform 0.2s;
        }

        .btn-proyek:hover {
            background: #2c454b;
            transform: translateY(-3px);
            box-shadow: 0 15px 25px -8px rgba(0,0,0,0.2);
        }

        .btn-proyek:hover i {
            transform: translateX(5px);
        }

        /* catatan tambahan (ayam) & footer */
        .fun-footer {
            background: #fff4ec;
            border-top: 1px solid #ffe2cf;
            padding: 1rem 2rem;
            font-size: 0.7rem;
            text-align: center;
            color: #b67453;
            display: flex;
            justify-content: center;
            gap: 0.8rem;
            flex-wrap: wrap;
        }

        .fun-footer span i {
            margin-right: 4px;
        }

        @media (max-width: 550px) {
            body {
                padding: 1rem;
            }
            .profile-header h1 {
                font-size: 1.5rem;
            }
            .info-value {
                font-size: 0.95rem;
            }
            .btn-proyek {
                padding: 0.7rem 1.5rem;
                font-size: 0.85rem;
            }
        }
    </style>
</head>
<body>

<div class="card">
    <div class="profile-header">
        <div class="avatar">
            <i class="fas fa-user-circle"></i>
        </div>
        <h1>Sabrina Septiawati</h1>
        <div class="tagline">✨ keep growing, keep glowing ✨</div>
    </div>

    <div class="biodata-content">
        <!-- Data grid informatif -->
        <div class="info-grid">
            <!-- Umur -->
            <div class="info-item">
                <div class="info-icon"><i class="fas fa-cake-candles"></i></div>
                <div class="info-text">
                    <div class="info-label">Umur</div>
                    <div class="info-value">16 tahun · Pelajar SMA</div>
                </div>
            </div>

            <!-- Asal Sekolah -->
            <div class="info-item">
                <div class="info-icon"><i class="fas fa-school"></i></div>
                <div class="info-text">
                    <div class="info-label">Asal Sekolah</div>
                    <div class="info-value">SMAN 15 JAKARTA</div>
                </div>
            </div>

            <!-- Hobi dengan tampilan tag -->
            <div class="info-item">
                <div class="info-icon"><i class="fas fa-head-side-headphones"></i></div>
                <div class="info-text">
                    <div class="info-label">Hobi</div>
                    <div class="hobi-list">
                        <span class="hobi-tag"><i class="fas fa-music"></i> Mendengarkan musik</span>
                        <span class="hobi-tag"><i class="fas fa-comments"></i> Mengobrol</span>
                    </div>
                </div>
            </div>

            <!-- Cita-cita -->
            <div class="info-item">
                <div class="info-icon"><i class="fas fa-star-of-life"></i></div>
                <div class="info-text">
                    <div class="info-label">Cita-cita</div>
                    <div class="info-value">Sukses <span style="font-size:0.85rem;">🚀</span></div>
                </div>
            </div>

            <!-- Makanan Favorit dengan gaya lucu -->
            <div class="info-item">
                <div class="info-icon"><i class="fas fa-drumstick-bite"></i></div>
                <div class="info-text">
                    <div class="info-label">Makanan Favorit</div>
                    <div class="info-value">Ayam apapun itu, asal tidak mentah/tiren/basi</div>
                    <div class="food-note"><i class="fas fa-check-circle"></i> ayam goreng, ayam bakar, ayam geprek, ayam katsu... semua enak!</div>
                </div>
            </div>
        </div>

        <!-- Motivasi -->
        <div class="motivation-box">
            <i class="fas fa-quote-left"></i>
            <span class="motivation-text">"Do Good, Look Good, Feel Good."</span>
            <div style="font-size:0.7rem; margin-top: 6px; color:#b45a3e;">— motivasi harian Sabrina</div>
        </div>

        <!-- TOMBOL PROYEK (link ke Dompet-Sabrina) -->
        <div class="project-button">
            <a href="https://septiawatisabrina-pixel.github.io/Dompet-Sabrina/" 
               target="_blank" 
               rel="noopener noreferrer" 
               class="btn-proyek">
                <i class="fas fa-external-link-alt"></i> 
                Lihat Proyek Dompet Sabrina
                <i class="fas fa-arrow-right"></i>
            </a>
            <p style="font-size: 0.7rem; margin-top: 10px; color:#b47453;">✨ Klik tombol di atas untuk menjelajahi proyek✨</p>
        </div>
    </div>

    <!-- Footer lucu / note ayam tidak mentah -->
    <div class="fun-footer">
        <span><i class="fas fa-egg"></i> Anti ayam mentah/tiren/basi</span>
        <span><i class="fas fa-music"></i> Playlist favorit: mood booster</span>
        <span><i class="fas fa-smile-wink"></i> #SuksesBersama</span>
    </div>
</div>

<!-- tambahan sedikit interaksi jika ingin smooth (opsional, tidak mengganggu) -->
<script>
    // Optional: memberikan efek konsol ramah, dan memastikan link aman
    (function() {
        const btn = document.querySelector('.btn-proyek');
        if(btn) {
            btn.addEventListener('click', function(e) {
                // hanya tracking ringan, tidak mengganggu navigasi
                console.log("🌐 Membuka proyek Dompet Sabrina: " + btn.href);
            });
        }
        // efek hover smooth secara css sudah ada
    })();
</script>
</body>
</html>
