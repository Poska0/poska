<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Wassim's Gaming Profile - Your ultimate destination for gaming news, streams, and updates.">
  <meta name="keywords" content="gaming, Wassim, Albion Online, GTA 5, A Way Out, streams, news">
  <meta property="og:title" content="Wassim - Gaming Profile">
  <meta property="og:description" content="Your ultimate destination for gaming news, streams, and updates.">
  <meta property="og:image" content="https://media.discordapp.net/attachments/947231675702714448/1353174480532541561/download.jpeg">
  <meta property="og:url" content="https://yourwebsite.com">
  <link rel="canonical" href="https://yourwebsite.com">
  <title>Wassim - Gaming Profile</title>
  <style>
    /* CSS Variables */
    :root {
      --primary-color: #FF0000;
      --secondary-color: #8A2BE2;
      --background-color: #1a1a1a;
      --text-color: #ffffff;
    }

    /* Basic Styling */
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      color: var(--text-color);
      text-align: center;
      overflow-x: hidden;
      background-image: url('https://images.unsplash.com/photo-1547658718-1cdaa0852790?q=80&w=1964&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
      background-size: cover;
      background-position: center;
    }

    /* Smooth Scrolling */
    html {
      scroll-behavior: smooth;
    }

    /* Opening Animation */
    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(-20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .hidden {
      opacity: 0;
    }

    .visible {
      animation: fadeIn 1.5s ease-out forwards;
    }

    /* Logo Animation */
    @keyframes logoExpand {
      0% {
        transform: scale(1);
        opacity: 1;
      }
      50% {
        transform: scale(5);
        opacity: 0;
      }
      100% {
        transform: scale(1);
        opacity: 1;
      }
    }

    .logo-animation {
      animation: logoExpand 2s ease-in-out forwards;
    }

    /* Logo Container */
    #logo-animation-container {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('https://t4.ftcdn.net/jpg/04/09/70/87/240_F_409708782_HxuxOH8f7xSmj5p4ygbAbuJE74vGGj2N.jpg') no-repeat center center/cover;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      z-index: 10000;
      cursor: pointer;
    }

    #logo-animation-container img {
      width: 150px;
      border-radius: 50%;
    }

    #logo-animation-container h2 {
      margin-top: 10px;
      font-size: 24px;
      color: var(--text-color);
    }

    /* Hero Section */
    .hero {
      height: 100vh;
      background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7));
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
    }

    .hero h1 {
      font-size: 64px;
      margin: 0;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
    }

    .hero p {
      font-size: 24px;
      margin: 20px 0;
    }

    .hero .cta-button {
      padding: 15px 30px;
      background-color: var(--primary-color);
      color: var(--text-color);
      text-decoration: none;
      border-radius: 5px;
      font-size: 20px;
      transition: background-color 0.3s;
    }

    .hero .cta-button:hover {
      background-color: var(--secondary-color);
    }

    /* Navigation Bar */
    nav {
      position: sticky;
      top: 0;
      background-color: var(--background-color);
      padding: 10px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
    }

    nav .logo img {
      width: 150px;
      border-radius: 50%;
    }

    nav ul {
      list-style: none;
      margin: 0;
      padding: 0;
      display: flex;
    }

    nav ul li {
      margin: 0 15px;
    }

    nav ul li a {
      color: var(--text-color);
      text-decoration: none;
      font-size: 18px;
      transition: color 0.3s;
    }

    nav ul li a:hover {
      color: var(--primary-color);
    }

    /* Hamburger Menu for Mobile */
    @media (max-width: 768px) {
      nav ul {
        flex-direction: column;
        align-items: center;
        display: none;
      }
      nav ul.active {
        display: flex;
      }
      nav .menu-icon {
        display: block;
        font-size: 24px;
        cursor: pointer;
      }
    }

    /* About Me Section */
    .about {
      padding: 60px 20px;
      background-color: rgba(0, 0, 0, 0.7);
    }

    .about h2 {
      font-size: 48px;
      margin: 0 0 20px;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
    }

    .about p {
      font-size: 20px;
      margin: 0 0 30px;
      max-width: 800px;
      margin-left: auto;
      margin-right: auto;
    }

    /* News Section */
    .section {
      padding: 60px 20px;
      background-color: rgba(0, 0, 0, 0.7);
    }

    .section h2 {
      font-size: 48px;
      margin: 0 0 40px;
    }

    .news-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .news-card {
      background-color: #333;
      border-radius: 10px;
      overflow: hidden;
      transition: transform 0.3s;
    }

    .news-card:hover {
      transform: scale(1.05);
    }

    .news-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }

    .news-card h3 {
      font-size: 24px;
      margin: 20px;
    }

    .news-card p {
      font-size: 16px;
      margin: 0 20px 20px;
      color: #e0e0e0;
    }

    .news-card a {
      display: inline-block;
      margin: 20px;
      padding: 10px 20px;
      background-color: var(--primary-color);
      color: var(--text-color);
      text-decoration: none;
      border-radius: 5px;
      transition: background-color 0.3s;
    }

    .news-card a:hover {
      background-color: var(--secondary-color);
    }

    /* Footer */
    footer {
      background-color: var(--background-color);
      padding: 40px 20px;
    }

    footer .social-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-bottom: 20px;
    }

    footer .social-links a {
      color: var(--text-color);
      text-decoration: none;
      font-size: 24px;
      transition: color 0.3s;
    }

    footer .social-links a:hover {
      color: var(--primary-color);
    }

    footer p {
      margin: 0;
      font-size: 14px;
      color: #e0e0e0;
    }

    footer .back-to-top {
      display: inline-block;
      margin-top: 20px;
      padding: 10px 20px;
      background-color: var(--primary-color);
      color: var(--text-color);
      text-decoration: none;
      border-radius: 5px;
      transition: background-color 0.3s;
    }

    footer .back-to-top:hover {
      background-color: var(--secondary-color);
    }
  </style>
</head>
<body>
  <!-- Logo Animation Container -->
  <div id="logo-animation-container">
    <img id="logo-animation" src="https://media.discordapp.net/attachments/947231675702714448/1353174480532541561/download.jpeg?ex=67e0b170&is=67df5ff0&hm=55000e9153aecf0da8628c61c53d0831aea6cf6bf76761185a4745e467429e9b&=&format=webp&width=930&height=930" alt="Wassim's Logo">
    <h2>poska05</h2>
  </div>

  <!-- Navigation Bar -->
  <nav class="hidden">
    <div class="logo">
      <img src="https://media.discordapp.net/attachments/947231675702714448/1353174480532541561/download.jpeg?ex=67e0b170&is=67df5ff0&hm=55000e9153aecf0da8628c61c53d0831aea6cf6bf76761185a4745e467429e9b&=&format=webp&width=930&height=930" alt="Wassim's Logo">
    </div>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#news">News</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="menu-icon">&#9776;</div>
  </nav>

  <!-- Hero Section -->
  <section class="hero hidden" id="home">
    <h1>Welcome to Wassim Gaming</h1>
    <p>Your ultimate destination for gaming news, streams, and updates.</p>
    <a href="#news" class="cta-button">Explore News</a>
  </section>

  <!-- About Me Section -->
  <section class="about hidden" id="about">
    <h2>About Me</h2>
    <p>
      Hi! I'm Wassim, a passionate gamer who loves streaming my gaming adventures. I'm a pro at games like Albion Online, GTA 5 Enhanced, and A Way Out. Join me on my journey to become the best in the gaming world! I also share tips, strategies, and game updates on my platforms. Let's connect and have some fun!
    </p>
  </section>

  <!-- News Section -->
  <section class="section hidden" id="news">
    <h2>Latest News</h2>
    <div class="news-grid">
      <!-- News 1: Albion Online -->
      <div class="news-card">
        <img src="https://scontent.fmek1-1.fna.fbcdn.net/v/t39.30808-6/355663459_655254063315457_1703027218362747513_n.png?_nc_cat=108&ccb=1-7&_nc_sid=6ee11a&_nc_eui2=AeF3o3wk4H3nlAnhBO-hIVDHjqjFl5Y4m4iOqMWXljibiKzr6xz1hZ4q0aNYgIxgxIkUvJ2neL6dHp-geeOoATDJ&_nc_ohc=Rp1URLJsM90Q7kNvgGikQyI&_nc_oc=AdmWX9q10Vz36jhlGDhDtT9NKxzWL6ayILEekJ0zyM8W1uEuKvlxOcYs9U4Kg-phdwI&_nc_zt=23&_nc_ht=scontent.fmek1-1.fna&_nc_gid=oR7kAtuDaxh2TrYu2F81uA&oh=00_AYEexW6ZhVPLgAsJcLCVpkTBcgZfpL5xX9Ejtv1ZBqc7DA&oe=67E53284" alt="Albion Online">
        <h3>5 Years of Albion Online</h3>
        <p>I've been playing Albion Online for 5 years and have become a pro in PvP and guild leadership. Join me in this epic sandbox MMORPG!</p>
        <a href="https://noping.com/blog/en/control-trade-and-your-enemies-in-albion/" target="_blank">Learn More</a>
      </div>

      <!-- News 2: GTA 5 Enhanced -->
      <div class="news-card">
        <img src="https://cdn.cloudflare.steamstatic.com/steam/apps/3240220/header.jpg" alt="GTA 5 Enhanced">
        <h3>Mastering GTA 5 Enhanced</h3>
        <p>I'm currently dominating GTA 5 Enhanced with advanced strategies and mods. Watch my streams to learn how to become a pro!</p>
        <a href="https://twitch.tv/zodlac05" target="_blank">Watch Stream</a>
      </div>

      <!-- News 3: A Way Out on Kick -->
      <div class="news-card">
        <img src="https://cdn.cloudflare.steamstatic.com/steam/apps/1222700/header.jpg" alt="A Way Out">
        <h3>Playing A Way Out on Kick</h3>
        <p>Join me and my friends as we play A Way Out on my Kick channel. It's going to be a fun and chaotic co-op experience!</p>
        <a href="https://kick.com/poska0" target="_blank">Join Stream</a>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="hidden">
    <div class="social-links">
      <a href="https://discord.gg/CgjaFJgyBM" target="_blank" aria-label="Join our Discord community">Discord</a>
      <a href="https://instagram.com/wassimos._.amd" target="_blank" aria-label="Follow me on Instagram">Instagram</a>
      <a href="https://facebook.com/wassimos.amd" target="_blank" aria-label="Follow me on Facebook">Facebook</a>
      <a href="https://twitch.tv/zodlac05" target="_blank" aria-label="Watch my streams on Twitch">Twitch</a>
      <a href="https://kick.com/poska0" target="_blank" aria-label="Watch my streams on Kick">Kick</a>
      <a href="https://www.youtube.com/@poska05" target="_blank" aria-label="Subscribe to my YouTube channel">YouTube</a>
    </div>
    <a href="#home" class="back-to-top">Back to Top</a>
    <p>&copy; 2023 Wassim. All rights reserved. | <a href="/privacy-policy">Privacy Policy</a></p>
  </footer>

  <!-- JavaScript for Animation and Mobile Menu -->
  <script>
    let isRevealed = false;

    function revealElements() {
      if (isRevealed) return;
      isRevealed = true;
      const elements = document.querySelectorAll('.hidden');
      elements.forEach((element, index) => {
        setTimeout(() => {
          element.classList.toggle('visible');
        }, index * 200);
      });
    }

    document.getElementById('logo-animation-container').addEventListener('click', () => {
      document.getElementById('logo-animation-container').style.display = 'none';
      revealElements();
    });

    // Mobile Menu Toggle
    const menuIcon = document.querySelector('.menu-icon');
    const navUl = document.querySelector('nav ul');

    menuIcon.addEventListener('click', () => {
      navUl.classList.toggle('active');
    });
  </script>
</body>
</html>
