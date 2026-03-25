
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>Mologna Residences | Ultra-Luxury Accommodations</title>
  <!-- Google Fonts + Font Awesome -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700;800;900&family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- AOS Library for scroll animations -->
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #FCF9F5;
      color: #1E2A28;
      overflow-x: hidden;
    }

    /* Custom scrollbar */
    ::-webkit-scrollbar {
      width: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #E8DFD3;
    }
    ::-webkit-scrollbar-thumb {
      background: #C6A15B;
      border-radius: 10px;
    }

    .container {
      max-width: 1440px;
      margin: 0 auto;
      padding: 0 48px;
    }

    /* Navigation - Glassmorphism */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 32px 0;
      flex-wrap: wrap;
      position: sticky;
      top: 0;
      background: rgba(252, 249, 245, 0.95);
      backdrop-filter: blur(10px);
      z-index: 1000;
      transition: all 0.3s;
    }

    .logo {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      font-weight: 800;
      background: linear-gradient(135deg, #B8860B, #8B5A2B);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      letter-spacing: -0.5px;
    }

    .logo span {
      font-weight: 400;
      color: #5C3E1B;
      background: none;
      -webkit-background-clip: unset;
    }

    .nav-links {
      display: flex;
      gap: 3rem;
      align-items: center;
    }

    .nav-links a {
      text-decoration: none;
      font-weight: 500;
      color: #2C3E2F;
      transition: 0.3s;
      font-size: 0.95rem;
      letter-spacing: 0.3px;
    }

    .nav-links a:hover {
      color: #B8860B;
    }

    .contact-cta {
      background: #B8860B;
      color: white !important;
      padding: 12px 28px;
      border-radius: 50px;
      font-weight: 600;
      box-shadow: 0 4px 12px rgba(184, 134, 11, 0.3);
    }

    .contact-cta:hover {
      background: #9B6E0C;
      transform: translateY(-2px);
    }

    /* Hero Section - cinematic */
    .hero {
      margin: 40px 0 80px 0;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 60px;
    }

    .hero-text {
      flex: 1.2;
    }

    .hero-text .badge {
      background: linear-gradient(135deg, #EBDCC9, #DCCFAE);
      display: inline-block;
      padding: 8px 20px;
      border-radius: 100px;
      font-size: 0.85rem;
      font-weight: 700;
      color: #5A3E1B;
      margin-bottom: 28px;
    }

    .hero-text h1 {
      font-family: 'Playfair Display', serif;
      font-size: 4.2rem;
      font-weight: 800;
      line-height: 1.1;
      letter-spacing: -0.02em;
      color: #1A2C26;
      margin-bottom: 24px;
    }

    .hero-text p {
      font-size: 1.2rem;
      color: #5C6E64;
      max-width: 90%;
      margin-bottom: 36px;
      line-height: 1.6;
    }

    .hero-stats {
      display: flex;
      gap: 48px;
      margin-top: 24px;
    }

    .stat {
      font-weight: 600;
    }

    .stat strong {
      font-size: 2rem;
      display: block;
      color: #B8860B;
      font-family: 'Playfair Display', serif;
    }

    .hero-image {
      flex: 1;
      border-radius: 32px;
      overflow: hidden;
      box-shadow: 0 40px 50px -25px rgba(0,0,0,0.25);
      transition: 0.5s;
    }

    .hero-image img {
      width: 100%;
      height: auto;
      display: block;
      transition: transform 0.7s ease;
    }

    .hero-image:hover img {
      transform: scale(1.03);
    }

    /* Section Headers */
    .section-header {
      text-align: center;
      margin: 100px 0 50px 0;
    }

    .section-header h2 {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      font-weight: 700;
      color: #1E2F2A;
    }

    .section-header p {
      color: #7D8C83;
      max-width: 650px;
      margin: 16px auto 0;
      font-size: 1.1rem;
    }

    /* Filter Tabs */
    .filter-tabs {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-bottom: 50px;
      flex-wrap: wrap;
    }

    .filter-btn {
      background: transparent;
      border: 1px solid #E0D5C4;
      padding: 10px 28px;
      border-radius: 40px;
      font-weight: 600;
      cursor: pointer;
      transition: 0.3s;
      font-family: 'Inter', sans-serif;
    }

    .filter-btn.active, .filter-btn:hover {
      background: #B8860B;
      color: white;
      border-color: #B8860B;
    }

    /* Cards Grid - Enhanced */
    .cards-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(380px, 1fr));
      gap: 45px;
      margin: 40px 0 30px;
    }

    .accommodation-card {
      background: white;
      border-radius: 32px;
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.2, 0.9, 0.4, 1.1);
      box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.08);
      cursor: pointer;
    }

    .accommodation-card:hover {
      transform: translateY(-12px);
      box-shadow: 0 35px 45px -18px rgba(0, 0, 0, 0.2);
    }

    .card-img {
      height: 300px;
      overflow: hidden;
      position: relative;
    }

    .card-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.6s ease;
    }

    .accommodation-card:hover .card-img img {
      transform: scale(1.08);
    }

    .card-badge {
      position: absolute;
      top: 20px;
      right: 20px;
      background: rgba(0,0,0,0.7);
      backdrop-filter: blur(8px);
      padding: 6px 14px;
      border-radius: 30px;
      color: #FFD966;
      font-size: 0.75rem;
      font-weight: 700;
    }

    .card-content {
      padding: 28px 28px 32px;
    }

    .card-title {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      margin-bottom: 16px;
      flex-wrap: wrap;
    }

    .card-title h3 {
      font-size: 1.6rem;
      font-weight: 700;
      font-family: 'Playfair Display', serif;
    }

    .price {
      font-size: 1.8rem;
      font-weight: 800;
      color: #B8860B;
    }

    .price small {
      font-size: 0.85rem;
      font-weight: 500;
      color: #8F9B92;
    }

    .amenities {
      display: flex;
      gap: 20px;
      margin: 20px 0;
      color: #6A7C72;
      font-size: 0.85rem;
      flex-wrap: wrap;
    }

    .amenities i {
      color: #C6A15B;
      margin-right: 6px;
    }

    .desc {
      color: #4A5B52;
      line-height: 1.5;
      margin-bottom: 28px;
      font-size: 0.95rem;
    }

    .btn-detail {
      background: linear-gradient(135deg, #1F2A24, #2A3A32);
      border: none;
      padding: 14px 0;
      width: 100%;
      font-weight: 700;
      border-radius: 50px;
      color: white;
      transition: 0.3s;
      cursor: pointer;
      font-family: inherit;
      font-size: 0.95rem;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
    }

    .btn-detail:hover {
      background: #B8860B;
      transform: scale(1.02);
    }

    /* Testimonials */
    .testimonials {
      background: #F5EFE6;
      border-radius: 48px;
      padding: 70px 60px;
      margin: 80px 0;
    }

    .testimonial-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 40px;
      margin-top: 50px;
    }

    .testimonial-card {
      background: white;
      padding: 32px;
      border-radius: 28px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.05);
    }

    .testimonial-card i {
      color: #C6A15B;
      font-size: 2rem;
      margin-bottom: 20px;
    }

    .testimonial-card p {
      font-style: italic;
      line-height: 1.6;
      margin-bottom: 20px;
    }

    .testimonial-card h4 {
      font-weight: 700;
      margin-top: 10px;
    }

    /* Contact Premium */
    .contact-premium {
      background: linear-gradient(135deg, #1E2F2A, #2A4038);
      border-radius: 48px;
      padding: 70px 60px;
      margin: 80px 0;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      gap: 40px;
    }

    .contact-left h3 {
      font-family: 'Playfair Display', serif;
      font-size: 2.4rem;
      color: #FFE6C7;
      margin-bottom: 16px;
    }

    .whatsapp-mega {
      background: #25D366;
      padding: 20px 48px;
      border-radius: 80px;
      display: inline-flex;
      align-items: center;
      gap: 16px;
      font-weight: 800;
      font-size: 1.3rem;
      color: #1E2F2A;
      text-decoration: none;
      transition: 0.3s;
      box-shadow: 0 12px 28px rgba(37,211,102,0.3);
    }

    .whatsapp-mega:hover {
      transform: scale(1.05);
      background: #20b859;
    }

    footer {
      text-align: center;
      padding: 50px 20px;
      border-top: 1px solid #E8DFD3;
      color: #8C9A91;
    }

    @media (max-width: 900px) {
      .container {
        padding: 0 24px;
      }
      .hero-text h1 {
        font-size: 2.8rem;
      }
      .navbar {
        flex-direction: column;
        gap: 20px;
      }
      .section-header h2 {
        font-size: 2.2rem;
      }
    }
  </style>
</head>
<body>

<div class="container">
  <!-- Navigation -->
  <div class="navbar">
    <div class="logo">MOLOGNA<span> · SUITES</span></div>
    <div class="nav-links">
      <a href="#">Home</a>
      <a href="#accommodations">Residences</a>
      <a href="#testimonials">Experiences</a>
      <a href="#contact" class="contact-cta">Secure Your Stay</a>
    </div>
  </div>

  <!-- Hero Section -->
  <div class="hero" data-aos="fade-up">
    <div class="hero-text">
      <div class="badge"><i class="fas fa-crown"></i>  Mologna's Most Coveted Address</div>
      <h1>Where heritage meets <br>contemporary opulence</h1>
      <p>Exquisite studio & one-bedroom sanctuaries. Each residence curated with bespoke Italian finishes, smart home technology, and breathtaking views over Mologna's historic district.</p>
      <div class="hero-stats">
        <div class="stat"><strong>14</strong> Exclusive Units</div>
        <div class="stat"><strong>€500–€1,200</strong> Tailored rates</div>
        <div class="stat"><strong>5★</strong> Concierge Service</div>
      </div>
    </div>
    <div class="hero-image">
      <img src="https://images.pexels.com/photos/2587054/pexels-photo-2587054.jpeg?auto=compress&cs=tinysrgb&w=1600" alt="Mologna luxury exterior">
    </div>
  </div>

  <!-- Accommodations Section -->
  <div id="accommodations">
    <div class="section-header" data-aos="fade-up">
      <h2>Signature residences</h2>
      <p>Curated studios and sophisticated one-bedroom apartments — each a masterpiece of design and comfort.</p>
    </div>

    <div class="filter-tabs" data-aos="fade-up">
      <button class="filter-btn active" data-filter="all">All Properties</button>
      <button class="filter-btn" data-filter="studio">Luxury Studios</button>
      <button class="filter-btn" data-filter="bedroom">1-Bedroom Suites</button>
    </div>

    <div class="cards-grid" id="cardsContainer">
      <!-- Dynamic cards will be loaded via JS for perfect realism, but we build static structure with data attributes -->
    </div>
  </div>

  <!-- Testimonials -->
  <div id="testimonials" class="testimonials" data-aos="fade-up">
    <div style="text-align: center;">
      <h2 style="font-family: 'Playfair Display'; font-size: 2.2rem;">Loved by global nomads</h2>
      <p style="margin-top: 12px;">What our residents say about Mologna living</p>
    </div>
    <div class="testimonial-grid">
      <div class="testimonial-card"><i class="fas fa-quote-left"></i><p>"Absolutely breathtaking. The studio I stayed in had museum-quality furniture and the most incredible sunrise view. Worth every euro."</p><h4>— Sofia M.</h4></div>
      <div class="testimonial-card"><i class="fas fa-quote-left"></i><p>"Professional, seamless, and luxurious. The 1-bedroom suite felt like a 5-star hotel but with the warmth of home. Highly recommend."</p><h4>— James K.</h4></div>
      <div class="testimonial-card"><i class="fas fa-quote-left"></i><p>"Best decision relocating to Mologna Suites. The team is incredible, and the attention to detail is unmatched."</p><h4>— Elena R.</h4></div>
    </div>
  </div>

  <!-- Contact Section with WhatsApp -->
  <div id="contact" class="contact-premium" data-aos="fade-up">
    <div class="contact-left">
      <h3>Reserve your masterpiece</h3>
      <p style="color: #E9DCCB; max-width: 450px;">Speak directly with our residence curator. Instant confirmation, flexible leases, and VIP access.</p>
      <p style="margin-top: 20px;"><i class="fas fa-check-circle"></i> 24/7 support • Virtual tours available</p>
    </div>
    <div>
      <a href="https://wa.me/447478061828?text=Hello%20Mologna%20Suites!%20I'm%20interested%20in%20your%20luxury%20accommodations%20(€500-1200).%20Please%20share%20available%20options." class="whatsapp-mega" target="_blank">
        <i class="fab fa-whatsapp fa-2x"></i> +44 7478 061828
      </a>
      <p style="margin-top: 16px; font-size: 0.85rem; color: #DDD2C0;">Click to chat — response within minutes</p>
    </div>
  </div>

  <footer>
    <p>© 2025 MOLOGNA SUITES — The pinnacle of residential artistry in Mologna. Prices range from €500–€1200 based on season and lease duration.</p>
    <p style="margin-top: 14px;"><i class="fab fa-whatsapp"></i> VIP WhatsApp: +447478061828  |  concierge@molognasuites.com</p>
  </footer>
</div>

<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
<script>
  AOS.init({ duration: 800, once: true, offset: 100 });

  // Luxury accommodations data with premium images and realistic details
  const accommodations = [
    { id: 1, name: "The Atelier Studio", type: "studio", price: 550, size: "42 m²", features: "Smart home • Marble bath", desc: "Minimalist elegance with floor-to-ceiling windows, designer furniture, and curated art.", img: "https://images.pexels.com/photos/276625/pexels-photo-276625.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2", amenities: "WiFi 6 • AC • Soundproof" },
    { id: 2, name: "Terrazza Studio", type: "studio", price: 720, size: "48 m²", features: "Private terrace • Espresso bar", desc: "Sun-drenched studio with a lush balcony, oak flooring, and panoramic city views.", img: "https://images.pexels.com/photos/1648772/pexels-photo-1648772.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2", amenities: "Terrace • 4K TV • Rain shower" },
    { id: 3, name: "Palazzo Suite", type: "bedroom", price: 950, size: "68 m²", features: "King bed • Separate living", desc: "Expansive one-bedroom with Italian leather sofa, gourmet kitchen, and walk-in closet.", img: "https://images.pexels.com/photos/1571468/pexels-photo-1571468.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2", amenities: "Walk-in shower • Dishwasher • Netflix" },
    { id: 4, name: "Belvedere Residence", type: "bedroom", price: 1200, size: "82 m²", features: "Panoramic views • Concierge", desc: "Top-floor masterpiece with heated floors, automated curtains, and private elevator access.", img: "https://images.pexels.com/photos/271618/pexels-photo-271618.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2", amenities: "Spa shower • Rooftop • Parking" },
    { id: 5, name: "Vintage Loft Studio", type: "studio", price: 500, size: "38 m²", features: "Exposed brick • High ceilings", desc: "Industrial-chic design with curated antiques, high-speed internet, and central location.", img: "https://images.pexels.com/photos/439227/pexels-photo-439227.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2", amenities: "Washer/dryer • Smart lock • Bicycle storage" },
    { id: 6, name: "Grande 1-Bedroom", type: "bedroom", price: 1100, size: "75 m²", features: "Workspace • Fitness access", desc: "Executive retreat with designer desk, premium bedding, and residents' lounge access.", img: "https://images.pexels.com/photos/2623464/pexels-photo-2623464.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2", amenities: "Gym • Pet friendly • Concierge" },
    { id: 7, name: "Cortile Studio", type: "studio", price: 680, size: "45 m²", features: "Courtyard view • Silent AC", desc: "Tranquil studio overlooking a historic courtyard, with premium bedding and minimalist design.", img: "https://images.pexels.com/photos/280229/pexels-photo-280229.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2", amenities: "Courtyard • Netflix • Rainfall shower" }
  ];

  function renderCards(filter = "all") {
    const container = document.getElementById("cardsContainer");
    const filtered = filter === "all" ? accommodations : accommodations.filter(acc => acc.type === filter);
    container.innerHTML = filtered.map(acc => `
      <div class="accommodation-card" data-aos="fade-up" data-type="${acc.type}">
        <div class="card-img">
          <img src="${acc.img}" alt="${acc.name}" loading="lazy">
          <div class="card-badge">${acc.type === "studio" ? "⭐ Signature Studio" : "🏆 Premier 1BR"}</div>
        </div>
        <div class="card-content">
          <div class="card-title">
            <h3>${acc.name}</h3>
            <div class="price">€${acc.price}<small>/month</small></div>
          </div>
          <div class="amenities">
            <span><i class="fas fa-expand-alt"></i> ${acc.size}</span>
            <span><i class="fas fa-star"></i> ${acc.features}</span>
          </div>
          <div class="desc">${acc.desc}<br><span style="font-size:0.85rem; color:#B8860B;"><i class="fas fa-check-circle"></i> ${acc.amenities}</span></div>
          <button class="btn-detail" onclick="window.open('https://wa.me/447478061828?text=Hello!%20I'm%20interested%20in%20the%20${encodeURIComponent(acc.name)}%20at%20€${acc.price}%20in%20Mologna.', '_blank')"><i class="fab fa-whatsapp"></i> Inquire & book</button>
        </div>
      </div>
    `).join("");
  }

  renderCards();

  // Filter functionality
  const filterBtns = document.querySelectorAll(".filter-btn");
  filterBtns.forEach(btn => {
    btn.addEventListener("click", () => {
      filterBtns.forEach(b => b.classList.remove("active"));
      btn.classList.add("active");
      const filterValue = btn.getAttribute("data-filter");
      renderCards(filterValue);
    });
  });
</script>
</body>
</html>
