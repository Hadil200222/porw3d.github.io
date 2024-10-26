<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      href="https://cdn.jsdelivr.net/npm/remixicon@3.2.0/fonts/remixicon.css"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>Web Design Mastery | Responsive Portfolio</title>
    <style>
        @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap");

:root {
  --primary-color: #a855f7;
  --primary-color-dark: #9333ea;
  --secondary-color: #ca8a04;
  --text-dark: #1f2937;
  --text-light: #6b7280;
  --extra-light: #faf5ff;
  --max-width: 1200px;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

a {
  text-decoration: none;
}

body {
  font-family: "Poppins", sans-serif;
}

nav {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background-color: #ffffff;
  z-index: 99;
}

.nav__content {
  max-width: var(--max-width);
  margin: auto;
  padding: 1.5rem 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

nav .logo a {
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--primary-color);
  transition: 0.3s;
}
nav .logo a:hover {
  color: var(--primary-color-dark);
}

nav .checkbox {
  display: none;
}

nav input {
  display: none;
}
nav .checkbox i {
  font-size: 2rem;
  color: var(--primary-color);
  cursor: pointer;
}

ul {
  display: flex;
  align-items: center;
  gap: 1rem;
  list-style: none;
  transition: left 0.3s;
}

ul li a {
  padding: 0.5rem 1rem;
  border: 2px solid transparent;
  text-decoration: none;
  font-weight: 600;
  color: var(--text-dark);
  transition: 0.3s;
}

ul li a:hover {
  border-top-color: var(--secondary-color);
  border-bottom-color: var(--secondary-color);
  color: var(--secondary-color);
}

.section {
  background-color: var(--extra-light);
}

.section__container {
  min-height: 100vh;
  max-width: var(--max-width);
  margin: auto;
  padding: 1rem;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 4rem;
}

.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.subtitle {
  letter-spacing: 2px;
  color: var(--text-light);
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.title {
  font-size: 2.5rem;
  font-weight: 400;
  line-height: 3rem;
  color: var(--text-dark);
  margin-bottom: 1rem;
}

.title span {
  font-weight: 600;
}

.description {
  line-height: 1.5rem;
  color: var(--text-light);
  margin-bottom: 2rem;
}

.action__btns {
  display: flex;
  gap: 1rem;
}

.action__btns button {
  font-size: 1rem;
  font-weight: 600;
  letter-spacing: 2px;
  padding: 1rem 2rem;
  outline: none;
  border: 2px solid var(--primary-color);
  border-radius: 10px;
  transition: 0.3s;
  cursor: pointer;
}

.hire__me {
  background-color: var(--primary-color);
  color: #ffffff;
}

.hire__me:hover {
  background-color: var(--primary-color-dark);
}

.portfolio {
  color: var(--primary-color);
}

.portfolio:hover {
  background-color: var(--primary-color-dark);
  color: #ffffff;
}

.btn {
  color: var(--primary-color);
}

.btn:hover {
  background-color: var(--primary-color-dark);
  color: #ffffff;
}


@media (width < 750px) {
  nav .checkbox {
    display: block;
  }

  ul {
    position: absolute;
    width: 100%;
    height: calc(100vh - 85px);
    left: -100%;
    top: 85px;
    background-color: var(--extra-light);
    flex-direction: column;
    justify-content: center;
    gap: 3rem;
  }

  nav #check:checked ~ ul {
    left: 0;
  }

  ul li a {
    font-size: 1.25rem;
  }

  .section__container {
    padding: 10rem 1rem 5rem 1rem;
    text-align: center;
    grid-template-columns: repeat(1, 1fr);
  }

  .action__btns {
    margin: auto;
  }

}

#skills .skills-container {
    display: flex;
    justify-content: center;
    gap: 20px;
    animation: fadeIn 1s ease forwards;
}

.skill {
    background-color: var(--primary-color-dark);
    color: white;
    padding: 15px 25px;
    border-radius: 5px;
    transition: transform 0.3s ease;
}

.skill:hover {
    transform: translateY(-10px);
}

#projects .project-item {
    background-color: white;
    margin: 20px auto;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    max-width: 500px;
    opacity: 0;
    transform: translateY(30px);
    animation: projectFadeIn 1s forwards;
}

@keyframes projectFadeIn {
    0% {
        opacity: 0;
        transform: translateY(30px);
    }
    100% {
        opacity: 1;
        transform: translateY(0);
    }
}

#projects .project-item a {
    color: #333;
    text-decoration: none;
    font-weight: bold;
}

#projects .project-item a:hover {
    text-decoration: underline;
}

form {
    display: flex;
    flex-direction: column;
}
input, textarea {
    margin: 10px 100px;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    height: 50px;
    width: 60rem;
}

.btn {
    margin: 10px 100px;
    padding: 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    height: 50px;
    width: 60rem;
}
footer {
    background-color: var(--extra-light);
    color: black;
    padding: 20px;
    text-align: center;
}

    </style>
  </head>
  <body>
    <nav>
      <div class="nav__content">
        <div class="logo"><a href="#">Hadil</a></div>
        <label for="check" class="checkbox">
          <i class="ri-menu-line"></i>
        </label>
        <input type="checkbox" name="check" id="check" />
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#skills">Scills</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>
    </nav>
    <section class="section">
      <div class="section__container">
        <div class="content">
          <p class="subtitle">HELLO</p>
          <h1 class="title">
            I'm <span>GUERIOUNE HADIL<br />a</span> Web Developer
          </h1>
          <p class="description">
            Welcome to my web developer portfolio! I'm Hadil, a skilled and
            creative web developer with a passion for creating beautiful,
            responsive, and user-friendly websites.
          </p>
          
          <div class="action__btns">
            <button class="hire__me">Hire Me</button>
            <button class="portfolio">Portfolio</button>
          </div>
          
        </div>
      </div>
    </section>
    <section id="skills">
        <h2 style="
            padding: 50px;
            text-align: center;
        ">Skills</h2>
        <div class="skills-container">
            <div class="skill">HTML</div>
            <div class="skill">CSS</div>
            <div class="skill">JavaScript</div>
        </div>
    </section>
    <section id="projects" style="
    padding: 50px;
    text-align: center;">
        <h2 style="
        padding: 50px;
        text-align: center;
    ">Projects</h2>
        <div class="project-item" style="background-color: var(--extra-light);">
            <h3>TP 01</h3>
            <p>Creating a scene with Blender.</p>
            <a href="https://drive.google.com/file/d/1ZXUVggzOENk3noXTE8ACYcmfQc9BXI1l/view?usp=sharing">View TP01</a>
        </div>
        <div class="project-item" style="background-color: var(--extra-light);">
            <h3>TP 02</h3>
            <p>.......</p>
            <a href="#">View TP02</a>
        </div>
    </section>
    <section id="contact">
        <h2 style="
        padding: 50px;
        text-align: center;
    ">Contact Me</h2>
        <form id="contactForm">
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="email" id="email" placeholder="Your Email" required>
            <textarea id="message" placeholder="Your Message" required></textarea>
            <button type="submit" class="btn">Send Message</button>
        </form>
        
    </section>
    <footer>
      <p>&copy; 2024 GUERIOUNE HADIL. Contact: hadil.guer@gmail.com</p>

  </footer>
  </body>
</html>
