<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Interactive Navigation Menu</title>
  <style>
    /* Base styling */
    body {
      margin: 0;
      font-family: Arial, sans-serif;
    }

    /* Fixed navbar */
    .navbar {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: transparent;
      padding: 15px 20px;
      display: flex;
      justify-content: space-around;
      align-items: center;
      transition: background-color 0.3s, box-shadow 0.3s;
      z-index: 1000;
    }

    .navbar.scrolled {
      background-color: #0d6efd;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

    .navbar a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      padding: 10px 15px;
      transition: color 0.3s, background-color 0.3s;
    }

    .navbar a:hover {
      background-color: white;
      color: #0d6efd;
      border-radius: 5px;
    }

    /* Dummy content for scrolling */
    .content {
      margin-top: 80px;
      padding: 20px;
      height: 2000px;
      background: linear-gradient(white, lightgray);
    }
  </style>
</head>
<body>

  <!-- Navigation Bar -->
  <div class="navbar" id="navbar">
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Services</a>
    <a href="#">Contact</a>
  </div>

  <!-- Page Content -->
  <div class="content">
    <h1>Welcome to the Page</h1>
    <p>Scroll down to see the navigation bar change color.</p>
  </div>

  <!-- JavaScript for Scroll Effect -->
  <script>
    window.addEventListener('scroll', function () {
      const navbar = document.getElementById('navbar');
      if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
      } else {
        navbar.classList.remove('scrolled');
      }
    });
  </script>

</body>
</html>
