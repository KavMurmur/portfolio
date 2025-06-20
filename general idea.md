<!-- Folder Structure -->
.
├── index.html            # Welcome page with logo
├── about.html
├── contact.html
├── portfolio/
│   ├── index.html        # Main gallery
│   ├── portraits.html
│   ├── music.html
│   └── editorial.html
├── assets/
│   ├── css/style.css
│   └── images/
│       ├── logo.png
│       ├── portraits/
│       ├── music/
│       └── editorial/
├── _includes/
│   ├── header.html
│   ├── footer.html
└── netlify.toml          # if deploying via Netlify

<!-- index.html (Welcome page) -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Welcome</title>
    <link rel="stylesheet" href="assets/css/style.css" />
  </head>
  <body class="welcome">
    <div class="logo-container">
      <a href="portfolio/index.html">
        <img src="assets/images/logo.png" alt="Logo" class="logo" />
      </a>
    </div>
  </body>
</html>

<!-- portfolio/index.html (Main Gallery) -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Portfolio</title>
    <link rel="stylesheet" href="../assets/css/style.css" />
  </head>
  <body>
    <header>
      <nav>
        <a href="../index.html">Home</a>
        <a href="../about.html">About</a>
        <a href="../contact.html">Contact</a>
      </nav>
    </header>
    <main class="gallery">
      <h1>Portfolio</h1>
      <div class="gallery-grid">
        <a href="portraits.html">Portraits</a>
        <a href="music.html">Music</a>
        <a href="editorial.html">Editorial</a>
      </div>
    </main>
  </body>
</html>

<!-- contact.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Contact</title>
    <link rel="stylesheet" href="assets/css/style.css" />
  </head>
  <body>
    <main>
      <h1>Contact</h1>
      <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
        <input type="email" name="email" placeholder="Your email" required />
        <textarea name="message" placeholder="Your message" required></textarea>
        <button type="submit">Send</button>
      </form>
    </main>
  </body>
</html>

<!-- assets/css/style.css -->
body {
  font-family: sans-serif;
  margin: 0;
  background: #fafafa;
  color: #333;
}
.logo-container {
  display: flex;
  height: 100vh;
  justify-content: center;
  align-items: center;
}
.logo {
  max-width: 300px;
}
nav a {
  margin-right: 1rem;
  text-decoration: none;
  color: #333;
}
.gallery-grid a {
  display: block;
  margin: 1rem 0;
  font-size: 1.5rem;
}
form {
  display: flex;
  flex-direction: column;
  max-width: 500px;
  margin: 2rem auto;
}
input, textarea {
  margin-bottom: 1rem;
  padding: 0.5rem;
  font-size: 1rem;
}
button {
  padding: 0.75rem;
  background: #000;
  color: #fff;
  border: none;
  cursor: pointer;
}

