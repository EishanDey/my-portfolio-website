# my-portfolio-website
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Your Name - Portfolio</title>
  <style>
    :root {
      --bg: #f4f4f9;
      --text: #333;
      --header-bg: #1e1e2f;
      --header-text: #fff;
    }

    body.dark-mode {
      --bg: #1e1e2f;
      --text: #f4f4f9;
      --header-bg: #12121c;
      --header-text: #ffffff;
    }

    * {
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background-color: var(--bg);
      color: var(--text);
      transition: background-color 0.3s, color 0.3s;
    }

    header {
      background-color: var(--header-bg);
      color: var(--header-text);
      padding: 40px 20px;
      text-align: center;
      position: relative;
    }

    .toggle-btn {
      position: absolute;
      top: 20px;
      right: 20px;
      background: none;
      border: 1px solid var(--header-text);
      color: var(--header-text);
      padding: 5px 10px;
      cursor: pointer;
    }

    main {
      max-width: 900px;
      margin: 20px auto;
      padding: 0 20px;
    }

    section {
      margin-bottom: 40px;
    }

    h2 {
      border-bottom: 2px solid #444;
      padding-bottom: 5px;
    }

    ul {
      list-style-type: disc;
      padding-left: 20px;
    }

    footer {
      background-color: var(--header-bg);
      color: var(--header-text);
      text-align: center;
      padding: 10px 0;
    }

    /* Interactive styles */
    .collapsible {
      background-color: #ddd;
      color: #333;
      cursor: pointer;
      padding: 10px;
      width: 100%;
      border: none;
      text-align: left;
      font-size: 16px;
      transition: 0.3s;
    }

    .content {
      display: none;
      padding: 10px 20px;
      background-color: #eee;
    }

    #backToTop {
      position: fixed;
      bottom: 30px;
      right: 30px;
      display: none;
      background-color: #444;
      color: #fff;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    form input, form textarea {
      width: 100%;
      padding: 10px;
      border: 1px solid #aaa;
      border-radius: 5px;
      font-size: 16px;
    }

    form button {
      background-color: #1e1e2f;
      color: #fff;
      border: none;
      padding: 10px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
    }

    form button:hover {
      background-color: #444;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 24px;
      }
      header p {
        font-size: 14px;
      }
      .toggle-btn {
        top: 10px;
        right: 10px;
        padding: 4px 8px;
        font-size: 14px;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Eishan Dey's Portfolio</h1>
    <p>Aspiring Astrophysicist | Student | Athlete | Future Scientist</p>
    <button class="toggle-btn" onclick="toggleTheme()">Toggle Theme</button>
  </header>

  <main>
    <section id="about">
      <h2>About Me</h2>
      <p>Hello! I'm a passionate student with a strong interest in astrophysics and space exploration. I aim to pursue a career in scientific research to explore the mysteries of the universe.</p>
    </section>

    <section id="awards">
      <h2>Awards & Achievements</h2>
      <button class="collapsible">Show/Hide Awards</button>
      <div class="content">
        <ul>
          <li>Selected for Bangladesh Physics Olympiad (BDPHO) nationals 2024 </li>
          <li>Second Runner Up in Bangladesh Biology Olympiad (BDBO) regionals 2024 </li>
          <li>Three time consecutive winner of CIDER International School Inter-School Tournament (CIFT) (2022-2024)</li>           
          <li>Captained CIDER International School's under-15 football team in winning Runner Up trophy of Chittagong Grammar School Futsal Tournament</li>
        </ul>
      </div>
    </section>

    <section id="contact">
      <h2>Contact Me</h2>
      <form action="https://formspree.io/f/mvgqozdr" method="POST">
        <input type="text" name="name" placeholder="Your Name" required />
        <input type="email" name="_replyto" placeholder="Your Email" required />
        <textarea name="message" rows="4" placeholder="Your Message" required></textarea>
        <button type="submit">Send</button>
      </form>
    </section>
  </main>

  <footer>
    <p>© 2025 Eishan Dey | Contact: eishandey10@gmail.com</p>
  </footer>

  <button id="backToTop" onclick="window.scrollTo({ top: 0, behavior: 'smooth' });">↑ Top</button>

  <script>
    // Collapsible content
    document.querySelector('.collapsible').addEventListener('click', function () {
      const content = this.nextElementSibling;
      content.style.display = content.style.display === 'block' ? 'none' : 'block';
    });

    // Theme toggle
    function toggleTheme() {
      document.body.classList.toggle('dark-mode');
    }

    // Back to top
    const backToTopBtn = document.getElementById('backToTop');
    window.onscroll = () => {
      backToTopBtn.style.display = window.scrollY > 200 ? 'block' : 'none';
    };
  </script>
</body>
</html>
