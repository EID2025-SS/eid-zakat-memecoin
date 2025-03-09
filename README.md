# eid-zakat-memecoin
"Website for EidMubarak ($EID) – A festive memecoin for Eid celebrations."
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EidMubarak ($EID) – Celebrate Eid with Crypto Joy!</title>
  <style>
    /* General Styles */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
      color: #333;
      line-height: 1.6;
    }

    .container {
      width: 90%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 20px;
    }

    /* Header */
    header {
      position: relative;
      height: 100vh; /* Full screen height */
      overflow: hidden;
    }

    #banner-video {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      z-index: -1;
    }

    .overlay {
      position: relative;
      z-index: 1;
      text-align: center;
      color: white;
      padding-top: 20%;
    }

    .logo {
      width: 100px;
      margin-bottom: 20px;
    }

    h1 {
      font-size: 3rem;
      margin: 0;
    }

    p {
      font-size: 1.2rem;
      margin: 10px 0 20px;
    }

    .cta-button {
      background: #e67e22;
      color: white;
      padding: 10px 20px;
      text-decoration: none;
      border-radius: 5px;
      font-size: 1.1rem;
    }

    .cta-button:hover {
      background: #d35400;
    }

    /* Sections */
    section {
      padding: 60px 0;
    }

    h2 {
      font-size: 2rem;
      margin-bottom: 20px;
      color: #2ecc71;
    }

    ul, ol {
      list-style: none;
      padding: 0;
    }

    ul li, ol li {
      background: #fff;
      margin: 10px 0;
      padding: 15px;
      border-radius: 5px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }

    ul li:hover, ol li:hover {
      transform: scale(1.05);
    }

    /* Footer */
    footer {
      background: #333;
      color: white;
      text-align: center;
      padding: 20px 0;
    }

    footer .social-links a {
      color: #e67e22;
      margin: 0 10px;
      text-decoration: none;
    }

    footer .social-links a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <!-- Hero Section -->
  <header>
    <div class="container">
      <video autoplay muted loop id="banner-video">
        <source src="images/animation.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <div class="overlay">
        <img src="images/logo.png" alt="EidMubarak Logo" class="logo">
        <h1>EidMubarak ($EID)</h1>
        <p>Celebrate Eid with Crypto Joy!</p>
        <a href="#how-to-buy" class="cta-button">Buy $EID Now</a>
      </div>
    </div>
  </header>

  <!-- About Section -->
  <section id="about">
    <div class="container">
      <h2>About $EID</h2>
      <p>$EID is a festive memecoin built on Solana, designed to bring joy, generosity, and financial blessings during Eid celebrations. Join us in making Eid more meaningful!</p>
    </div>
  </section>

  <!-- Tokenomics Section -->
  <section id="tokenomics">
    <div class="container">
      <h2>Tokenomics</h2>
      <ul>
        <li><strong>Total Supply:</strong> 1,000,000,000 $EID</li>
        <li><strong>50%:</strong> Public Sale</li>
        <li><strong>20%:</strong> Liquidity Pool</li>
        <li><strong>15%:</strong> Marketing</li>
        <li><strong>10%:</strong> Team (locked for 6-12 months)</li>
        <li><strong>5%:</strong> Charity Fund</li>
      </ul>
    </div>
  </section>

  <!-- Roadmap Section -->
  <section id="roadmap">
    <div class="container">
      <h2>Roadmap</h2>
      <ul>
        <li><strong>Phase 1:</strong> Launch and Awareness</li>
        <li><strong>Phase 2:</strong> Community Growth</li>
        <li><strong>Phase 3:</strong> Real-World Use</li>
        <li><strong>Phase 4:</strong> Long-Term Vision</li>
      </ul>
    </div>
  </section>

  <!-- How to Buy Section -->
  <section id="how-to-buy">
    <div class="container">
      <h2>How to Buy $EID</h2>
      <ol>
        <li>Download a Solana wallet (e.g., Phantom).</li>
        <li>Purchase SOL from an exchange.</li>
        <li>Swap SOL for $EID on Raydium or Orca.</li>
      </ol>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <p>&copy; 2024 EidMubarak ($EID). All rights reserved.</p>
      <div class="social-links">
        <a href="https://twitter.com/YOUR_TWITTER_HANDLE" target="_blank">Twitter</a>
        <a href="https://telegram.org" target="_blank">Telegram</a>
        <a href="https://discord.com" target="_blank">Discord</a>
      </div>
    </div>
  </footer>

  <!-- JavaScript for Countdown -->
  <script>
    // Countdown to Eid
    const eidDate = new Date("2024-06-16").getTime();

    const countdown = setInterval(() => {
      const now = new Date().getTime();
      const distance = eidDate - now;

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      document.getElementById("countdown").innerHTML = `${days} days until Eid!`;

      if (distance < 0) {
        clearInterval(countdown);
        document.getElementById("countdown").innerHTML = "Eid Mubarak!";
      }
    }, 1000);

    // Smooth Scrolling
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
          behavior: 'smooth'
        });
      });
    });
  </script>
</body>
</html>
