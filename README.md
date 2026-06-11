<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>Savindu Nawanjana · DevProfile</title>
  <!-- Google Fonts + Font Awesome 6 (free) -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- Animate.css CDN for subtle entrance animations -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(145deg, #0a0f1e 0%, #0c1222 100%);
      font-family: 'Inter', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 2rem 1.5rem;
    }

    /* Glassmorphic card container — resembles GitHub profile aesthetic */
    .readme-card {
      max-width: 1100px;
      width: 100%;
      background: rgba(18, 25, 45, 0.65);
      backdrop-filter: blur(12px);
      border-radius: 2.5rem;
      border: 1px solid rgba(72, 187, 255, 0.2);
      box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.5), 0 0 0 1px rgba(0, 255, 255, 0.05);
      overflow: hidden;
      transition: all 0.3s ease;
    }

    /* inner content padding */
    .profile-content {
      padding: 2.2rem 2rem 2.5rem;
    }

    /* header area with floating glow */
    .header-glow {
      text-align: center;
      margin-bottom: 1.2rem;
    }

    h1 {
      font-size: 2.8rem;
      font-weight: 700;
      background: linear-gradient(135deg, #E6F7FF, #7BC9FF, #2B9AFF);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      letter-spacing: -0.5px;
      display: inline-flex;
      align-items: center;
      gap: 12px;
      flex-wrap: wrap;
      justify-content: center;
    }

    h1 i {
      background: none;
      color: #3b9eff;
      font-size: 2.2rem;
      background-clip: unset;
      -webkit-background-clip: unset;
      text-shadow: 0 0 6px #2b9aff80;
    }

    .sub-badge {
      display: inline-flex;
      align-items: center;
      gap: 12px;
      background: rgba(0, 255, 255, 0.08);
      backdrop-filter: blur(4px);
      padding: 0.5rem 1.4rem;
      border-radius: 60px;
      margin-top: 12px;
      border: 1px solid rgba(43, 154, 255, 0.3);
    }

    .sub-badge h3 {
      font-weight: 500;
      font-size: 1.1rem;
      color: #c6e2ff;
    }

    .sub-badge i {
      font-size: 1.2rem;
      color: #ffd966;
    }

    /* view counter animation card */
    .stats-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      background: rgba(0, 0, 0, 0.35);
      border-radius: 2rem;
      padding: 0.7rem 1.5rem;
      margin: 1.8rem 0 1.5rem;
      backdrop-filter: blur(4px);
      gap: 15px;
    }

    .profile-views {
      display: flex;
      align-items: center;
      gap: 12px;
      background: #0f172ad9;
      padding: 6px 18px;
      border-radius: 40px;
      font-weight: 500;
    }

    .profile-views i {
      font-size: 1.4rem;
      color: #7bc9ff;
      animation: pulseIcon 1.8s infinite;
    }

    .profile-views span {
      color: #dbecff;
      font-size: 0.95rem;
    }

    .profile-views .count {
      font-weight: 700;
      color: white;
      background: #1e2a44;
      padding: 2px 10px;
      border-radius: 30px;
      margin-left: 5px;
      font-family: monospace;
      letter-spacing: 1px;
    }

    .fun-fact {
      background: linear-gradient(95deg, #1a263b, #101826);
      padding: 8px 18px;
      border-radius: 40px;
      color: #bcdeff;
      font-size: 0.85rem;
      font-weight: 500;
      border-left: 3px solid #2b9aff;
    }

    .fun-fact i {
      margin-right: 8px;
      color: #ffb347;
    }

    /* Contact & social section - modern grid */
    .connect-section {
      margin: 2rem 0 2rem;
    }

    .section-title {
      font-size: 1.4rem;
      font-weight: 600;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 12px;
      color: #eef5ff;
      border-left: 4px solid #2b9aff;
      padding-left: 1rem;
    }

    .social-links {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin-top: 0.8rem;
    }

    .social-card {
      background: rgba(21, 32, 58, 0.7);
      backdrop-filter: blur(4px);
      border-radius: 2rem;
      padding: 0.6rem 1.4rem;
      display: inline-flex;
      align-items: center;
      gap: 12px;
      transition: all 0.2s ease;
      border: 1px solid rgba(71, 147, 255, 0.2);
      text-decoration: none;
      color: #d6eaff;
      font-weight: 500;
      font-size: 0.9rem;
    }

    .social-card i {
      font-size: 1.5rem;
      transition: transform 0.2s;
    }

    .social-card:hover {
      background: #2b4b9e70;
      border-color: #2b9aff;
      transform: translateY(-3px);
      color: white;
      box-shadow: 0 10px 20px -8px #00000040;
    }

    .social-card:hover i {
      transform: scale(1.1);
    }

    /* Tool stack section - smooth icons animation */
    .tools-section {
      margin: 2rem 0 1.8rem;
    }

    .tech-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin-top: 1rem;
    }

    .tech-badge {
      background: #0e1629cc;
      backdrop-filter: blur(8px);
      border-radius: 60px;
      padding: 0.6rem 1.2rem;
      display: inline-flex;
      align-items: center;
      gap: 12px;
      font-size: 0.9rem;
      font-weight: 500;
      color: #cce6ff;
      transition: all 0.2s;
      border: 1px solid rgba(63, 165, 255, 0.3);
    }

    .tech-badge i, .tech-badge img {
      font-size: 1.4rem;
      width: 1.4rem;
      text-align: center;
    }

    .tech-badge img {
      filter: brightness(0) invert(1);
    }

    .tech-badge:hover {
      transform: scale(1.02) translateY(-2px);
      background: #1f2a48;
      border-color: #70b9ff;
      box-shadow: 0 8px 14px -8px #00000066;
    }

    /* animated footer / contact line */
    .contact-line {
      margin-top: 2.5rem;
      background: #050a15b3;
      border-radius: 2rem;
      padding: 0.8rem 1.4rem;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
    }

    .email-chip {
      display: flex;
      align-items: center;
      gap: 0.7rem;
      font-family: monospace;
      background: #00000055;
      padding: 5px 15px;
      border-radius: 60px;
      letter-spacing: 0.3px;
    }

    .email-chip i {
      color: #fcb43a;
    }

    .ask-badge {
      background: #2b9aff20;
      border-radius: 60px;
      padding: 5px 16px;
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    /* keyframe animations */
    @keyframes pulseIcon {
      0% { text-shadow: 0 0 0px #3b9eff; opacity: 0.8; transform: scale(1);}
      50% { text-shadow: 0 0 8px #3b9eff; opacity: 1; transform: scale(1.05);}
      100% { text-shadow: 0 0 0px #3b9eff; opacity: 0.8; transform: scale(1);}
    }

    /* responsive touches */
    @media (max-width: 680px) {
      .profile-content {
        padding: 1.5rem;
      }
      h1 {
        font-size: 1.9rem;
      }
      .tech-badge {
        padding: 0.4rem 1rem;
        font-size: 0.8rem;
      }
      .social-card {
        padding: 0.4rem 1rem;
      }
    }
  </style>
</head>
<body>
<div class="readme-card animate__animated animate__fadeInUp animate__fast">
  <div class="profile-content">

    <!-- header with waving hand icon & animated greeting -->
    <div class="header-glow">
      <h1>
        <i class="fas fa-code"></i> 
        Hi 👋, I'm Savindu Nawanjana
        <i class="fas fa-terminal"></i>
      </h1>
      <div class="sub-badge animate__animated animate__pulse animate__infinite infinite" style="animation-duration: 3s;">
        <i class="fas fa-globe-asia"></i>
        <h3>A passionate frontend developer from Sri Lanka 🇱🇰</h3>
        <i class="fas fa-laptop-code"></i>
      </div>
    </div>

    <!-- profile views + fun fact (animated count increment simulation) -->
    <div class="stats-row">
      <div class="profile-views">
        <i class="fas fa-eye"></i>
        <span>Profile views</span>
        <span class="count" id="viewCounter">2,481</span>
      </div>
      <div class="fun-fact">
        <i class="fas fa-lightbulb"></i> Fun fact: <strong>Savindu</strong> · caffeine + code = magic ✨
      </div>
    </div>

    <!-- Connect with me section - original social links with brand icons -->
    <div class="connect-section">
      <div class="section-title">
        <i class="fab fa-telegram-plane"></i> Connect with me
        <i class="fas fa-share-alt" style="font-size: 1rem; opacity: 0.7;"></i>
      </div>
      <div class="social-links">
        <a href="https://twitter.com/savindunaw25129" target="_blank" class="social-card"><i class="fab fa-twitter"></i> Twitter</a>
        <a href="https://linkedin.com/in/savindu-nawanjana-613584389" target="_blank" class="social-card"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
        <a href="https://fb.com/savindu.nawanjana.2025" target="_blank" class="social-card"><i class="fab fa-facebook-f"></i> Facebook</a>
        <a href="https://instagram.com/savindu_nawanjana_7" target="_blank" class="social-card"><i class="fab fa-instagram"></i> Instagram</a>
        <a href="https://youtube.com/@savindunawanjana-k7o?si=9tq44-rtklgffsj-" target="_blank" class="social-card"><i class="fab fa-youtube"></i> YouTube</a>
        <a href="https://www.hackerrank.com/savindunawanjan1" target="_blank" class="social-card"><i class="fab fa-hackerrank"></i> HackerRank</a>
      </div>
    </div>

    <!-- Languages & Tools with shimmering icons (official svg replacements with fontawesome & devicon style) -->
    <div class="tools-section">
      <div class="section-title">
        <i class="fas fa-cogs"></i> Languages & Tools
        <i class="fas fa-wrench" style="font-size: 1rem;"></i>
      </div>
      <div class="tech-grid">
        <!-- use exact original set : each icon using fontawesome or custom from devicon via font awesome brands/regular but to match we also include some custom svg appearance like figma, docker etc. All official style -->
        <span class="tech-badge"><i class="fab fa-bootstrap"></i> Bootstrap</span>
        <span class="tech-badge"><i class="fab fa-css3-alt"></i> CSS3</span>
        <span class="tech-badge"><i class="fab fa-docker"></i> Docker</span>
        <span class="tech-badge"><i class="fab fa-node-js"></i> Express</span>
        <span class="tech-badge"><i class="fab fa-figma"></i> Figma</span>
        <span class="tech-badge"><i class="fas fa-fire"></i> Firebase</span>
        <span class="tech-badge"><i class="fab fa-git-alt"></i> Git</span>
        <span class="tech-badge"><i class="fab fa-html5"></i> HTML5</span>
        <span class="tech-badge"><i class="fab fa-java"></i> Java</span>
        <span class="tech-badge"><i class="fab fa-js"></i> JavaScript</span>
        <span class="tech-badge"><i class="fab fa-linux"></i> Linux</span>
        <span class="tech-badge"><i class="fas fa-database"></i> MongoDB</span>
        <span class="tech-badge"><i class="fas fa-database"></i> MySQL</span>
        <span class="tech-badge"><i class="fab fa-node"></i> Node.js</span>
        <span class="tech-badge"><i class="fas fa-database"></i> PostgreSQL</span>
        <span class="tech-badge"><i class="fas fa-vial"></i> Postman</span>
        <span class="tech-badge"><i class="fab fa-python"></i> Python</span>
        <span class="tech-badge"><i class="fab fa-react"></i> React</span>
        <span class="tech-badge"><i class="fab fa-react"></i> React Native</span>
        <span class="tech-badge"><i class="fas fa-leaf"></i> Spring</span>
        <span class="tech-badge"><i class="fas fa-wind"></i> Tailwind</span>
        <span class="tech-badge"><i class="fab fa-js"></i> TypeScript</span>
      </div>
    </div>

    <!-- contact & ask me section exactly as original but animated -->
    <div class="contact-line">
      <div class="email-chip">
        <i class="far fa-envelope"></i>
        <span>savindunawanjana08@gmail.com</span>
        <i class="fas fa-long-arrow-alt-right"></i>
      </div>
      <div class="ask-badge">
        <i class="fas fa-comment-dots"></i> 💬 Ask me about <strong style="color:#7bc9ff; margin-left:6px;">Java</strong>
        <i class="fas fa-coffee"></i>
      </div>
    </div>

    <!-- Additional Dev quote: original content preserved, but with animated element! -->
    <div style="margin-top: 1.6rem; text-align: center; font-size: 0.75rem; opacity: 0.75; border-top: 1px dashed #2b4c7c; padding-top: 1rem;">
      <i class="fas fa-code-branch"></i>   Savindu Nawanjana · full‑stack enthusiast   <i class="fas fa-heart" style="color:#ff7070;"></i>
    </div>
  </div>
</div>

<!-- simple dynamic view counter increment simulation with developer touch (random increment upon visit, but realistic) -->
<script>
  (function() {
    // Retrieve or initialize view count using localStorage to simulate +1 per unique session
    // We will make it a nice animated increment effect similar to github profile views.
    let storedViews = localStorage.getItem('savindu_profile_views');
    let currentViews = 2481;  // base as given in mock komarev
    if(storedViews) {
      currentViews = parseInt(storedViews, 10);
      // simulate new visit: increment by 1 to 3 (showing dynamic growth)
      let increment = Math.floor(Math.random() * 2) + 1;  // +1 or +2
      currentViews += increment;
      localStorage.setItem('savindu_profile_views', currentViews);
    } else {
      // first time visit: add a small random increment
      currentViews = 2481 + Math.floor(Math.random() * 5);
      localStorage.setItem('savindu_profile_views', currentViews);
    }
    
    const viewSpan = document.getElementById('viewCounter');
    if(viewSpan) {
      // animated counter effect
      const oldValue = parseInt(viewSpan.innerText.replace(/,/g, '')) || 2481;
      const newValue = currentViews;
      let diff = newValue - oldValue;
      if(diff === 0) diff = 1;
      let step = diff > 0 ? Math.ceil(diff / 20) : 1;
      let currentDisplay = oldValue;
      const counterInterval = setInterval(() => {
        if((diff > 0 && currentDisplay >= newValue) || (diff < 0 && currentDisplay <= newValue)) {
          viewSpan.innerText = newValue.toLocaleString();
          clearInterval(counterInterval);
          return;
        }
        currentDisplay += step;
        if(currentDisplay > newValue) currentDisplay = newValue;
        viewSpan.innerText = currentDisplay.toLocaleString();
      }, 20);
    }
  })();

  // additional smooth hover tooltip for tech badges? not necessary, but adds subtle animation to stats row.
  // Also add dynamic year? no needed. But ensure email copy / links open correctly.
  // extra micro-interactions: badge bouncing on load
  const badges = document.querySelectorAll('.tech-badge');
  badges.forEach((badge, idx) => {
    badge.style.transition = 'all 0.2s cubic-bezier(0.2, 0.9, 0.4, 1.1)';
    badge.addEventListener('mouseenter', (e) => {
      badge.style.transform = 'translateY(-3px) scale(1.02)';
    });
    badge.addEventListener('mouseleave', () => {
      badge.style.transform = 'translateY(0px) scale(1)';
    });
  });
  
  // interactive floating effect on social cards
  const socials = document.querySelectorAll('.social-card');
  socials.forEach(s => {
    s.addEventListener('mouseenter', () => {
      s.style.transform = 'translateY(-4px)';
    });
    s.addEventListener('mouseleave', () => {
      s.style.transform = 'translateY(0px)';
    });
  });
  
  // console fun: developer greeting
  console.log("%c✨ Savindu Nawanjana's Dev Profile — built with style & animation ✨", "color: #2b9aff; font-size: 14px; font-weight: bold;");
  console.log("%c🔥 Frontend developer from Sri Lanka | ask me about Java", "color: #ffbd44; font-size: 12px;");
</script>
</body>
</html>
