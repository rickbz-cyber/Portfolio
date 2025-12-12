
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ricardo Bautista-Zapata Portfolio</title>
    <style>
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      body {
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
        line-height: 1.6;
        color: #333;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        min-height: 100vh;
      }

      .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 20px;
      }

      /* Header */
      header {
        background: rgba(255, 255, 255, 0.95);
        backdrop-filter: blur(10px);
        padding: 20px 0;
        position: sticky;
        top: 0;
        z-index: 100;
        box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
      }

      nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 20px;
      }

      .logo {
        font-size: 24px;
        font-weight: bold;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
      }

      .nav-links {
        display: flex;
        gap: 30px;
        list-style: none;
      }

      .nav-links a {
        text-decoration: none;
        color: #333;
        font-weight: 500;
        transition: color 0.3s;
      }

      .nav-links a:hover {
        color: #667eea;
      }

      /* Hero Section */
      .hero {
        text-align: center;
        padding: 100px 20px;
        color: white;
        animation: fadeIn 1s ease-in;
      }

      @keyframes fadeIn {
        from {
          opacity: 0;
          transform: translateY(20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      .hero h1 {
        font-size: 48px;
        margin-bottom: 20px;
        animation: slideDown 1s ease-out;
      }

      @keyframes slideDown {
        from {
          opacity: 0;
          transform: translateY(-30px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      .hero p {
        font-size: 20px;
        margin-bottom: 30px;
        opacity: 0.9;
      }

      .cta-button {
        display: inline-block;
        padding: 15px 40px;
        background: white;
        color: #667eea;
        text-decoration: none;
        border-radius: 30px;
        font-weight: bold;
        transition: transform 0.3s, box-shadow 0.3s;
        box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
      }

      .cta-button:hover {
        transform: translateY(-3px);
        box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3);
      }

      /* Section Styles */
      section {
        background: white;
        margin: 40px 0;
        padding: 60px 40px;
        border-radius: 20px;
        box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
        animation: fadeInUp 0.8s ease-out;
      }

      @keyframes fadeInUp {
        from {
          opacity: 0;
          transform: translateY(30px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }

      section h2 {
        font-size: 36px;
        margin-bottom: 30px;
        text-align: center;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
      }

      /* About Section */
      .about-content {
        max-width: 800px;
        margin: 0 auto;
        text-align: center;
        font-size: 18px;
        line-height: 1.8;
      }

      /* Skills Section */
      .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 30px;
        margin-top: 40px;
      }

      .skill-card {
        padding: 30px;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        border-radius: 15px;
        color: white;
        transition: transform 0.3s, box-shadow 0.3s;
        cursor: pointer;
      }

      .skill-card:hover {
        transform: translateY(-10px);
        box-shadow: 0 15px 40px rgba(102, 126, 234, 0.4);
      }

      .skill-card h3 {
        font-size: 24px;
        margin-bottom: 15px;
      }

      .skill-bar {
        background: rgba(255, 255, 255, 0.3);
        height: 10px;
        border-radius: 5px;
        overflow: hidden;
        margin-top: 15px;
      }

      .skill-progress {
        background: white;
        height: 100%;
        border-radius: 5px;
        transition: width 1s ease-out;
      }

      /* Projects Section */
      .projects-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
        margin-top: 40px;
      }

      .project-card {
        background: #f8f9fa;
        border-radius: 15px;
        overflow: hidden;
        transition: transform 0.3s, box-shadow 0.3s;
        cursor: pointer;
      }

      .project-card:hover {
        transform: translateY(-10px);
        box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
      }

      .project-image {
        width: 100%;
        height: 200px;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
        font-size: 48px;
      }

      .project-content {
        padding: 25px;
      }

      .project-content h3 {
        font-size: 22px;
        margin-bottom: 10px;
        color: #333;
      }

      .project-content p {
        color: #666;
        margin-bottom: 15px;
      }

      .project-tags {
        display: flex;
        gap: 10px;
        flex-wrap: wrap;
        margin-bottom: 15px;
      }

      .tag {
        padding: 5px 15px;
        background: #667eea;
        color: white;
        border-radius: 20px;
        font-size: 12px;
      }

      .project-link {
        display: inline-block;
        padding: 10px 25px;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        color: white;
        text-decoration: none;
        border-radius: 25px;
        font-weight: 600;
        transition: transform 0.3s, box-shadow 0.3s;
      }

      .project-link:hover {
        transform: translateY(-2px);
        box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
      }

      /* Contact Section */
      .contact-content {
        max-width: 800px;
        margin: 0 auto;
      }

      .contact-info-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 30px;
        margin-top: 40px;
      }

      .contact-card {
        padding: 30px;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        border-radius: 15px;
        color: white;
        text-align: center;
        transition: transform 0.3s, box-shadow 0.3s;
        cursor: pointer;
      }

      .contact-card:hover {
        transform: translateY(-10px);
        box-shadow: 0 15px 40px rgba(102, 126, 234, 0.4);
      }

      .contact-card-icon {
        font-size: 48px;
        margin-bottom: 15px;
      }

      .contact-card h3 {
        font-size: 20px;
        margin-bottom: 10px;
      }

      .contact-card p {
        font-size: 16px;
        opacity: 0.95;
        word-break: break-word;
      }

      .contact-card a {
        color: white;
        text-decoration: none;
      }

      .contact-card a:hover {
        text-decoration: underline;
      }

      /* Footer */
      footer {
        text-align: center;
        padding: 40px 20px;
        color: white;
      }

      .social-links {
        display: flex;
        justify-content: center;
        gap: 20px;
        margin-bottom: 20px;
      }

      .social-links a {
        color: white;
        text-decoration: none;
        font-size: 24px;
        transition: transform 0.3s;
      }

      .social-links a:hover {
        transform: translateY(-5px);
      }

      @media (max-width: 768px) {
        .hero h1 {
          font-size: 36px;
        }

        .nav-links {
          gap: 15px;
        }

        section {
          padding: 40px 20px;
        }
      }
    </style>
  </head>
  <body>
    <header>
      <nav>
        <div class="logo">Portfolio</div>
        <ul class="nav-links">
          <li><a href="#about">About</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>

    <div class="hero">
      <div class="container">
        <h1>Hi, I'm Ricardo Bautista-Zapata</h1>
        <p>Full Stack Developer, Creative Problem Solver, Software Developer</p>
        <a href="#projects" class="cta-button">View My Work</a>
      </div>
    </div>

    <div class="container">
      <section id="about">
        <h2>About Me</h2>
        <div class="about-content">
          <p>
            I am a freshman at the Lawrence Technological University in
            Southfield and I am also establishing the foundation of my future
            career in the IT world.I just graduated high school at the
            International Technology Academy in Pontiac Michigan where I sparked
            an interest in technology, problem-solving, and innovation. I am
            also willing to develop myself, learn through practical work, and
            find a job that would allow me to contribute to the ever-changing
            information technology world.
          </p>
        </div>
      </section>

      <section id="skills">
        <h2>My Skills</h2>
        <div class="skills-grid">
          <div class="skill-card">
            <h3>Skillset</h3>
            <p>HTML/CSS, AI-Generative, Java, JavaScript, Python</p>
            <div class="skill-bar">
              <div class="skill-progress" style="width: 100%"></div>
            </div>
          </div>
          <div class="skill-card">
            <h3>IDEs</h3>
            <p>Eclipse, Aptana Studio, Codesandbox.io</p>
            <div class="skill-bar">
              <div class="skill-progress" style="width: 100%"></div>
            </div>
          </div>
          <div class="skill-card">
            <h3>Languages</h3>
            <p>English, Spanish</p>
            <div class="skill-bar">
              <div class="skill-progress" style="width: 100%"></div>
            </div>
          </div>
          <div class="skill-card">
            <h3>Tools & Workflow</h3>
            <p>Github, Replit, CI/CD</p>
            <div class="skill-bar">
              <div class="skill-progress" style="width: 100%"></div>
            </div>
          </div>
        </div>
      </section>

      <section id="projects">
        <h2>Featured Projects</h2>
        <div class="projects-grid">
          <div class="project-card">
            <div class="project-image">🚀</div>
            <div class="project-content">
              <h3>Mood Detector</h3>
              <p>
                This project uses a Teachable Machine (TM) to recongize patterns
                and determine the mood of the consumer using facial expressions.
              </p>
              <div class="project-tags">
                <span class="tag">P5.js</span>
                <span class="tag">TM</span>
              </div>
              <a
                href="https://editor.p5js.org/Rbautista_zapata/full/NpTV8cqr1"
                target="_blank"
                class="project-link"
                >View Project →</a
              >
            </div>
          </div>
          <div class="project-card">
            <div class="project-image">📱</div>
            <div class="project-content">
              <h3>Get to work</h3>
              <p>The description once you finish.</p>
              <div class="project-tags">
                <span class="tag">code complier</span>
                <span class="tag">Source</span>
                <span class="tag">Redux</span>
              </div>
              <a
                href="https://your-project-link.com"
                target="_blank"
                class="project-link"
                >View Project →</a
              >
            </div>
          </div>
          <div class="project-card">
            <div class="project-image">💼</div>
            <div class="project-content">
              <h3>Get to work</h3>
              <p>The description once you finish.</p>
              <div class="project-tags">
                <span class="tag">HTML</span>
                <span class="tag">CSS</span>
                <span class="tag">JavaScript</span>
              </div>
              <a
                href="https://your-project-link.com"
                target="_blank"
                class="project-link"
                >View Project →</a
              >
            </div>
          </div>
        </div>
      </section>

      <section id="contact">
        <h2>Contact Information</h2>
        <div class="contact-content">
          <div class="contact-info-grid">
            <div class="contact-card">
              <div class="contact-card-icon">📧</div>
              <h3>Email</h3>
              <p>
                <a href="mailto:bautistazapata.ricardo@gmail.com"
                  >bautistazapata.ricardo@gmail.com</a
                >
              </p>
            </div>
            <div class="contact-card">
              <div class="contact-card-icon">📱</div>
              <h3>Phone</h3>
              <p><a href="tel:+2489808129">+1 (248) 980-8129</a></p>
            </div>
            <div class="contact-card">
              <div class="contact-card-icon">📍</div>
              <h3>Location</h3>
              <p>Pontiac, MI, USA</p>
            </div>
            <div class="contact-card">
              <div class="contact-card-icon">💼</div>
              <h3>LinkedIn</h3>
              <p>
                <a
                  href="https://www.linkedin.com/public-profile/settings?trk=d_flagship3_profile_self_view_public_profile"
                  target="_blank"
                  >My LinkedIn Profile</a
                >
              </p>
            </div>
          </div>
        </div>
      </section>
    </div>

    <footer>
      <div class="social-links">
        <a href="#" title="GitHub">🔗</a>
        <a href="#" title="LinkedIn">💼</a>
        <a href="#" title="Twitter">🐦</a>
        <a href="#" title="Email">📧</a>
      </div>
      <p>&copy; 2025 Bautista. All rights reserved.</p>
    </footer>

    <script>
      // Smooth scrolling for navigation links
      document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
        anchor.addEventListener("click", function (e) {
          e.preventDefault();
          const target = document.querySelector(this.getAttribute("href"));
          if (target) {
            target.scrollIntoView({ behavior: "smooth", block: "start" });
          }
        });
      });

      // Animate skill bars on scroll
      const observerOptions = {
        threshold: 0.5,
      };

      const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            const progressBars =
              entry.target.querySelectorAll(".skill-progress");
            progressBars.forEach((bar) => {
              const width = bar.style.width;
              bar.style.width = "0%";
              setTimeout(() => {
                bar.style.width = width;
              }, 100);
            });
          }
        });
      }, observerOptions);

      const skillsSection = document.querySelector("#skills");
      if (skillsSection) {
        observer.observe(skillsSection);
      }
    </script>
  </body>
</html>
