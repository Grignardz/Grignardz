<svg viewBox="0 0 1180 610" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="display: block; margin: 0 auto; max-width: 100%;">
  <defs>
    <!-- Color Gradients -->
    <linearGradient id="accentGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#7C3AED;stop-opacity:1" />
      <stop offset="50%" style="stop-color:#22D3EE;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#10B981;stop-opacity:1" />
      <animate attributeName="x1" values="0%;100%;0%" dur="6s" repeatCount="indefinite" />
      <animate attributeName="y1" values="0%;100%;0%" dur="6s" repeatCount="indefinite" />
    </linearGradient>

    <linearGradient id="asciiGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#06B7D4;stop-opacity:1" />
      <stop offset="50%" style="stop-color:#7C3AED;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#06B7D4;stop-opacity:1" />
      <animate attributeName="x1" values="0%;100%;0%" dur="8s" repeatCount="indefinite" />
    </linearGradient>

    <radialGradient id="bgGlow1" cx="20%" cy="20%">
      <stop offset="0%" style="stop-color:#3B82F6;stop-opacity:0.15" />
      <stop offset="100%" style="stop-color:#030712;stop-opacity:0" />
    </radialGradient>

    <radialGradient id="bgGlow2" cx="80%" cy="80%">
      <stop offset="0%" style="stop-color:#7C3AED;stop-opacity:0.1" />
      <stop offset="100%" style="stop-color:#030712;stop-opacity:0" />
    </radialGradient>

    <!-- Filters -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur" />
      <feMerge>
        <feMergeNode in="coloredBlur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <filter id="textGlow">
      <feGaussianBlur stdDeviation="2" result="coloredBlur" />
      <feMerge>
        <feMergeNode in="coloredBlur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <filter id="blur">
      <feGaussianBlur stdDeviation="4" />
    </filter>

    <!-- Scanline Animation -->
    <linearGradient id="scanline" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:rgba(255,255,255,0.03);stop-opacity:1" />
      <stop offset="50%" style="stop-color:rgba(255,255,255,0.08);stop-opacity:1" />
      <stop offset="100%" style="stop-color:rgba(255,255,255,0.03);stop-opacity:1" />
      <animate attributeName="y1" values="0%;100%" dur="3s" repeatCount="indefinite" />
      <animate attributeName="y2" values="100%;200%" dur="3s" repeatCount="indefinite" />
    </linearGradient>
  </defs>

  <!-- Background -->
  <rect width="1180" height="610" fill="#030712" />
  
  <!-- Background Glows -->
  <circle cx="200" cy="150" r="300" fill="url(#bgGlow1)" />
  <circle cx="1000" cy="450" r="350" fill="url(#bgGlow2)" />

  <!-- Main Container with rounded corners -->
  <g>
    <!-- Outer glow -->
    <rect x="20" y="20" width="1140" height="570" rx="20" fill="none" stroke="url(#accentGrad)" stroke-width="2" opacity="0.3" filter="url(#glow)" />
    
    <!-- Inner panel -->
    <rect x="30" y="30" width="1120" height="550" rx="16" fill="#0F172A" stroke="rgba(255,255,255,0.08)" stroke-width="1" />

    <!-- Scanline overlay -->
    <rect x="30" y="30" width="1120" height="550" rx="16" fill="url(#scanline)" />

    <!-- LEFT SECTION: ASCII Portrait -->
    <g>
      <!-- ASCII Container -->
      <g opacity="0.95">
        <!-- Floating animation -->
        <animateTransform
          attributeName="transform"
          type="translate"
          values="0,0; 0,-8; 0,0"
          dur="4s"
          repeatCount="indefinite"
        />

        <!-- ASCII Art with gradient -->
        <text x="150" y="120" font-family="'Courier New', monospace" font-size="10" fill="url(#asciiGrad)" filter="url(#textGlow)" font-weight="bold" letter-spacing="2">
          <tspan x="150" dy="14">  ╔═══════════════╗</tspan>
          <tspan x="150" dy="14">  ║  LABHANSH     ║</tspan>
          <tspan x="150" dy="14">  ║               ║</tspan>
          <tspan x="150" dy="14">  ║  DEV & BUILD  ║</tspan>
          <tspan x="150" dy="14">  ║               ║</tspan>
          <tspan x="150" dy="14">  ╚═══════════════╝</tspan>
        </text>

        <!-- Typing cursor for ASCII -->
        <rect x="320" y="220" width="2" height="12" fill="#06B7D4">
          <animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite" />
        </rect>
      </g>

      <!-- ASCII Glow Background -->
      <circle cx="220" cy="180" r="120" fill="#06B7D4" opacity="0.05" filter="url(#blur)" />
    </g>

    <!-- RIGHT SECTION: Terminal Content -->
    <g>
      <!-- Greeting with typing animation -->
      <text x="450" y="80" font-family="'Segoe UI', sans-serif" font-size="28" font-weight="700" fill="#F8FAFC">
        <tspan>Hi</tspan>
        <tspan fill="#06B7D4" opacity="0">👋</tspan>
      </text>

      <text x="450" y="130" font-family="'Segoe UI', sans-serif" font-size="36" font-weight="700" fill="#F8FAFC">
        I'm
        <tspan fill="url(#accentGrad)" font-weight="700"> Labhansh</tspan>
      </text>

      <!-- Animated typing text -->
      <text x="450" y="180" font-family="'Courier New', monospace" font-size="16" fill="#22D3EE">
        <tspan>Full Stack Developer</tspan>
        <animate attributeName="opacity" values="0;1;1;0" dur="8s" repeatCount="indefinite" />
      </text>

      <text x="450" y="180" font-family="'Courier New', monospace" font-size="16" fill="#10B981">
        <tspan>AI/ML Enthusiast</tspan>
        <animate attributeName="opacity" values="0;0;0;1;1;0" dur="12s" repeatCount="indefinite" begin="4s" />
      </text>

      <text x="450" y="180" font-family="'Courier New', monospace" font-size="16" fill="#7C3AED">
        <tspan>Open Source Builder</tspan>
        <animate attributeName="opacity" values="0;0;0;0;0;1;1;0" dur="16s" repeatCount="indefinite" begin="8s" />
      </text>

      <!-- Typing cursor -->
      <rect x="720" y="163" width="2" height="16" fill="#06B7D4">
        <animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite" />
      </rect>

      <!-- Info Section with sequential reveal -->
      <g opacity="0">
        <animate attributeName="opacity" values="0;1" dur="0.8s" begin="3s" fill="freeze" />
        
        <text x="450" y="240" font-family="'Segoe UI', sans-serif" font-size="13" fill="#94A3B8">
          <tspan font-weight="600" fill="#F8FAFC">📍 Location:</tspan>
          <tspan fill="#94A3B8"> Ghaziabad, India</tspan>
        </text>

        <text x="450" y="270" font-family="'Segoe UI', sans-serif" font-size="13" fill="#94A3B8">
          <tspan font-weight="600" fill="#F8FAFC">🎓 Focus:</tspan>
          <tspan fill="#94A3B8"> DSA, AI/ML, Full-Stack</tspan>
        </text>

        <text x="450" y="300" font-family="'Segoe UI', sans-serif" font-size="13" fill="#94A3B8">
          <tspan font-weight="600" fill="#F8FAFC">💡 Passion:</tspan>
          <tspan fill="#94A3B8"> Building Practical Apps</tspan>
        </text>
      </g>

      <!-- Skills Pills -->
      <g opacity="0">
        <animate attributeName="opacity" values="0;1" dur="0.8s" begin="4s" fill="freeze" />

        <text x="450" y="350" font-family="'Segoe UI', sans-serif" font-size="12" font-weight="600" fill="#94A3B8">
          Tech Stack
        </text>

        <!-- Skill Pills with hover effect (visual only via animation) -->
        <g>
          <!-- Python -->
          <rect x="450" y="365" width="70" height="28" rx="14" fill="rgba(59, 130, 246, 0.15)" stroke="rgba(59, 130, 246, 0.4)" stroke-width="1.5">
            <animate attributeName="stroke" values="rgba(59, 130, 246, 0.4);rgba(59, 130, 246, 0.8);rgba(59, 130, 246, 0.4)" dur="3s" repeatCount="indefinite" />
          </rect>
          <text x="485" y="385" font-family="'Segoe UI', sans-serif" font-size="11" fill="#3B82F6" text-anchor="middle" font-weight="600">Python</text>

          <!-- C++ -->
          <rect x="535" y="365" width="60" height="28" rx="14" fill="rgba(139, 92, 246, 0.15)" stroke="rgba(139, 92, 246, 0.4)" stroke-width="1.5">
            <animate attributeName="stroke" values="rgba(139, 92, 246, 0.4);rgba(139, 92, 246, 0.8);rgba(139, 92, 246, 0.4)" dur="3.2s" repeatCount="indefinite" begin="0.3s" />
          </rect>
          <text x="565" y="385" font-family="'Segoe UI', sans-serif" font-size="11" fill="#8B5CF6" text-anchor="middle" font-weight="600">C++</text>

          <!-- JavaScript -->
          <rect x="610" y="365" width="90" height="28" rx="14" fill="rgba(34, 211, 238, 0.15)" stroke="rgba(34, 211, 238, 0.4)" stroke-width="1.5">
            <animate attributeName="stroke" values="rgba(34, 211, 238, 0.4);rgba(34, 211, 238, 0.8);rgba(34, 211, 238, 0.4)" dur="3.4s" repeatCount="indefinite" begin="0.6s" />
          </rect>
          <text x="655" y="385" font-family="'Segoe UI', sans-serif" font-size="11" fill="#22D3EE" text-anchor="middle" font-weight="600">JavaScript</text>

          <!-- React -->
          <rect x="715" y="365" width="65" height="28" rx="14" fill="rgba(6, 183, 212, 0.15)" stroke="rgba(6, 183, 212, 0.4)" stroke-width="1.5">
            <animate attributeName="stroke" values="rgba(6, 183, 212, 0.4);rgba(6, 183, 212, 0.8);rgba(6, 183, 212, 0.4)" dur="3.6s" repeatCount="indefinite" begin="0.9s" />
          </rect>
          <text x="747" y="385" font-family="'Segoe UI', sans-serif" font-size="11" fill="#06B7D4" text-anchor="middle" font-weight="600">React</text>

          <!-- Git -->
          <rect x="795" y="365" width="55" height="28" rx="14" fill="rgba(16, 185, 129, 0.15)" stroke="rgba(16, 185, 129, 0.4)" stroke-width="1.5">
            <animate attributeName="stroke" values="rgba(16, 185, 129, 0.4);rgba(16, 185, 129, 0.8);rgba(16, 185, 129, 0.4)" dur="3.8s" repeatCount="indefinite" begin="1.2s" />
          </rect>
          <text x="822" y="385" font-family="'Segoe UI', sans-serif" font-size="11" fill="#10B981" text-anchor="middle" font-weight="600">Git</text>
        </g>

        <!-- More Skills Row -->
        <g>
          <!-- ML/AI -->
          <rect x="450" y="410" width="75" height="28" rx="14" fill="rgba(249, 115, 22, 0.15)" stroke="rgba(249, 115, 22, 0.4)" stroke-width="1.5">
            <animate attributeName="stroke" values="rgba(249, 115, 22, 0.4);rgba(249, 115, 22, 0.8);rgba(249, 115, 22, 0.4)" dur="4s" repeatCount="indefinite" begin="1.5s" />
          </rect>
          <text x="487" y="430" font-family="'Segoe UI', sans-serif" font-size="11" fill="#F97316" text-anchor="middle" font-weight="600">ML/AI</text>

          <!-- Next.js -->
          <rect x="540" y="410" width="70" height="28" rx="14" fill="rgba(100, 116, 139, 0.15)" stroke="rgba(100, 116, 139, 0.4)" stroke-width="1.5">
            <animate attributeName="stroke" values="rgba(100, 116, 139, 0.4);rgba(100, 116, 139, 0.8);rgba(100, 116, 139, 0.4)" dur="4.2s" repeatCount="indefinite" begin="1.8s" />
          </rect>
          <text x="575" y="430" font-family="'Segoe UI', sans-serif" font-size="11" fill="#64748B" text-anchor="middle" font-weight="600">Next.js</text>

          <!-- MongoDB -->
          <rect x="625" y="410" width="80" height="28" rx="14" fill="rgba(76, 175, 80, 0.15)" stroke="rgba(76, 175, 80, 0.4)" stroke-width="1.5">
            <animate attributeName="stroke" values="rgba(76, 175, 80, 0.4);rgba(76, 175, 80, 0.8);rgba(76, 175, 80, 0.4)" dur="4.4s" repeatCount="indefinite" begin="2.1s" />
          </rect>
          <text x="665" y="430" font-family="'Segoe UI', sans-serif" font-size="11" fill="#4CAF50" text-anchor="middle" font-weight="600">MongoDB</text>

          <!-- Firebase -->
          <rect x="720" y="410" width="75" height="28" rx="14" fill="rgba(251, 146, 60, 0.15)" stroke="rgba(251, 146, 60, 0.4)" stroke-width="1.5">
            <animate attributeName="stroke" values="rgba(251, 146, 60, 0.4);rgba(251, 146, 60, 0.8);rgba(251, 146, 60, 0.4)" dur="4.6s" repeatCount="indefinite" begin="2.4s" />
          </rect>
          <text x="757" y="430" font-family="'Segoe UI', sans-serif" font-size="11" fill="#FB923C" text-anchor="middle" font-weight="600">Firebase</text>
        </g>
      </g>

      <!-- Social Links -->
      <g opacity="0">
        <animate attributeName="opacity" values="0;1" dur="0.8s" begin="5s" fill="freeze" />

        <text x="450" y="500" font-family="'Segoe UI', sans-serif" font-size="12" font-weight="600" fill="#94A3B8">
          Connect
        </text>

        <!-- GitHub -->
        <g>
          <circle cx="470" cy="530" r="18" fill="rgba(255,255,255,0.08)" stroke="rgba(255,255,255,0.15)" stroke-width="1.5">
            <animate attributeName="r" values="18;22;18" dur="2s" repeatCount="indefinite" />
            <animate attributeName="stroke-width" values="1.5;2.5;1.5" dur="2s" repeatCount="indefinite" />
          </circle>
          <text x="470" y="536" font-family="Arial, sans-serif" font-size="12" fill="#F8FAFC" text-anchor="middle" font-weight="bold">🔗</text>
        </g>

        <!-- LinkedIn -->
        <g>
          <circle cx="510" cy="530" r="18" fill="rgba(59, 130, 246, 0.15)" stroke="rgba(59, 130, 246, 0.4)" stroke-width="1.5">
            <animate attributeName="r" values="18;22;18" dur="2s" repeatCount="indefinite" begin="0.3s" />
            <animate attributeName="stroke-width" values="1.5;2.5;1.5" dur="2s" repeatCount="indefinite" begin="0.3s" />
          </circle>
          <text x="510" y="536" font-family="Arial, sans-serif" font-size="12" fill="#3B82F6" text-anchor="middle" font-weight="bold">in</text>
        </g>

        <!-- Instagram -->
        <g>
          <circle cx="550" cy="530" r="18" fill="rgba(219, 39, 119, 0.15)" stroke="rgba(219, 39, 119, 0.4)" stroke-width="1.5">
            <animate attributeName="r" values="18;22;18" dur="2s" repeatCount="indefinite" begin="0.6s" />
            <animate attributeName="stroke-width" values="1.5;2.5;1.5" dur="2s" repeatCount="indefinite" begin="0.6s" />
          </circle>
          <text x="550" y="536" font-family="Arial, sans-serif" font-size="12" fill="#DB2777" text-anchor="middle" font-weight="bold">📷</text>
        </g>

        <!-- Mail -->
        <g>
          <circle cx="590" cy="530" r="18" fill="rgba(249, 115, 22, 0.15)" stroke="rgba(249, 115, 22, 0.4)" stroke-width="1.5">
            <animate attributeName="r" values="18;22;18" dur="2s" repeatCount="indefinite" begin="0.9s" />
            <animate attributeName="stroke-width" values="1.5;2.5;1.5" dur="2s" repeatCount="indefinite" begin="0.9s" />
          </circle>
          <text x="590" y="536" font-family="Arial, sans-serif" font-size="12" fill="#F97316" text-anchor="middle" font-weight="bold">✉</text>
        </g>
      </g>

      <!-- CTA Text -->
      <text x="450" y="570" font-family="'Segoe UI', sans-serif" font-size="12" fill="#94A3B8" opacity="0">
        <tspan font-weight="500">Let's build something amazing together</tspan>
        <animate attributeName="opacity" values="0;0.8" dur="0.8s" begin="6s" fill="freeze" />
      </text>
    </g>
  </g>

  <!-- Floating particles -->
  <g opacity="0.3">
    <circle cx="100" cy="100" r="2" fill="#06B7D4">
      <animate attributeName="cy" values="100;50;100" dur="6s" repeatCount="indefinite" />
      <animate attributeName="opacity" values="0;0.5;0" dur="6s" repeatCount="indefinite" />
    </circle>
    <circle cx="1050" cy="500" r="1.5" fill="#7C3AED">
      <animate attributeName="cy" values="500;450;500" dur="5s" repeatCount="indefinite" />
      <animate attributeName="opacity" values="0;0.4;0" dur="5s" repeatCount="indefinite" />
    </circle>
    <circle cx="300" cy="550" r="1" fill="#10B981">
      <animate attributeName="cy" values="550;480;550" dur="7s" repeatCount="indefinite" />
      <animate attributeName="opacity" values="0;0.3;0" dur="7s" repeatCount="indefinite" />
    </circle>
  </g>
</svg>

---

## 🚀 About Me

Hey ppl! myself **Labhansh Vashisht**

First-year undergrad passionate about coding, problem-solving, and building practical projects.

I work with Python and have explored AI/ML libraries, data science, Streamlit, C++, and R. I also love learning about cybersecurity fundamentals and enjoy vibe coding while experimenting with new ideas and technologies.

---

## 🌐 Socials

[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com)

---

## 💻 Tech Stack

### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

### AI / Data Science
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)

### Development Tools
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

---

## 🎯 Interests

- 🤖 Artificial Intelligence & Machine Learning
- 🔐 Cybersecurity
- 📊 Data Science & Analytics
- 🏗️ Software Engineering
- 🔓 Open Source Development
- 🧩 Problem Solving
- 🛠️ Building Practical Applications

---

## 📈 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Grignardz&show_icons=true&theme=dark&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Grignardz&layout=compact&theme=dark&hide_border=true)

---

## 🎓 Currently Learning

- Artificial Intelligence & Machine Learning
- Cybersecurity
- Full-Stack Development
- Data Structures & Algorithms
- Cloud Computing

---

## 🔥 Open To

- 🤝 Open Source Contributions
- 💼 Software Development Projects
- 🤖 AI/ML Collaborations
- 🏆 Hackathons
- 🔬 Research Opportunities

---

## 📫 Connect With Me

Feel free to reach out if you'd like to collaborate, discuss technology, or work on interesting projects.

- 📧 **Email:** labhanshvashisht2103@gmail.com
- 💼 **LinkedIn:** [linkedin.com/in/labhansh](https://linkedin.com/in/vashishtlabhansh)
- 🐙 **GitHub:** [github.com/labhansh](https://github.com/Grignardz)
- 📸 **Instagram:** [@labhsolutely](https://instagram.com/labhsolutely)

---

<div align="center">
  
  **Let's build something amazing together! 🚀**
  
  <sub>Made with ❤️ by Labhansh Vashisht</sub>
  
</div>
