<!DOCTYPE html>
<html>
<head>
<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
    background: linear-gradient(135deg, #0a0a0a 0%, #0d0d1a 50%, #1a0a2e 100%);
    color: #e0e0e0;
    line-height: 1.6;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 20px;
  }
  
  /* Header Section */
  .hero {
    text-align: center;
    padding: 60px 20px;
    background: linear-gradient(135deg, rgba(106, 13, 173, 0.2) 0%, rgba(0, 0, 0, 0.8) 100%);
    border-radius: 30px;
    margin-bottom: 40px;
    border: 1px solid rgba(156, 39, 176, 0.3);
  }
  
  .hero h1 {
    font-size: 72px;
    background: linear-gradient(135deg, #ffffff 0%, #b388ff 50%, #7b1fa2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 15px;
  }
  
  .hero p {
    font-size: 20px;
    color: #b388ff;
    letter-spacing: 2px;
  }
  
  .badge-container {
    margin-top: 30px;
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  
  .badge {
    padding: 8px 20px;
    background: rgba(156, 39, 176, 0.2);
    border: 1px solid #9c27b0;
    border-radius: 50px;
    font-size: 14px;
    color: #ce93d8;
  }
  
  /* Card Grid */
  .card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 25px;
    margin-bottom: 40px;
  }
  
  .card {
    background: rgba(20, 20, 40, 0.6);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    padding: 25px;
    border: 1px solid rgba(156, 39, 176, 0.3);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 30px rgba(156, 39, 176, 0.2);
    border-color: #9c27b0;
  }
  
  .card h3 {
    color: #b388ff;
    font-size: 24px;
    margin-bottom: 15px;
    border-left: 3px solid #9c27b0;
    padding-left: 15px;
  }
  
  .card h4 {
    color: #ce93d8;
    font-size: 18px;
    margin: 15px 0 10px 0;
  }
  
  .tech-list {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 15px;
  }
  
  .tech-tag {
    background: rgba(156, 39, 176, 0.2);
    padding: 5px 12px;
    border-radius: 20px;
    font-size: 12px;
    color: #ce93d8;
    border: 1px solid rgba(156, 39, 176, 0.5);
  }
  
  /* Stats Section */
  .stats-section {
    background: rgba(20, 20, 40, 0.6);
    border-radius: 20px;
    padding: 30px;
    margin-bottom: 40px;
    text-align: center;
    border: 1px solid rgba(156, 39, 176, 0.3);
  }
  
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    margin-top: 20px;
  }
  
  .stat-card {
    background: rgba(0, 0, 0, 0.4);
    padding: 20px;
    border-radius: 15px;
  }
  
  .stat-number {
    font-size: 36px;
    font-weight: bold;
    color: #b388ff;
  }
  
  .stat-label {
    font-size: 14px;
    color: #aaa;
    margin-top: 5px;
  }
  
  /* Project Cards */
  .project-card {
    background: rgba(20, 20, 40, 0.6);
    border-radius: 20px;
    padding: 25px;
    margin-bottom: 20px;
    border-left: 4px solid #9c27b0;
    transition: all 0.3s ease;
  }
  
  .project-card:hover {
    background: rgba(30, 30, 60, 0.8);
  }
  
  .project-title {
    font-size: 22px;
    color: #b388ff;
    margin-bottom: 10px;
  }
  
  .project-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin: 15px 0;
  }
  
  .project-link {
    display: inline-block;
    margin-top: 15px;
    padding: 8px 20px;
    background: linear-gradient(135deg, #7b1fa2, #4a148c);
    color: white;
    text-decoration: none;
    border-radius: 25px;
    font-size: 14px;
    transition: opacity 0.3s;
  }
  
  .project-link:hover {
    opacity: 0.8;
  }
  
  /* Education Card */
  .education-card {
    background: linear-gradient(135deg, rgba(123, 31, 162, 0.2), rgba(0, 0, 0, 0.6));
    border-radius: 20px;
    padding: 30px;
    margin-bottom: 40px;
    border: 1px solid #9c27b0;
  }
  
  /* Footer */
  .footer {
    text-align: center;
    padding: 30px;
    border-top: 1px solid rgba(156, 39, 176, 0.3);
    margin-top: 40px;
  }
  
  .social-links {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-bottom: 20px;
  }
  
  .social-link {
    padding: 10px 25px;
    background: rgba(156, 39, 176, 0.2);
    border-radius: 30px;
    text-decoration: none;
    color: #ce93d8;
    transition: all 0.3s;
  }
  
  .social-link:hover {
    background: #9c27b0;
    color: white;
  }
  
  hr {
    border-color: rgba(156, 39, 176, 0.3);
    margin: 20px 0;
  }
  
  @media (max-width: 768px) {
    .hero h1 { font-size: 48px; }
    .stats-grid { grid-template-columns: 1fr; }
    .card-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<div class="container">

  <!-- Hero Section -->
  <div class="hero">
    <h1>K AKASH</h1>
    <p>Software Engineer | AI/ML | Full-Stack | IoT</p>
    <div class="badge-container">
      <div class="badge">🚀 Open for Collaborations</div>
      <div class="badge">💡 Building Intelligent Systems</div>
      <div class="badge">🌟 4+ Years Coding</div>
    </div>
  </div>

  <!-- About & Info Grid -->
  <div class="card-grid">
    <div class="card">
      <h3>✨ About Me</h3>
      <p><strong>📍 Location:</strong> Vellore, India</p>
      <p><strong>🎓 Education:</strong> Integrated M.Tech @ VIT</p>
      <p><strong>📊 CGPA:</strong> 9.24</p>
      <p><strong>📅 Graduation:</strong> July 2027</p>
      <p><strong>📧 Email:</strong> akash260704@gmail.com</p>
      <br/>
      <p><strong>🔨 Currently Building:</strong><br/>IoT-Based Predictive Water Contamination Detection System for Hydroponics</p>
    </div>
    
    <div class="card">
      <h3>🎯 Core Domains</h3>
      <div class="tech-list">
        <div class="tech-tag">Full-Stack Web Dev</div>
        <div class="tech-tag">AI & Machine Learning</div>
        <div class="tech-tag">Internet of Things (IoT)</div>
        <div class="tech-tag">Cloud-Based Systems</div>
        <div class="tech-tag">Android Development</div>
      </div>
      
      <h4>💡 Interests</h4>
      <div class="tech-list">
        <div class="tech-tag">Scalable Products</div>
        <div class="tech-tag">Intelligent Design</div>
        <div class="tech-tag">Embedded Systems</div>
        <div class="tech-tag">Research & Open Source</div>
      </div>
    </div>
    
    <div class="card">
      <h3>📚 Currently Learning</h3>
      <div class="tech-list">
        <div class="tech-tag">System Design</div>
        <div class="tech-tag">AWS Advanced</div>
        <div class="tech-tag">RAG Pipelines</div>
        <div class="tech-tag">Sensor Fusion</div>
      </div>
      <br/>
      <p>• Advanced system design patterns<br/>
      • Cloud-native development with AWS<br/>
      • RAG pipelines & LLM applications<br/>
      • Sensor fusion for embedded IoT</p>
    </div>
  </div>

  <!-- Tech Stack Section -->
  <div class="stats-section">
    <h3 style="color: #b388ff; font-size: 28px; margin-bottom: 20px;">🛠️ Tech Stack</h3>
    
    <h4 style="color: #ce93d8; margin: 20px 0 10px 0;">💻 Programming Languages</h4>
    <div class="tech-list" style="justify-content: center;">
      <div class="tech-tag">Java</div>
      <div class="tech-tag">Python</div>
      <div class="tech-tag">C</div>
      <div class="tech-tag">C++</div>
    </div>
    
    <h4 style="color: #ce93d8; margin: 20px 0 10px 0;">🌐 Web & Backend</h4>
    <div class="tech-list" style="justify-content: center;">
      <div class="tech-tag">React</div>
      <div class="tech-tag">FastAPI</div>
      <div class="tech-tag">REST APIs</div>
      <div class="tech-tag">SQLAlchemy</div>
    </div>
    
    <h4 style="color: #ce93d8; margin: 20px 0 10px 0;">🗄️ Databases</h4>
    <div class="tech-list" style="justify-content: center;">
      <div class="tech-tag">MySQL</div>
      <div class="tech-tag">PostgreSQL</div>
      <div class="tech-tag">Firebase</div>
    </div>
    
    <h4 style="color: #ce93d8; margin: 20px 0 10px 0;">🤖 AI/ML</h4>
    <div class="tech-list" style="justify-content: center;">
      <div class="tech-tag">TensorFlow</div>
      <div class="tech-tag">Scikit-learn</div>
      <div class="tech-tag">OpenCV</div>
      <div class="tech-tag">NLP</div>
    </div>
    
    <h4 style="color: #ce93d8; margin: 20px 0 10px 0;">☁️ Cloud & DevOps</h4>
    <div class="tech-list" style="justify-content: center;">
      <div class="tech-tag">AWS</div>
      <div class="tech-tag">Vercel</div>
      <div class="tech-tag">Docker</div>
      <div class="tech-tag">Git/GitHub</div>
    </div>
    
    <h4 style="color: #ce93d8; margin: 20px 0 10px 0;">📡 IoT & Embedded</h4>
    <div class="tech-list" style="justify-content: center;">
      <div class="tech-tag">ESP32</div>
      <div class="tech-tag">ESP8266</div>
      <div class="tech-tag">Arduino IDE</div>
    </div>
  </div>

  <!-- GitHub Stats -->
  <div class="stats-section">
    <h3 style="color: #b388ff; font-size: 28px; margin-bottom: 20px;">📊 GitHub Analytics</h3>
    
    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px;">
      <img src="https://github-readme-stats.vercel.app/api?username=Akash2027&show_icons=true&theme=radical&hide_border=true&bg_color=0a0a0a&title_color=b388ff&icon_color=b388ff&text_color=e0e0e0&border_radius=12" width="45%" />
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Akash2027&layout=compact&theme=radical&hide_border=true&bg_color=0a0a0a&title_color=b388ff&text_color=e0e0e0&border_radius=12" width="45%" />
    </div>
    
    <br/>
    
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=Akash2027&theme=dark&background=0a0a0a&stroke=b388ff&ring=b388ff&fire=b388ff&currStreakLabel=b388ff&hide_border=true&border_radius=12" width="60%" />
    
    <br/><br/>
    
    <img src="https://github-profile-trophy.vercel.app/?username=Akash2027&theme=algolia&no-frame=true&bg_color=0a0a0a&title_color=b388ff&column=7" width="100%" />
  </div>

  <!-- Featured Projects -->
  <div class="stats-section">
    <h3 style="color: #b388ff; font-size: 28px; margin-bottom: 20px;">🚀 Featured Projects</h3>
    
    <div class="project-card">
      <div class="project-title">🌾 AI Crop Disease Assistant</div>
      <p>AI-powered multilingual crop disease diagnosis using Retrieval-Augmented Generation with speech-to-text and translation capabilities.</p>
      <div class="project-tech">
        <div class="tech-tag">Python</div>
        <div class="tech-tag">RAG</div>
        <div class="tech-tag">Gemini API</div>
        <div class="tech-tag">NLP</div>
      </div>
      <a href="https://github.com/Akash2027/AI-crop-disease-advisor" class="project-link">🔗 View Repository</a>
    </div>
    
    <div class="project-card">
      <div class="project-title">📚 Software Engineering Archive</div>
      <p>Full-stack academic repository platform for 85+ Software Engineering courses with resource upload and intelligent search.</p>
      <div class="project-tech">
        <div class="tech-tag">React</div>
        <div class="tech-tag">FastAPI</div>
        <div class="tech-tag">PostgreSQL</div>
        <div class="tech-tag">Cloudinary</div>
      </div>
      <a href="https://github.com/Akash2027/software-engineering-archive" class="project-link">🔗 GitHub</a>
      <a href="https://software-engineering-archive.vercel.app/" class="project-link">🌐 Live Demo</a>
    </div>
    
    <div class="project-card">
      <div class="project-title">📡 Smart Library IoT System</div>
      <p>IoT-based smart library seat recommendation system with real-time occupancy detection and Android app integration.</p>
      <div class="project-tech">
        <div class="tech-tag">ESP32</div>
        <div class="tech-tag">Android</div>
        <div class="tech-tag">Firebase</div>
      </div>
      <p style="margin-top: 10px;">🏆 <strong style="color: #b388ff;">Best Paper Award @ IConSCEPT 2025</strong> | IEEE Published</p>
      <a href="https://github.com/Akash2027/Smart-Library-Android-App" class="project-link">🔗 View Repository</a>
    </div>
    
    <div class="project-card">
      <div class="project-title">🔬 IoT Water Contamination System</div>
      <p>Predictive water contamination detection system for hydroponics with multi-parameter quality monitoring and automated response.</p>
      <div class="project-tech">
        <div class="tech-tag">ESP32</div>
        <div class="tech-tag">TensorFlow</div>
        <div class="tech-tag">Sensor Fusion</div>
      </div>
      <div class="tech-tag" style="background: #f7b500; color: #000;">Status: In Development</div>
    </div>
  </div>

  <!-- Publications & Patent -->
  <div class="card-grid">
    <div class="card">
      <h3>📄 Publications</h3>
      <p><strong>Crime Prediction & Resource Allocation Framework</strong><br/>
      <em>A Real-Time Crime Prediction Framework Using ML and Geospatial Analysis</em><br/>
      📍 International Conference, NIT Puducherry (2026)</p>
      <hr/>
      <p><strong>IoT-Based Smart Library Seat Recommendation System</strong><br/>
      <em>IoT-Based Smart Library System with Android App</em><br/>
      📖 IEEE Published | 🏆 Best Paper Award @ IConSCEPT 2025</p>
    </div>
    
    <div class="card">
      <h3>🔏 Patent</h3>
      <p><strong>Indian Patent — Published 2026</strong></p>
      <p><em>A System for Non-Invasive Quantitative Assessment of Palmar Hyperhidrosis Using Computer Vision</em></p>
      <p>AI-based embedded system for automated pixel-level sweat segmentation and quantitative severity grading from iodine-starch palm images.</p>
      <div class="tech-list">
        <div class="tech-tag">Computer Vision</div>
        <div class="tech-tag">Embedded AI</div>
      </div>
    </div>
  </div>

  <!-- Certifications -->
  <div class="stats-section">
    <h3 style="color: #b388ff; font-size: 28px; margin-bottom: 20px;">🏆 Certifications & Achievements</h3>
    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px;">
      <div class="tech-tag">☁️ AWS Certified Cloud Practitioner</div>
      <div class="tech-tag">🏆 Best Paper Award @ IConSCEPT 2025</div>
      <div class="tech-tag">📡 IEEE Conference Publications</div>
      <div class="tech-tag">🔏 Indian Patent Published 2026</div>
      <div class="tech-tag">🌐 Active Open-Source Learner</div>
    </div>
  </div>

  <!-- Education -->
  <div class="education-card">
    <h3 style="color: #b388ff; font-size: 24px; margin-bottom: 15px;">🎓 Education</h3>
    <p style="font-size: 18px;"><strong>Integrated M.Tech in Software Engineering</strong></p>
    <p>Vellore Institute of Technology (VIT), Vellore, India</p>
    <p style="color: #b388ff;">📊 CGPA: 9.24 | 📅 Expected Graduation: July 2027</p>
    <hr/>
    <p><strong>Core Areas:</strong> OOP · DSA · Operating Systems · Computer Networks · DBMS · REST APIs · Software Architecture</p>
  </div>

  <!-- Connect -->
  <div class="footer">
    <div class="social-links">
      <a href="https://www.linkedin.com/in/akash-k-bb9a20274" class="social-link">🔗 LinkedIn</a>
      <a href="https://github.com/Akash2027" class="social-link">🐙 GitHub</a>
      <a href="mailto:akash260704@gmail.com" class="social-link">✉️ Email</a>
      <a href="https://software-engineering-archive.vercel.app/" class="social-link">🌐 Portfolio</a>
    </div>
    
    <img src="https://komarev.com/ghpvc/?username=Akash2027&label=Profile+Views&color=b388ff&style=for-the-badge" />
    
    <hr/>
    
    <p style="color: #888;">✨ Thanks for visiting! ✨</p>
  </div>

</div>

</body>
</html>
