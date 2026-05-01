[index.html](https://github.com/user-attachments/files/27280381/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Last Touch Inc. — Professional Cleaning Services</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #FAF7F2;
    --sage: #7A9E87;
    --sage-light: #A8C4B0;
    --sage-dark: #4F7060;
    --charcoal: #2C2C2C;
    --warm-gray: #8A8580;
    --gold: #C8A96E;
    --white: #FFFFFF;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--charcoal);
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 100;
    background: rgba(250,247,242,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(122,158,135,0.15);
    padding: 18px 60px;
    display: flex; align-items: center; justify-content: space-between;
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem; color: var(--sage-dark);
    letter-spacing: 0.02em;
  }
  .nav-logo span { color: var(--gold); }
  .nav-links { display: flex; gap: 36px; list-style: none; }
  .nav-links a {
    text-decoration: none; color: var(--warm-gray);
    font-size: 0.88rem; font-weight: 500; letter-spacing: 0.05em;
    text-transform: uppercase; transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--sage-dark); }
  .nav-cta {
    background: var(--sage); color: var(--white);
    border: none; padding: 10px 24px; border-radius: 40px;
    font-family: 'DM Sans', sans-serif; font-size: 0.85rem;
    font-weight: 500; cursor: pointer; text-decoration: none;
    transition: background 0.2s, transform 0.15s;
    letter-spacing: 0.03em;
  }
  .nav-cta:hover { background: var(--sage-dark); transform: translateY(-1px); }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: grid; grid-template-columns: 1fr 1fr;
    align-items: center;
    padding: 120px 60px 80px;
    position: relative; overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; right: -80px; top: 50%; transform: translateY(-50%);
    width: 700px; height: 700px; border-radius: 50%;
    background: radial-gradient(circle, rgba(122,158,135,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-text { position: relative; z-index: 2; }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(122,158,135,0.12); border: 1px solid rgba(122,158,135,0.3);
    color: var(--sage-dark); padding: 6px 16px; border-radius: 40px;
    font-size: 0.78rem; font-weight: 500; letter-spacing: 0.06em;
    text-transform: uppercase; margin-bottom: 28px;
  }
  .hero-badge::before { content: '✦'; color: var(--gold); }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 5vw, 4.2rem);
    line-height: 1.12; color: var(--charcoal);
    margin-bottom: 24px;
  }
  .hero h1 em { font-style: italic; color: var(--sage); }
  .hero-desc {
    font-size: 1.05rem; color: var(--warm-gray); line-height: 1.7;
    max-width: 440px; margin-bottom: 40px; font-weight: 300;
  }
  .hero-actions { display: flex; gap: 16px; align-items: center; }
  .btn-primary {
    background: var(--sage-dark); color: var(--white);
    padding: 14px 32px; border-radius: 40px; text-decoration: none;
    font-weight: 500; font-size: 0.95rem; transition: all 0.2s;
    letter-spacing: 0.02em;
  }
  .btn-primary:hover { background: var(--charcoal); transform: translateY(-2px); }
  .btn-secondary {
    color: var(--sage-dark); text-decoration: none;
    font-weight: 500; font-size: 0.95rem;
    display: flex; align-items: center; gap: 8px;
    transition: gap 0.2s;
  }
  .btn-secondary:hover { gap: 12px; }
  .hero-right {
    position: relative; z-index: 2;
    display: flex; flex-direction: column; align-items: center; gap: 24px;
  }
  .hero-visual {
    width: 100%; max-width: 420px;
    background: linear-gradient(135deg, var(--sage-light) 0%, var(--sage) 100%);
    border-radius: 32px 32px 80px 32px;
    padding: 60px 40px;
    display: flex; flex-direction: column; align-items: center;
    position: relative; overflow: hidden;
  }
  .hero-visual::before {
    content: '';
    position: absolute; top: -40px; right: -40px;
    width: 200px; height: 200px; border-radius: 50%;
    background: rgba(255,255,255,0.1);
  }
  .hero-icon { font-size: 5rem; margin-bottom: 20px; }
  .hero-visual h3 {
    font-family: 'Playfair Display', serif;
    color: var(--white); font-size: 1.6rem; text-align: center;
    margin-bottom: 12px;
  }
  .hero-visual p { color: rgba(255,255,255,0.85); text-align: center; font-size: 0.9rem; line-height: 1.6; }
  .hero-stats {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 12px; width: 100%; max-width: 420px;
  }
  .stat-card {
    background: var(--white); border-radius: 16px;
    padding: 20px; text-align: center;
    box-shadow: 0 2px 20px rgba(0,0,0,0.05);
  }
  .stat-number {
    font-family: 'Playfair Display', serif;
    font-size: 2rem; color: var(--sage-dark); font-weight: 700;
  }
  .stat-label { font-size: 0.78rem; color: var(--warm-gray); margin-top: 4px; }

  /* ABOUT */
  .section { padding: 100px 60px; }
  .section-tag {
    font-size: 0.75rem; letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--sage); font-weight: 500; margin-bottom: 14px;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 3.5vw, 3rem);
    line-height: 1.2; color: var(--charcoal); margin-bottom: 20px;
  }
  .section-title em { font-style: italic; color: var(--sage); }

  .about-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 80px; align-items: center;
  }
  .about-text p {
    color: var(--warm-gray); line-height: 1.8; font-weight: 300;
    font-size: 1rem; margin-bottom: 16px;
  }
  .about-features { margin-top: 32px; display: flex; flex-direction: column; gap: 14px; }
  .feature-item {
    display: flex; align-items: center; gap: 12px;
    font-size: 0.95rem; color: var(--charcoal);
  }
  .feature-dot {
    width: 8px; height: 8px; border-radius: 50%;
    background: var(--gold); flex-shrink: 0;
  }
  .about-visual {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
  .about-card {
    background: var(--white); border-radius: 20px;
    padding: 32px 24px; text-align: center;
    box-shadow: 0 4px 24px rgba(0,0,0,0.06);
    transition: transform 0.2s;
  }
  .about-card:hover { transform: translateY(-4px); }
  .about-card:first-child { grid-column: span 2; background: var(--sage-dark); }
  .about-card:first-child .card-title { color: var(--white); }
  .about-card:first-child .card-text { color: rgba(255,255,255,0.75); }
  .card-icon { font-size: 2rem; margin-bottom: 12px; }
  .card-title { font-family: 'Playfair Display', serif; font-size: 1.1rem; margin-bottom: 8px; }
  .card-text { font-size: 0.85rem; color: var(--warm-gray); line-height: 1.6; }

  /* INFO BAR */
  .info-bar {
    background: var(--charcoal); padding: 60px;
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 48px;
  }
  .info-item { text-align: center; }
  .info-icon { font-size: 1.8rem; margin-bottom: 12px; }
  .info-label {
    font-size: 0.72rem; letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--sage-light); margin-bottom: 8px;
  }
  .info-value { color: var(--white); font-size: 1rem; line-height: 1.6; }
  .info-value a { color: var(--gold); text-decoration: none; }
  .info-value a:hover { text-decoration: underline; }

  /* REVIEWS */
  .reviews-section { padding: 100px 60px; background: var(--white); }
  .reviews-header { text-align: center; margin-bottom: 60px; }
  .rating-display {
    display: flex; align-items: center; justify-content: center; gap: 12px;
    margin-bottom: 16px;
  }
  .stars { color: var(--gold); font-size: 1.4rem; letter-spacing: 2px; }
  .rating-num {
    font-family: 'Playfair Display', serif; font-size: 2.5rem;
    color: var(--charcoal);
  }
  .reviews-grid {
    columns: 3; gap: 24px;
  }
  .review-card {
    break-inside: avoid; background: var(--cream);
    border-radius: 20px; padding: 28px; margin-bottom: 24px;
    border: 1px solid rgba(122,158,135,0.1);
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .review-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 32px rgba(0,0,0,0.08);
  }
  .review-stars { color: var(--gold); font-size: 0.9rem; margin-bottom: 12px; }
  .review-text {
    font-size: 0.92rem; color: var(--charcoal); line-height: 1.7;
    margin-bottom: 16px; font-weight: 300;
  }
  .review-author { display: flex; align-items: center; gap: 12px; }
  .review-avatar {
    width: 38px; height: 38px; border-radius: 50%;
    background: linear-gradient(135deg, var(--sage-light), var(--sage));
    display: flex; align-items: center; justify-content: center;
    font-weight: 600; color: var(--white); font-size: 0.85rem; flex-shrink: 0;
  }
  .review-name { font-weight: 500; font-size: 0.88rem; color: var(--charcoal); }
  .review-date { font-size: 0.75rem; color: var(--warm-gray); margin-top: 2px; }

  /* CTA */
  .cta-section {
    padding: 100px 60px; text-align: center;
    background: linear-gradient(135deg, var(--sage-dark) 0%, var(--charcoal) 100%);
    position: relative; overflow: hidden;
  }
  .cta-section::before {
    content: '';
    position: absolute; top: -100px; left: 50%; transform: translateX(-50%);
    width: 600px; height: 600px; border-radius: 50%;
    background: rgba(255,255,255,0.04);
  }
  .cta-section .section-tag { color: var(--sage-light); }
  .cta-section .section-title { color: var(--white); }
  .cta-section .section-title em { color: var(--sage-light); }
  .cta-desc {
    color: rgba(255,255,255,0.7); max-width: 480px; margin: 0 auto 40px;
    line-height: 1.7; font-weight: 300;
  }
  .cta-actions { display: flex; gap: 16px; justify-content: center; align-items: center; }
  .btn-white {
    background: var(--white); color: var(--sage-dark);
    padding: 14px 32px; border-radius: 40px; text-decoration: none;
    font-weight: 600; font-size: 0.95rem; transition: all 0.2s;
  }
  .btn-white:hover { background: var(--cream); transform: translateY(-2px); }
  .btn-outline {
    border: 1px solid rgba(255,255,255,0.4); color: var(--white);
    padding: 14px 32px; border-radius: 40px; text-decoration: none;
    font-weight: 500; font-size: 0.95rem; transition: all 0.2s;
  }
  .btn-outline:hover { border-color: rgba(255,255,255,0.8); }

  /* FOOTER */
  footer {
    background: var(--charcoal); padding: 40px 60px;
    display: flex; align-items: center; justify-content: space-between;
    border-top: 1px solid rgba(255,255,255,0.06);
  }
  .footer-logo {
    font-family: 'Playfair Display', serif;
    color: var(--white); font-size: 1.2rem;
  }
  .footer-logo span { color: var(--gold); }
  .footer-text { color: var(--warm-gray); font-size: 0.82rem; }
  .footer-badge {
    display: flex; align-items: center; gap: 6px;
    color: var(--sage-light); font-size: 0.8rem;
  }

  /* ANIMATIONS */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .fade-up { animation: fadeUp 0.7s ease forwards; }
  .delay-1 { animation-delay: 0.1s; opacity: 0; }
  .delay-2 { animation-delay: 0.25s; opacity: 0; }
  .delay-3 { animation-delay: 0.4s; opacity: 0; }
  .delay-4 { animation-delay: 0.55s; opacity: 0; }

  @media (max-width: 900px) {
    nav { padding: 16px 24px; }
    .nav-links { display: none; }
    .hero { grid-template-columns: 1fr; padding: 100px 24px 60px; }
    .hero-right { display: none; }
    .section { padding: 70px 24px; }
    .about-grid { grid-template-columns: 1fr; gap: 40px; }
    .info-bar { padding: 40px 24px; grid-template-columns: 1fr; gap: 32px; }
    .reviews-section { padding: 70px 24px; }
    .reviews-grid { columns: 1; }
    .cta-section { padding: 70px 24px; }
    .cta-actions { flex-direction: column; }
    footer { flex-direction: column; gap: 16px; text-align: center; padding: 32px 24px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Last Touch<span>.</span></div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#reviews">Reviews</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="tel:4168368006" class="nav-cta">Call Us Now</a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-text">
    <div class="hero-badge fade-up">Serving Mississauga & the GTA</div>
    <h1 class="fade-up delay-1">Your home,<br><em>immaculately</em><br>cared for.</h1>
    <p class="hero-desc fade-up delay-2">Professional residential cleaning with a personal touch. We bring pride, precision, and passion to every home — so you come back to a space that truly sparkles.</p>
    <div class="hero-actions fade-up delay-3">
      <a href="tel:4168368006" class="btn-primary">📞 Book a Clean</a>
      <a href="#reviews" class="btn-secondary">Read Reviews →</a>
    </div>
  </div>
  <div class="hero-right fade-up delay-4">
    <div class="hero-visual">
      <div class="hero-icon">🏡</div>
      <h3>Available 24/7, Every Day</h3>
      <p>We work around your schedule — mornings, evenings, weekends. No job too big or small.</p>
    </div>
    <div class="hero-stats">
      <div class="stat-card">
        <div class="stat-number">2+</div>
        <div class="stat-label">Years of trust</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">5★</div>
        <div class="stat-label">Google rating</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">24h</div>
        <div class="stat-label">Availability</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">100%</div>
        <div class="stat-label">Reliable</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="section" id="about">
  <div class="about-grid">
    <div class="about-text">
      <p class="section-tag">Who We Are</p>
      <h2 class="section-title">More than a clean home — <em>a fresh start</em></h2>
      <p>Last Touch Inc. is a professional home cleaning company based in Mississauga, Ontario. Led by Corina, our team brings dedication, thoroughness, and genuine care to every single visit.</p>
      <p>We've been trusted by families across the GTA for years, and many of our clients have been with us for over two years — because once you experience the Last Touch difference, you won't want anyone else.</p>
      <div class="about-features">
        <div class="feature-item"><div class="feature-dot"></div>Punctual arrivals with helpful reminders</div>
        <div class="feature-item"><div class="feature-dot"></div>Attention to every corner and detail</div>
        <div class="feature-item"><div class="feature-dot"></div>Flexible, customized to your needs</div>
        <div class="feature-item"><div class="feature-dot"></div>Honest, hardworking, and trustworthy</div>
        <div class="feature-item"><div class="feature-dot"></div>Reasonable pricing for exceptional quality</div>
      </div>
    </div>
    <div class="about-visual">
      <div class="about-card">
        <div class="card-icon">✨</div>
        <div class="card-title">The Last Touch Promise</div>
        <div class="card-text" style="color:rgba(255,255,255,0.75)">We don't leave until every surface sparkles and every corner is cared for. Your satisfaction is our standard.</div>
      </div>
      <div class="about-card">
        <div class="card-icon">🕐</div>
        <div class="card-title">Always On Time</div>
        <div class="card-text">We respect your time — punctual arrivals and clear communication, every visit.</div>
      </div>
      <div class="about-card">
        <div class="card-icon">💚</div>
        <div class="card-title">Flexible Scheduling</div>
        <div class="card-text">Open 24 hours, 7 days a week. We adapt to what works for your life.</div>
      </div>
    </div>
  </div>
</section>

<!-- INFO BAR -->
<div class="info-bar" id="contact">
  <div class="info-item">
    <div class="info-icon">📍</div>
    <div class="info-label">Location</div>
    <div class="info-value">3145 Queen Frederica Dr<br>Mississauga, ON L4Y 3A7</div>
  </div>
  <div class="info-item">
    <div class="info-icon">📞</div>
    <div class="info-label">Phone</div>
    <div class="info-value"><a href="tel:4168368006">(416) 836-8006</a></div>
  </div>
  <div class="info-item">
    <div class="info-icon">🕐</div>
    <div class="info-label">Hours</div>
    <div class="info-value">Open 24 Hours<br>7 Days a Week</div>
  </div>
</div>

<!-- REVIEWS -->
<section class="reviews-section" id="reviews">
  <div class="reviews-header">
    <p class="section-tag">What Our Clients Say</p>
    <h2 class="section-title">Loved by every <em>household</em></h2>
    <div class="rating-display">
      <span class="stars">★★★★★</span>
      <span class="rating-num">5.0</span>
    </div>
    <p style="color:var(--warm-gray); font-size:0.9rem;">Based on Google Reviews</p>
  </div>

  <div class="reviews-grid">

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"I recently had my home cleaned and I couldn't be happier with the results! I can tell Corina takes pride in her work and goes above and beyond to make sure everything is done properly. I'll for sure be booking again!"</p>
      <div class="review-author">
        <div class="review-avatar">IR</div>
        <div><div class="review-name">Irina R.</div><div class="review-date">A week ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Corina was amazing! Left my place looking spotless and smelling fresh! She truly is the best, I would recommend her to all my friends and family."</p>
      <div class="review-author">
        <div class="review-avatar">RS</div>
        <div><div class="review-name">Rabeea Siddiqui</div><div class="review-date">4 months ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Corina does very thorough cleaning. She takes initiative, is punctual and sends helpful reminders to confirm her day and time of arrival. I highly recommend her."</p>
      <div class="review-author">
        <div class="review-avatar">DM</div>
        <div><div class="review-name">Deborah MacLean</div><div class="review-date">5 months ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Corina does an immaculate job in cleaning my house. It feels fresh and sparkling clean. She is very thorough and cleans every corner with care and attention and does an outstanding job. She also comes on time and is never late."</p>
      <div class="review-author">
        <div class="review-avatar">SE</div>
        <div><div class="review-name">Shellina Esmail</div><div class="review-date">6 months ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"I didn't understand what hiring a professional cleaner meant until I used Corina's services. My jaw dropped to the floor when I arrived home from work after her first visit. Corina's passion, dedication, and not to mention a spotless house, has secured her position in my household for the foreseeable future."</p>
      <div class="review-author">
        <div class="review-avatar">JA</div>
        <div><div class="review-name">Jason Archer</div><div class="review-date">A year ago · Local Guide</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"We have been using Corina's services for over 2 years and she always does an amazing job! She has great attention to detail and her prices are very reasonable considering how high the quality is."</p>
      <div class="review-author">
        <div class="review-avatar">SM</div>
        <div><div class="review-name">Serena MacLeod</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"We are using their cleaning services for our home for last 2+ years. They are the best in the industry. 100% reliable and hard working."</p>
      <div class="review-author">
        <div class="review-avatar">VS</div>
        <div><div class="review-name">Vasanth S.</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Very detail oriented and friendly. Very thorough and above expectations. Highly recommended to anyone."</p>
      <div class="review-author">
        <div class="review-avatar">RN</div>
        <div><div class="review-name">Rose Nesich</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"I strongly recommend their services. I'm very happy and will use them again. Very reliable. Thank you so much!"</p>
      <div class="review-author">
        <div class="review-avatar">LK</div>
        <div><div class="review-name">Lucia Kelly</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Corina is dedicated and committed to her job and executes meticulously. You know she's been there done that when you spot Corina's work which is spotless. I would recommend her to my contacts without a second thought."</p>
      <div class="review-author">
        <div class="review-avatar">SS</div>
        <div><div class="review-name">Sheeba Smith</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Corina did an incredible job cleaning our home! Every surface sparkled, the floors were spotless, and even the little details were taken care of. She even restored pots to look like new. Corina is professional, very thorough, and efficient."</p>
      <div class="review-author">
        <div class="review-avatar">HP</div>
        <div><div class="review-name">Holly Petersen</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Last touch services are reliable and thorough. I appreciate that the service is flexible and adapted to my needs. Highly recommend!"</p>
      <div class="review-author">
        <div class="review-avatar">Si</div>
        <div><div class="review-name">Siham Soufiani</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Corina is truly the best. She is so hardworking and caring that she became a part of the family. She sets a very high standard for cleanliness and organization that I have never seen before. You will not be disappointed!"</p>
      <div class="review-author">
        <div class="review-avatar">RM</div>
        <div><div class="review-name">Rola Mehio</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Corina has been keeping my house clean and tidy for the last year. She is honest hardworking and always willing to go the extra mile. I am fortunate to have found her."</p>
      <div class="review-author">
        <div class="review-avatar">Sh</div>
        <div><div class="review-name">Shahira Hafez</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"The best cleaning service out there.. always on time and leaves the house spotless! Great attention to details."</p>
      <div class="review-author">
        <div class="review-avatar">SQ</div>
        <div><div class="review-name">Suhail Qaddumi</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Excellent service... Why aren't all house cleaning services as efficient as this one? The cleaning I received to my home was incredible — better than I even hoped to expect."</p>
      <div class="review-author">
        <div class="review-avatar">MV</div>
        <div><div class="review-name">Marie Vella</div><div class="review-date">A year ago · Local Guide</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Last touch is great and professional!"</p>
      <div class="review-author">
        <div class="review-avatar">SN</div>
        <div><div class="review-name">Sheena Noud</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Spotless. I highly recommend. Very friendly and reliable owner."</p>
      <div class="review-author">
        <div class="review-avatar">GH</div>
        <div><div class="review-name">Gabriela Husu</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

    <div class="review-card">
      <div class="review-stars">★★★★★</div>
      <p class="review-text">"Excellent cleaning. Incredibly thorough and reliable."</p>
      <div class="review-author">
        <div class="review-avatar">DI</div>
        <div><div class="review-name">Donald Inglis</div><div class="review-date">A year ago</div></div>
      </div>
    </div>

  </div>
</section>

<!-- CTA -->
<section class="cta-section">
  <p class="section-tag">Ready to experience the difference?</p>
  <h2 class="section-title">Book your <em>first clean</em> today</h2>
  <p class="cta-desc">Available 24 hours a day, 7 days a week. Call us and we'll take care of the rest — so you can come home to a space that truly shines.</p>
  <div class="cta-actions">
    <a href="tel:4168368006" class="btn-white">📞 (416) 836-8006</a>
    <a href="https://maps.google.com/?q=3145+Queen+Frederica+Dr,+Mississauga,+ON+L4Y+3A7" target="_blank" class="btn-outline">Get Directions →</a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Last Touch<span>.</span> Inc.</div>
  <div class="footer-text">3145 Queen Frederica Dr, Mississauga, ON L4Y 3A7 · Ontario</div>
  <div class="footer-badge">✦ Open 24/7, Every Day</div>
</footer>

</body>
</html>
