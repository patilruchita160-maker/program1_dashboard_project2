# program1_dashboard_project2
This project is about building a modern, interactive navigation menu for websites. The goal is to make navigation user-friendly, responsive, and visually engaging.  ✨ Features  Responsive Design – Works seamlessly on desktop, tablet, and mobile.  Smooth Animations – Hover effects, transitions, or slide-in menus for a modern feel.  Intera
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Fixed Navigation Menu</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: Arial, sans-serif;
      min-height: 2000px;
      background: #28efdc;
    }

    
    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: #70de2b;
      color: #1c38c5;
      transition: all 0.3s ease;
      z-index: 1000;
      box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    }
    nav.scrolled {
      background: #ee0959b3;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    }
    .nav-container {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      padding: 0 20px;
      height: 60px;
    }
    .logo {
      font-size: 1.5rem;
      font-weight: bold;
      letter-spacing: 1px;
      color: #ef0c0c;
      margin-right: 40px;
    }
    ul.menu {
      display: flex;
      gap: 20px;
      list-style: none;
    }
    ul.menu li {
      padding: 0;
    }
    ul.menu li a {
      text-decoration: none;
      color: #f7f438;
      padding: 12px 14px;
      border-radius: 5px;
      transition: background 0.2s, color 0.2s;
      font-size: 1rem;
      position: relative;
    }
    ul.menu li a:hover {
      background: #d1b286;
      color: #222;
      font-weight: bold;
      box-shadow: 0 2px 8px rgba(0,0,0,0.07);
    }

    
    @media (max-width: 700px) {
      .nav-container {
        flex-direction: column;
        height: auto;
        padding: 10px 15px;
      }
      ul.menu {
        flex-direction: column;
        width: 100%;
        gap: 0;
      }
      ul.menu li a {
        display: block;
        width: 100%;
        margin: 2px 0;
      }
    }

    
    .content {
      margin-top: 80px;
      padding: 30px;
      max-width: 800px;
      margin-left: auto;
      margin-right: auto;
      background: #d67575;
      border-radius: 10px;
      box-shadow: 0 2px 16px rgba(0,0,0,0.07);
    }
  </style>
</head>
<body>
  <nav id="mainNav">
    <div class="nav-container">
      <span class="logo">MySite</span>
      <ul class="menu">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Features</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
  </nav>
  <div class="content">
    <h1>Welcome to MySite</h1>
    <p>Scroll this page to see the navigation menu change color! Hover over the menu items to see their styling change. This navigation bar is fixed so it stays visible as you move through the page. You can copy and use this snippet for your own website navigation!</p>
    <p>dolor sit amet, consectetur adipiscing elit. Pellentesque posuere, nisi eu laoreet porta, odio eros ultricies urna, nec eleifend purus nulla at ex. Duis euismod luctus purus, in imperdiet magna ullamcorper vitae.</p>
  </div>
  <script>
    
    window.addEventListener('scroll', function() {
      var nav = document.getElementById('mainNav');
      if(window.scrollY > 40) {
        nav.classList.add('scrolled');
      } else {
        nav.classList.remove('scrolled');
      }
    });
  </script>
</body>
</html>
