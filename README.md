# Otaku_Media
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>VideoStream - Your Content Platform</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0f0f0f;
      color: #ffffff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      overflow-x: hidden;
    }

    /* Navigation */
    nav {
      background: linear-gradient(180deg, rgba(0,0,0,0.8) 0%, transparent 100%);
      padding: 20px 50px;
      position: sticky;
      top: 0;
      z-index: 100;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 28px;
      font-weight: bold;
      color: #e50914;
      letter-spacing: 2px;
    }

    .nav-links {
      display: flex;
      gap: 30px;
      list-style: none;
    }

    .nav-links a {
      color: #ffffff;
      text-decoration: none;
      font-size: 14px;
      transition: color 0.3s;
    }

    .nav-links a:hover {
      color: #e50914;
    }

    /* Hero Section */
    .hero {
      height: 500px;
      background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
      display: flex;
      align-items: center;
      padding: 0 50px;
      margin-bottom: 60px;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      right: 0;
      top: 0;
      width: 400px;
      height: 100%;
      background: linear-gradient(135deg, rgba(229, 9, 20, 0.1), rgba(229, 9, 20, 0.3));
      border-radius: 100px 0 0 100px;
    }

    .hero-content {
      position: relative;
      z-index: 10;
      max-width: 600px;
    }

    .hero h1 {
      font-size: 56px;
      margin-bottom: 20px;
      font-weight: 700;
      line-height: 1.1;
    }

    .hero p {
      font-size: 16px;
      color: #b3b3b3;
      margin-bottom: 30px;
      line-height: 1.6;
    }

    .cta-buttons {
      display: flex;
      gap: 15px;
    }

    .btn {
      padding: 12px 30px;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s;
    }

    .btn-primary {
      background: #e50914;
      color: white;
    }

    .btn-primary:hover {
      background: #f40812;
      transform: scale(1.05);
    }

    .btn-secondary {
      background: rgba(255, 255, 255, 0.2);
      color: white;
      border: 2px solid #ffffff;
    }

    .btn-secondary:hover {
      background: rgba(255, 255, 255, 0.3);
    }

    /* Section Title */
    .section-title {
      font-size: 28px;
      font-weight: 700;
      margin: 60px 0 30px 50px;
      letter-spacing: 1px;
    }

    /* Video Grid */
    .video-container {
      padding: 0 50px;
      margin-bottom: 80px;
    }

    .video-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 20px;
    }

    .video-card {
      position: relative;
      cursor: pointer;
      border-radius: 8px;
      overflow: hidden;
      background: #1a1a1a;
      border: 1px solid #333333;
      transition: transform 0.3s, box-shadow 0.3s;
      height: 300px;
    }

    .video-card:hover {
      transform: scale(1.05) translateY(-10px);
      box-shadow: 0 15px 40px rgba(229, 9, 20, 0.3);
    }

    .video-thumbnail {
      width: 100%;
      height: 70%;
      background: linear-gradient(135deg, #2d2d2d, #1a1a1a);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 50px;
      color: #e50914;
      border-bottom: 3px solid #e50914;
    }

    .video-info {
      padding: 15px;
      height: 30%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .video-title {
      font-size: 14px;
      font-weight: 600;
      margin-bottom: 8px;
      line-height: 1.3;
    }

    .video-meta {
      font-size: 12px;
      color: #b3b3b3;
    }

    .video-card:hover .video-meta {
      color: #e50914;
    }

    /* Featured Section */
    .featured-section {
      padding: 0 50px;
      margin-bottom: 80px;
      background: linear-gradient(to right, rgba(229, 9, 20, 0.1), transparent);
      padding: 40px 50px;
      border-left: 4px solid #e50914;
      border-radius: 5px;
    }

    .featured-title {
      font-size: 24px;
      font-weight: 700;
      margin-bottom: 15px;
    }

    .featured-desc {
      color: #b3b3b3;
      font-size: 14px;
      margin-bottom: 20px;
    }

    /* Monetag Integration Note */
    .monetag-placeholder {
      background: rgba(229, 9, 20, 0.1);
      border: 2px dashed #e50914;
      border-radius: 8px;
      padding: 30px;
      text-align: center;
      color: #b3b3b3;
      margin: 20px 0;
      font-size: 14px;
    }

    /* Footer */
    footer {
      background: #0a0a0a;
      padding: 50px;
      text-align: center;
      color: #666666;
      border-top: 1px solid #333333;
      margin-top: 100px;
    }

    footer p {
      margin: 10px 0;
      font-size: 14px;
    }

    .footer-links {
      display: flex;
      justify-content: center;
      gap: 30px;
      margin-top: 20px;
      flex-wrap: wrap;
    }

    .footer-links a {
      color: #666666;
      text-decoration: none;
      transition: color 0.3s;
    }

    .footer-links a:hover {
      color: #e50914;
    }

    /* Responsive */
    @media (max-width: 1024px) {
      .video-grid {
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        gap: 15px;
      }
      
      nav, .hero, .section-title, .video-container, .featured-section, footer {
        padding-left: 30px;
        padding-right: 30px;
      }

      .hero {
        height: 400px;
      }

      .hero h1 {
        font-size: 42px;
      }
    }

    @media (max-width: 640px) {
      nav {
        padding: 15px 20px;
      }

      .logo {
        font-size: 20px;
      }

      .nav-links {
        gap: 15px;
        font-size: 12px;
      }

      .hero {
        height: 300px;
        padding: 0 20px;
        margin-bottom: 40px;
      }

      .hero h1 {
        font-size: 32px;
      }

      .hero p {
        font-size: 14px;
      }

      .cta-buttons {
        flex-direction: column;
      }

      .section-title {
        margin-left: 20px;
        font-size: 20px;
      }

      .video-container, .featured-section, footer {
        padding-left: 20px;
        padding-right: 20px;
      }

      .video-grid {
        grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
        gap: 10px;
      }

      .video-card {
        height: 220px;
      }

      .video-title {
        font-size: 12px;
      }

      .video-meta {
        font-size: 11px;
      }
    }
  </style>
</head>
<body>
  <!-- Navigation -->
  <nav>
    <div class="logo">VIDEOSTREAM</div>
    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#trending">Trending</a></li>
      <li><a href="#categories">Categories</a></li>
      <li><a href="#my-list">My List</a></li>
    </ul>
  </nav>

  <!-- Hero Section -->
  <section class="hero">
    <div class="hero-content">
      <h1>Start Your Video Journey</h1>
      <p>Upload your content, build your audience, and earn with Monetag. Join thousands of creators making money from their videos.</p>
      <div class="cta-buttons">
        <button class="btn btn-primary">Start Uploading</button>
        <button class="btn btn-secondary">Learn More</button>
      </div>
    </div>
  </section>

  <!-- Featured Content -->
  <section class="featured-section">
    <h2 class="featured-title">🎬 How It Works</h2>
    <p class="featured-desc">Create → Upload → Monetize. Earn revenue from views with Monetag's video monetization platform.</p>
    <div class="monetag-placeholder">
      📍 Monetag Integration Point: Replace this with your Monetag video player embed code
    </div>
  </section>

  <!-- Trending Videos -->
  <section class="video-container">
    <h2 class="section-title">🔥 Trending Now</h2>
    <div class="video-grid">
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Sample Video 1</h3>
          <p class="video-meta">2.5M views • 2 days ago</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Sample Video 2</h3>
          <p class="video-meta">1.8M views • 3 days ago</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Sample Video 3</h3>
          <p class="video-meta">3.2M views • 1 week ago</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Sample Video 4</h3>
          <p class="video-meta">890K views • 5 days ago</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Sample Video 5</h3>
          <p class="video-meta">1.5M views • 1 week ago</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Sample Video 6</h3>
          <p class="video-meta">920K views • 4 days ago</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Popular Category -->
  <section class="video-container">
    <h2 class="section-title">⭐ Most Popular</h2>
    <div class="video-grid">
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Popular 1</h3>
          <p class="video-meta">5.2M views</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Popular 2</h3>
          <p class="video-meta">4.8M views</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Popular 3</h3>
          <p class="video-meta">4.1M views</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Popular 4</h3>
          <p class="video-meta">3.9M views</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Popular 5</h3>
          <p class="video-meta">3.6M views</p>
        </div>
      </div>
      <div class="video-card">
        <div class="video-thumbnail">▶</div>
        <div class="video-info">
          <h3 class="video-title">Popular 6</h3>
          <p class="video-meta">3.4M views</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2024 VideoStream. All rights reserved.</p>
    <p>Powered by Monetag</p>
    <div class="footer-links">
      <a href="#privacy">Privacy Policy</a>
      <a href="#terms">Terms of Service</a>
      <a href="#contact">Contact Us</a>
      <a href="#monetag">Monetag Creator Portal</a>
    </div>
  </footer>

  <script>
    // Add interactivity
    const videoCards = document.querySelectorAll('.video-card');
    videoCards.forEach(card => {
      card.addEventListener('click', function() {
        alert('Click here to play the video in a Monetag player with ads');
      });
    });

    // Smooth scroll for nav links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if(target) {
          target.scrollIntoView({ behavior: 'smooth' });
        }
      });
    });
  </script>
</body>
</html>
