<section id="portfolio-tabs">
  <div align="center">
  <h1>Hi, I'm Luca</h1>
  </div>
  <div align="center"><h3>A passionate Full Stack Developer from Belgium</h3></div>
  
  <h3>Skills</h3>

<div class="tab-panel" id="tech">
      <div class="tech-grid">
        <!-- Programming Languages -->
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="images/c-1.svg" alt="C" class="tech-logo">
          </div>
          <span class="tech-name">C</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/python-5.svg" alt="Python" class="tech-logo">
          </div>
          <span class="tech-name">Python</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/c--4.svg" alt="C#" class="tech-logo">
          </div>
          <span class="tech-name">C#</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/java-14.svg" alt="Java" class="tech-logo">
          </div>
          <span class="tech-name">Java</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
              <img src="/images/html-1.svg" alt="HTML" class="tech-logo">
          </div>
          <span class="tech-name">HTML</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
              <img src="/images/javascript-1.svg" alt="JavaScript" class="tech-logo">
          </div>
          <span class="tech-name">JavaScript</span>
        </div>
        <!-- Hardware/Embedded -->
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/stm32-logo.svg" alt="STM32" class="tech-logo">
          </div>
          <span class="tech-name">STM32</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/css-3.svg" alt="CSS" class="tech-logo">
          </div>
          <span class="tech-name">CSS</span>
        </div>
        <!-- Databases -->
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/postgresql-inc.svg" alt="PostgreSQL" class="tech-logo">
          </div>
          <span class="tech-name">PostgreSQL</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/postgresql-inc.svg" alt="SQL" class="tech-logo">
          </div>
          <span class="tech-name">SQL</span>
        </div>
        <!-- Frameworks & Tools -->
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/flask.svg" alt="Flask" class="tech-logo">
          </div>
          <span class="tech-name">Flask</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/jinja-logo.svg" alt="Jinja" class="tech-logo">
          </div>
          <span class="tech-name">Jinja</span>
        </div>
        <!-- Containerization -->
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/docker-4.svg" alt="Docker" class="tech-logo">
          </div>
          <span class="tech-name">Docker</span>
        </div>
        <!-- Version Control -->
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/git-icon.svg" alt="Git" class="tech-logo">
          </div>
          <span class="tech-name">Git</span>
        </div>
        <!-- Extra -->
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/wireshark.svg" alt="Wireshark" class="tech-logo">
          </div>
          <span class="tech-name">Wireshark</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/vmware-7.svg" alt="WMWare" class="tech-logo">
          </div>
          <span class="tech-name">VMWare</span>
        </div>
        <div class="tech-item">
          <div class="tech-logo-wrapper">
            <img src="/images/azure-2.svg" alt="Azure" class="tech-logo">
          </div>
          <span class="tech-name">Azure</span>
        </div>
      </div>
    </div>
  </div>

  <!-- Modal for expanded certificate view -->
  <div id="cert-modal" class="modal">
    <span class="close">&times;</span>
    <img class="modal-content" id="expanded-cert">
    <div id="caption"></div>
  </div>
</section>

<script>
  const buttons = document.querySelectorAll(".tab-btn");
  const panels = document.querySelectorAll(".tab-panel");
  
  buttons.forEach(btn => {
    btn.addEventListener("click", () => {
      buttons.forEach(b => b.classList.remove("active"));
      btn.classList.add("active");
      panels.forEach(p => p.classList.remove("active"));
      document.getElementById(btn.dataset.tab).classList.add("active");
    });
  });

  // Certificate modal functionality
  const modal = document.getElementById("cert-modal");
  const modalImg = document.getElementById("expanded-cert");
  const captionText = document.getElementById("caption");
  const thumbnails = document.querySelectorAll(".cert-thumbnail");
  const closeBtn = document.querySelector(".close");

  thumbnails.forEach(img => {
    img.addEventListener("click", function() {
      modal.style.display = "block";
      modalImg.src = this.src;
      captionText.innerHTML = this.alt;
    });
  });

  closeBtn.addEventListener("click", () => {
    modal.style.display = "none";
  });

  modal.addEventListener("click", (e) => {
    if (e.target === modal) {
      modal.style.display = "none";
    }
  });

  // Close modal with Escape key
  document.addEventListener("keydown", (e) => {
    if (e.key === "Escape" && modal.style.display === "block") {
      modal.style.display = "none";
    }
  });
</script>

<style>
  .tabs { display: flex; gap: 1rem; margin-bottom: 1.5rem; justify-content: center; }
  .tab-btn {
    padding: 0.6rem 1.2rem;
    border: 1px solid #ccc;
    border-radius: 8px;
    background: #f7f7f7;
    cursor: pointer;
  }
  .tab-btn.active {
    background: #2563eb;
    color: white;
    border-color: #2563eb;
  }
  .tab-content .tab-panel { display: none; gap: 1rem; }
  .tab-content .tab-panel.active { display: flex; flex-wrap: wrap; justify-content: center; }
  .card {
    flex: 1 1 250px;
    border: 1px solid #ccc;
    border-radius: 8px;
    padding: 1rem;
    margin: 0.5rem;
    background: #fafafa;
  }

  /* Certificate specific styles */
  .cert-card {
    flex: 1 1 250px;
    border: 1px solid #ccc;
    border-radius: 8px;
    padding: 1rem;
    margin: 0.5rem;
    background: #fafafa;
    text-align: center;
  }

  .cert-thumbnail {
    width: 100%;
    max-width: 300px;
    height: auto;
    border-radius: 6px;
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
    border: 1px solid #ddd;
  }

  .cert-thumbnail:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
  }

  .cert-card h4 {
    margin-top: 0.75rem;
    margin-bottom: 0.25rem;
  }

  /* Modal styles */
  .modal {
    display: none;
    position: fixed;
    z-index: 1000;
    padding-top: 50px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0,0,0,0.9);
  }

  .modal-content {
    margin: auto;
    display: block;
    max-width: 90%;
    max-height: 80vh;
    border-radius: 8px;
    animation: zoom 0.3s;
  }

  @keyframes zoom {
    from { transform: scale(0.8); }
    to { transform: scale(1); }
  }

  .close {
    position: absolute;
    top: 20px;
    right: 35px;
    color: #f1f1f1;
    font-size: 40px;
    font-weight: bold;
    cursor: pointer;
    transition: color 0.3s;
    z-index: 1001;
  }

  .close:hover,
  .close:focus {
    color: #bbb;
  }

  #caption {
    margin: auto;
    display: block;
    width: 80%;
    max-width: 700px;
    text-align: center;
    color: #ccc;
    padding: 10px 0;
    height: 50px;
  }

  /* Tech Stack Grid */
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
    gap: 2rem;
    width: 100%;
    padding: 1rem;
    justify-items: center;
  }

  .tech-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.75rem;
    text-align: center;
  }

  .tech-logo-wrapper {
    width: 80px;
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 1rem;
    background: #fafafa;
    border: 1px solid #e5e5e5;
    border-radius: 12px;
    transition: all 0.3s ease;
  }

  .tech-logo {
    max-width: 100%;
    max-height: 100%;
    object-fit: contain;
    transition: transform 0.3s ease;
  }

  .tech-logo-wrapper:hover {
    transform: scale(1.1);
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    border-color: #2563eb;
  }

  .tech-logo-wrapper:hover .tech-logo {
    transform: scale(1.05);
  }

  .tech-name {
    font-size: 0.9rem;
    font-weight: 500;
    color: #333;
  }

  /* Responsive adjustments */
  @media (max-width: 768px) {
    .tech-grid {
      grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
      gap: 1.5rem;
    }

    .tech-logo-wrapper {
      width: 70px;
      height: 70px;
    }
  }
</style>
