# Anatomy-lab
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Anatomy Lab with Amen</title>
  <style>
    :root {
      --bg-color: #ffffff;
      --text-color: #000000;
      --nav-bg: #f0f0f0;
    }

    [data-theme="dark"] {
      --bg-color: #121212;
      --text-color: #f5f5f5;
      --nav-bg: #1e1e1e;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: var(--bg-color);
      color: var(--text-color);
      transition: background 0.3s, color 0.3s;
    }

    nav {
      background-color: var(--nav-bg);
      padding: 10px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    nav a {
      margin: 0 10px;
      color: var(--text-color);
      text-decoration: none;
    }

    .toggle-btn {
      background: none;
      border: 1px solid var(--text-color);
      color: var(--text-color);
      padding: 5px 10px;
      cursor: pointer;
      border-radius: 5px;
    }

    section {
      padding: 20px;
    }

    iframe {
      width: 100%;
      height: 500px;
      border: none;
    }
  </style>
</head>
<body data-theme="light">

  <nav>
    <div><strong>Anatomy Lab with Amen</strong></div>
    <div>
      <a href="#intro">Intro</a>
      <a href="#viewer">3D Viewer</a>
      <a href="#info">Organs</a>
      <a href="#contact">Contact</a>
      <button class="toggle-btn" onclick="toggleTheme()">🌓 Mode</button>
    </div>
  </nav>

  <section id="intro">
    <h2>Welcome to Anatomy Lab</h2>
    <p>This website helps you explore the human body in 3D, with clear explanations and visuals. Perfect for students and curious minds.</p>
  </section>

  <section id="viewer">
    <h2>3D Human Viewer</h2>
    <!-- We'll embed a 3D anatomy model here -->
    <iframe src="https://human.biodigital.com/embed?be=1&ui-info=false&ui-tools=false" allowfullscreen></iframe>
  </section>

  <section id="info">
    <h2>Explore Body Systems</h2>
    <p>Detailed information about the brain, heart, lungs, and more will go here with images and videos.</p>
    <!-- Add images/videos later -->
  </section>

  <section id="contact">
    <h2>Contact / Feedback</h2>
    <form>
      <label>Name:</label><br>
      <input type="text" name="name" /><br><br>
      <label>Message:</label><br>
      <textarea name="message" rows="4" cols="40"></textarea><br><br>
      <button type="submit">Send</button>
    </form>
  </section>

  <script>
    function toggleTheme() {
      const body = document.body;
      body.dataset.theme = body.dataset.theme === "light" ? "dark" : "light";
    }
  </script>

</body>
</html>
