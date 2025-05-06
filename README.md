# week4-web-dev-assignment
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Flexbox Layout</title>
  <style>
    :root {
      --nav-bg: #2c3e50;
      --nav-text: #fff;
      --main-bg: #f4f4f4;
      --sidebar-bg: #ecf0f1;
      --gap: 1.5rem;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: var(--main-bg);
      color: #222;
    }

    /* Navigation Bar */
    nav {
      background: var(--nav-bg);
      color: var(--nav-text);
      padding: 1rem;
    }
    .navbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      max-width: 1200px;
      margin: 0 auto;
    }
    .nav-logo {
      font-weight: bold;
      font-size: 1.2rem;
    }
    .nav-links {
      display: flex;
      gap: 1rem;
    }
    .nav-links a {
      color: var(--nav-text);
      text-decoration: none;
      padding: 0.5rem 1rem;
      border-radius: 4px;
      transition: background 0.2s;
    }
    .nav-links a:hover {
      background: #34495e;
    }

    /* Main Layout */
    .container {
      display: flex;
      gap: var(--gap);
      max-width: 1200px;
      margin: 2rem auto;
      padding: 0 1rem;
    }
    main {
      flex: 2;
      background: #fff;
      padding: 1.5rem;
      border-radius: 8px;
      min-width: 0;
    }
    aside {
      flex: 1;
      background: var(--sidebar-bg);
      padding: 1.5rem;
      border-radius: 8px;
      min-width: 200px;
    }

    /* Responsive Styles */
    @media (max-width: 900px) {
      .container {
        flex-direction: column;
      }
      aside {
        margin-top: var(--gap);
        min-width: 0;
      }
    }

    @media (max-width: 600px) {
      .navbar {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.5rem;
      }
      .nav-links {
        flex-direction: column;
        width: 100%;
        gap: 0.5rem;
      }
      .container {
        padding: 0 0.5rem;
      }
      main, aside {
        padding: 1rem;
      }
    }
  </style>
</head>
<body>
  <nav>
    <div class="navbar">
      <div class="nav-logo">MySite</div>
      <div class="nav-links">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Services</a>
        <a href="#">Contact</a>
      </div>
    </div>
  </nav>

  <div class="container">
    <main>
      <h1>Welcome to My Responsive Site</h1>
      <p>
        This layout uses Flexbox and media queries to adapt to different screen sizes. Resize your browser to see the layout change for mobile, tablet, and desktop!
      </p>
    </main>
    <aside>
      <h2>Sidebar</h2>
      <p>
        Additional content or navigation can go here.
      </p>
    </aside>
  </div>
</body>
</html>
