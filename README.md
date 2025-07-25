

<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stasiun Klaten</title>
    <style>
        /* Global Styles */
        :root {
            --primary-blue: #02155e;
            --secondary-blue: #003366;
            --accent-orange: #ef6408;
            --light-blue: #e6f2ff;
            --white: #ffffff;
            --gray: #f5f5f5;
            --dark-gray: #333333;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--dark-gray);
            background-color: var(--white);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        h1, h2, h3 {
            color: var(--secondary-blue);
            margin-bottom: 20px;
        }
        
        p {
            margin-bottom: 15px;
        }
        
        .btn {
            display: inline-block;
            padding: 10px 20px;
            background-color: var(--accent-orange);
            color: var(--white);
            text-decoration: none;
            border-radius: 5px;
            transition: all 0.3s ease;
            font-weight: bold;
        }
        
        .btn:hover {
            background-color: var(--secondary-blue);
            transform: translateY(-2px);
        }
        
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: var(--accent-orange);
            margin: 15px auto 0;
        }
        
        /* Header Styles */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
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
        }
        
        .logo-img {
            width: 50px;
            height: 50px;
            margin-right: 10px;
        }
        
        .logo-text {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary-blue);
        }
        
        .logo-text span {
            color: var(--accent-orange);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--secondary-blue);
            font-weight: 500;
            transition: color 0.3s ease;
        }
        
        nav ul li a:hover {
            color: var(--accent-orange);
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background-color: var(--light-blue);
            padding: 150px 0 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--secondary-blue);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
            color: var(--dark-gray);
        }
        
         .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
        }

        .hero-image img {
            width: 100%;
            max-width: 900px;
            height: 400px;
            object-fit: cover;
            border-radius: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        

        
        /* About Section */
        .about {
            background-color: var(--white);
        }
        
        .about-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            
        }
        
        .about-img {
            flex: 1;
            min-width: 300px;
            border-radius: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        /* Services Section */
        .services {
            background-color: var(--gray);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .service-card {
            background-color: var(--white);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: var(--accent-orange);
            margin-bottom: 20px;
        }
        
        .service-card h3 {
            color: var(--primary-blue);
        }
        
        /* Gallery Section */
        .gallery {
            background-color: var(--white);
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 20px;
            
        }
        
        .gallery-item {
           
            height: 260px;
            width: 220px;
            border-radius: 10px;
            overflow: hidden;
            position: center;
            place-self: center;
            align-items: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            
            
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
            
            
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
            
        }
        
        /* Contact Section */
        .contact {
            background-color: var(--light-blue);
        }
        
        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
        }
        
        .contact-info {
            flex: 1;
            min-width: 300px;
        }
        
        .contact-info h3 {
            color: var(--primary-blue);
        }
        
        .info-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 20px;
        }
        
        .info-icon {
            color: var(--accent-orange);
            font-size: 1.5rem;
            margin-right: 15px;
            margin-top: 5px;
        }
        
        .contact-form {
            flex: 1;
            min-width: 300px;
            background-color: var(--white);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        .form-group textarea {
            height: 150px;
        }
        
        /* Footer */
        footer {
            background-color: var(--secondary-blue);
            color: var(--white);
            padding: 40px 0 20px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .footer-logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--white);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
        }
        
        .footer-logo span {
            color: var(--accent-orange);
        }
        
        .footer-links h3 {
            color: var(--white);
            margin-bottom: 20px;
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links ul li {
            margin-bottom: 10px;
        }
        
        .footer-links ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links ul li a:hover {
            color: var(--accent-orange);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: var(--white);
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--accent-orange);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #ccc;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                align-items: flex-start;
            }
            
            nav {
                width: 100%;
                margin-top: 15px;
                display: none;
            }
            
            nav.active {
                display: block;
            }
            
            nav ul {
                flex-direction: column;
            }
            
            nav ul li {
                margin: 0;
                margin-bottom: 10px;
            }
            
            .mobile-menu {
                display: block;
                position: absolute;
                top: 20px;
                right: 20px;
            }
            
            .hero {
                padding: 120px 0 60px;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            section {
                padding: 40px 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-container">
            <div class="logo">
                <img src="data:image/jpeg;base64,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" alt="Logo PT Kereta Api Indonesia - Garuda bergerak melintasi rel kereta warna biru dan orange" class="logo-img">
                <div class="logo-text">Stasiun <span>Klaten</span></div>
            </div>
            
            <div class="mobile-menu">☰</div>
            
            <nav>
                <ul>
                    <li><a href="#home">Beranda</a></li>
                    <li><a href="#about">Tentang Kami</a></li>
                    <li><a href="#services">Informasi</a></li>
                    <li><a href="#gallery">Fasilitas</a></li>
                    <li><a href="#contact">Kontak</a></li>
                </ul>
            </nav>
        </div>
    </header>
     
    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h1>Stasiun Klaten</h1>
            <p>Sebagai perusahaan BUMN penyedia jasa transportasi kereta api terbesar di Indonesia, kami berkomitmen untuk memberikan pelayanan terbaik dengan standar keselamatan tinggi.</p>
            <a href="#about" class="btn">Pelajari Lebih Lanjut</a>
            <br>
            <br>

           <div class="hero-image">
                    <img src="c:\Users\HP\Downloads\WhatsApp Image 2025-07-04 at 08.06.48.jpeg"foto profil alt="Team in modern office collaborating on digital project with laptops and whiteboard" />
                </div>
            
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">Profil Stasiun Klaten</h2>
            
            <div class="about-content">
                <div class="about-text">
                    <h3>Stasiun Klaten</h3>
                    <p style="text-align: justify;">Stasiun Klaten (KT) adalah stasiun kereta api kelas I yang terletak di Tonggalan, Klaten Tengah, Klaten pada ketinggian +151 meter, termasuk dalam pengelolaan Daerah Operasi VI Yogyakarta dan KAI Commuter. Kini, Stasiun Klaten dilengkapi dengan sistem tiket elektronik, papan informasi digital, dan peron modern. Meski begitu, sisa-sisa arsitektur kolonialnya masih terlihat, mengingatkan kita pada usia dan kisah panjang stasiun ini.</p>
                </div>
                
                <img src="https://nos.jkt-1.neo.id/jurnalis/post/2/1294-1745766600-stasiun-klaten-semakin-modern-akses-mudah-ke-wisata-dan-bandara-layani-277-ribu-penumpa.webp" alt="Stasiun kereta api besar dengan arsitektur kolonial Belanda, penumpang sedang naik dan turun dari kereta" class="about-img">
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">Visi dan Misi Perusahaan</h2>
            
            <div class="about-content">
                <div class="about-text">
                    <h3 style="text-align: center;">Visi</h3>
                    <p style="text-align: center;">Menggerakkan transportasi berkelanjutan, meningkatkan kualitas hidup masyarakat</p>
                    <h3 style="text-align: center;">Misi</h3>
                    <p style="text-align: center;">Menyediakan jasa yang mengedepankan keselamatan, ketepatan waktu, dan kenyamanan</p>
                    <p style="text-align: center;">Mengembangkan sumber daya dengan mengedepankan ESG</p>
                    <p style="text-align: center;">Berperan aktif dalam pengembangan transportasi antarmoda berkelanjutan bersama para pemangku kepentingan</p>
                </div>
                
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Stasiun Klaten</h2>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">👥</div>
                    <h3>Struktur Organisasi</h3>
                    <p>Struktur organisasi jajaran direksi, komisaris, daderah, dan stasiun</p>
                    <a href="https://drive.google.com/drive/mobile/folders/1YHK5rq2vsW8QvMED71ogFUA5dO8IWGs9?hl=ID">Selengkapnya →</a>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">🚆</div>
                    <h3>Operasional</h3>
                    <p>Kereta api yang dilayani, kereta api berhenti, kereta api langsung, emplasemen, panjang jalue efektif</p>
                    <a href="https://docs.google.com/spreadsheets/d/1zNOQbbzc_bfVioL5rPiKXd6wvSwH78Lf-PfB8R1DyDE/htmlview#gid=1362484005">Selengkapnya →</a>
                </div>
                

                <div class="service-card">
                    <div class="service-icon">📑</div>
                    <h3>IBPR</h3>
                    <p>Realisasi Isi IBPR</p>
                    <a href="https://drive.google.com/drive/mobile/folders/1N3rpkj3s0CTMwpfhOXwnbTC8B5oAwHeE">Selengkapnya →</a>
                </div>


                
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="gallery" id="gallery">
        <div class="container">
            <h2 class="section-title">INFORMASI DIGITAL STASIUN KLATEN</h2>
    
            
            <div class="gallery-grid">
                <div class="gallery-item">
                    <h4 style="text-align: center;">STRUKTUR ORGANISASI</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (STRUKTUR ORGANISASI) fix_page-0001 (1).jpg" alt="missing">
                    <figcaption class="gallery-item-captiontext-center">   
                        </figcaption>
                    
                </div>
               
                <div class="gallery-item">
                    <h4 style="text-align: center;">VOLUME PENUMPANG</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (DATA VOLUME PNP KA JJ DAN KRL 2025)_page-0001.jpg" alt="Interior kereta kelas eksekutif dengan kursi empuk berwarna biru dan meja lipat">
                    <figcaption>
                        </figcaption>
                </div> 
                
                <div class="gallery-item">
                    <h4 style="text-align: center;">IBPR</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (IBPR 2025)_page-0001.jpg" alt="Stasiun besar dengan banyak penumpang dan digital signage modern">
        
                </div> 
                
                <div class="gallery-item">
                    <h4 style="text-align: center;">SAFETY TALK</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (LAPORAN SAFETY TALK) _page-0001.jpg"> 
                    
                </div> 
                
                <div class="gallery-item">
                    <h4 style="text-align: center;">PROGRAM KESELAMATAN</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (PROGRAM KESELAMATAN 2025)_page-0001.jpg" alt="Petugas kereta api dengan seragam resmi sedang membantu penumpang lansia">
                    
                </div>
                
                <div class="gallery-item">
                    <h4 style="text-align: center;">SMARTCARD DIRJEN</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (SMARTCARD DIRJENKA 2025) _page-0001.jpg" alt="Pemandangan udara rel kereta melintasi lanskap pegunungan yang hijau"> 
                   
                </div>

                <div class="gallery-item">
                    <h4 style="text-align: center;">DATA PENUMPANG ANGLEB</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (DATA PNP ANGLEB 2024-2025) _page-0001.jpg" alt="Pemandangan udara rel kereta melintasi lanskap pegunungan yang hija"> 
                   
                </div>

                <div class="gallery-item">
                    <h4 style="text-align: center;">D-SAFE</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (D-SAFE 2025)_page-0001.jpg" alt="Pemandangan udara rel kereta melintasi lanskap pegunungan yang hijau">
                </div>

                <div class="gallery-item">
                    <h4 style="text-align: center;">IMO KLATEN</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (IMO 2025)_page-0001.jpg" alt="Pemandangan udara rel kereta melintasi lanskap pegunungan yang hijau">
                </div>

                <div class="gallery-item">
                    <h4 style="text-align: center;">DOKUMEN PEMBINAAN</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (PEMBINAAN KLATEN 2025)_page-0001.jpg" alt="Pemandangan udara rel kereta melintasi lanskap pegunungan yang hijau">
                </div>

                <div class="gallery-item">
                    <h4 style="text-align: center;">APAR STASIUN KLATEN</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (APAR STASIUN KLATEN 2025) _page-0001.jpg" alt="Pemandangan udara rel kereta melintasi lanskap pegunungan yang hijau">
                </div>

                <div class="gallery-item">
                    <h4 style="text-align: center;">E-RAPOR KLATEN</h4>
                    <img src="c:\Users\HP\Downloads\QR CODE (E RAPOR KLATEN 2025) _page-0001.jpg" alt="Pemandangan udara rel kereta melintasi lanskap pegunungan yang hijau">
                </div>

                
            </div>
        </div>
    </section>


    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Layanan Kereta Api</h2>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">🚆</div>
                    <h3>Kereta Jarak Jauh</h3>
                    <p style="text-align: justify;">Melayani perjalanan antarkota dengan berbagai kelas mulai dari ekonomi hingga eksekutif, menghubungkan kota-kota besar di daerah lintas Jawa.</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">🚉</div>
                    <h3>Commuter Line</h3>
                    <p style="text-align: justify;">Layanan kereta cmomuter untuk wilayah yogyakarta-palur untuk mobilitas harian yang efisien.</p>
                </div>
                
                
                <div class="service-card">
                    <div class="service-icon">📦</div>
                    <h3>Angkutan Barang</h3>
                    <p style="text-align: justify;">Solusi logistik dengan kereta barang untuk pengiriman massal yang hemat dan ramah lingkungan.</p>
                </div>

            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="gallery" id="gallery">
        <div class="container">
            <h2 class="section-title">Fasilitas Stasiun</h2>
            
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="c:\Users\HP\Downloads\WhatsApp Image 2025-07-14 at 20.04.08.jpeg" alt="Eksterior kereta api eksekutif baru dengan desain aerodinamis dan cat biru metalik">
                </div>
                <div class="gallery-item">
                    <img src="c:\Users\HP\Downloads\WhatsApp Image 2025-07-14 at 20.04.06.jpeg" alt="Interior kereta kelas eksekutif dengan kursi empuk berwarna biru dan meja lipat">
                </div>
                <div class="gallery-item">
                    <img src="c:\Users\HP\Downloads\WhatsApp Image 2025-07-14 at 20.04.08 (2).jpeg" alt="Stasiun besar dengan banyak penumpang dan digital signage modern">
                </div>
                <div class="gallery-item">
                    <img src="https://placehold.co/600x400" alt="Pemandangan matahari terbenam dari jendela kereta yang sedang melintasi sawah">
                </div>
                <div class="gallery-item">
                    <img src="https://placehold.co/600x400" alt="Petugas kereta api dengan seragam resmi sedang membantu penumpang lansia">
                </div>
                <div class="gallery-item">
                    <img src="https://placehold.co/600x400" alt="Pemandangan udara rel kereta melintasi lanskap pegunungan yang hijau">
                </div>
                
                
               
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Hubungi Kami</h2>
            
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Stasiun Klaten - Daop 6 Yogyakarta</h3>
                    
                    <div class="info-item">
                        <span class="info-icon">📍</span>
                        <div>
                            <p><strong>Alamat:</strong></p>
                            <p>Jalan K.H. Samanhudi Nomor 53, Tonggalan, Klaten Tengah, Kabupaten Klaten, Jawa Tengah, Indonesia</p>
                        </div>
                    </div>
                    
                    <div class="info-item">
                        <span class="info-icon">📞</span>
                        <div>
                            <p><strong>Telepon:</strong></p>
                            <p>121 (Call Center)</p>
                        </div>
                    </div>
                    
                    <div class="info-item">
                        <span class="info-icon"></span>
                        <div>
                            
                        </div>
                    </div>
                    
                    <div class="social-links">
                        <a href="#" aria-label="Facebook PT Kereta Api Indonesia">FB</a>
                        <a href="#" aria-label="Twitter PT Kereta Api Indonesia">TW</a>
                        <a href="#" aria-label="Instagram PT Kereta Api Indonesia">IG</a>
                        <a href="#" aria-label="YouTube PT Kereta Api Indonesia">YT</a>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Nama Lengkap</label>
                            <input type="text" id="name" placeholder="Masukkan nama lengkap" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" placeholder="Masukkan alamat email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="phone">Nomor Telepon</label>
                            <input type="tel" id="phone" placeholder="Masukkan nomor telepon">
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Pesan</label>
                            <textarea id="message" placeholder="Tulis pesan Anda di sini" required></textarea>
                        </div>
                        
                        <button type="submit" class="btn">Kirim Pesan</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-about">
                <div class="logo">
                <img src="data:image/jpeg;base64,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" alt="Logo PT Kereta Api Indonesia - Garuda bergerak melintasi rel kereta warna biru dan orange" class="logo-img">

                <div class="logo-text">Stasiun <span>Klaten</span></div>
            </div>
            <br>
        
                    <p>Perusahaan BUMN penyedia jasa transportasi kereta api terbesar di Indonesia</p>
                </div>
                
                <div class="footer-links">
                    <h3>AKHLAK</h3>
                    <ul>
                        <li><a href="#home">Amanah</a></li>
                        <li><a href="#about">Kompeten</a></li>
                        <li><a href="#services">Harmonis</a></li>
                        <li><a href="#gallery">Adaptif</a></li>
                        <li><a href="#contact">Kolaboratif</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h3>Layanan</h3>
                    <ul>
                        <li><a href="#">Tiket Kereta</a></li>
                        <li><a href="#">Jadwal Kereta</a></li>
                        <li><a href="#">Fasilitas Penumpang</a></li>
                        
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; Stasiun Klaten - PT Kereta Api Indonesia (Persero).</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('nav').classList.toggle('active');
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // Close mobile menu if open
                document.querySelector('nav').classList.remove('active');
            });
        });
    </script>
</body>
</html>



# stasiun-klaten
