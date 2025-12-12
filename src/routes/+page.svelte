<script lang="ts">
  import { fade } from "svelte/transition";
  import { Github, Linkedin, Mail } from "lucide-svelte";

  let showFloating = false;

  // Track scroll position
  if (typeof window !== "undefined") {
    window.addEventListener("scroll", () => {
      showFloating = window.scrollY > 250; // adjust threshold
    });
  }
</script>


<!-- MOBILE SOCIAL ICONS -->
<div class="socials-mobile">
  <a href="https://github.com/SuryanshMaurya" target="_blank">
    <Github size="20" />
  </a>

  <a href="https://in.linkedin.com/in/suryansh-maurya-cse" target="_blank">
    <Linkedin size="20" />
  </a>

  <a href="mailto:suryanshmaurya23@gmail.com">
    <Mail size="20" />
  </a>
</div>

{#if showFloating}
  <div class="socials-floating">
    <a href="https://github.com/YOUR_USERNAME">
      <Github size="18" />
    </a>

    <a href="https://linkedin.com/in/YOUR_USERNAME">
      <Linkedin size="18" />
    </a>

    <a href="mailto:your@email.com">
      <Mail size="18" />
    </a>
  </div>
{/if}





<!-- PROFILE -->
<section class="section" transition:fade>
  <!-- <h1 class="title">Suryansh Maurya</h1> -->
  <p class="subtitle">Gen AI Engineer • IITian • Love Technology</p>
  <p class="intro">
    Computer Science Engineer with an expertise in Artificial Intelligence and Machine Learning.<br>
    I build AI systems, Models, Latest Tech and Tools.
  </p>
</section>


<!-- EDUCATION -->
<section class="section" transition:fade>
  <h2>Education</h2>

  <p class="degree">
    Bachelor of Technology in Computer Science Engineering
  </p>

  <div class="edu-row">
    <span class="school"><u>Indian Institute of Technology Goa</u></span>
    <span class="year">2019–2023</span>
  </div>
</section>


<!-- EXPERIENCE -->
<section class="section" transition:fade>
  <h2>Experience</h2>
  
  <div class="exp-row">
    <h4>AI Full Stack Developer | DNS Group, Delhi</h4>
    <span class="date">Aug’25–Present</span>
  </div>
  <ul>
    <li>Designed and implemented scalable data pipelines to support the development and deployment of the company's AI Agent ecosystem.</li>
    <li>Contributed to the AI Agent and central engine architecture, ensuring optimized data flow modularity, and reliability.</li>
    <li>Built forecasting and predictive analytics tools using LSTM, Temporal Fusion Transformers (TFT), Prophet, and custom in-house algorithms to deliver accurate business insights.</li>
    <li>Developed a local on-device AI chatbot optimized for low resource hardware using lightweight models such as phi-3 and quantized transformers varients.</li>
  </ul>

  <div class="exp-row">
    <h4>Data Analyst Intern | EXL Service, Chennai</h4>
    <span class="date">June'22 - Nov'22</span>
  </div>
  <ul>
    <li>Aggregated and integrated data from multiple sources to build efficient data pipelines, improving data workflow efficiency by 30%.</li>
    <li>Automated data reporting processes using Python scripts, reducing report generation time by 40%.</li>
    <li>Validated SQL queries to ensure 100% accuracy and consistency of data.</li>
    <li>Created advanced data visualizations including pivot tables and graphs to support decision-making.</li>
  </ul>

</section>


<!-- PROJECTS -->
<section class="section" transition:fade>
  <h2>Projects</h2>

  <div class="exp-row">
    <h4>
    Doc Inspec Software - RAG-based AI Application
    <a href="https://github.com/AsaeDawn/PainImage" target="_blank">
      - [CODE]
    </a>
    </h4>

    <span class="date">2025</span>
  </div>
  <ul>
    <li>Developed an AI system using RAG methodology to process uploaded documents and provide context-aware answers.</li>
    <li>Integrated transformer models with vector search engines (FAISS) and Hugging Face libraries for efficient information retrieval.</li>
    <li>Enabled real-time document parsing and dynamic Q&A functionalities within AI  workflows.</li>
  </ul>

  <div class="exp-row">
    <h4>
    PainImage - Offline AI Image Editor
    <a href="https://github.com/AsaeDawn/PainImage" target="_blank">
      - [CODE]
    </a>
    </h4>
    <span class="date">Work in Progress</span>
</div>
<ul>
    <li>Developed a cross-platform desktop image editor for Windows, macOS, and Linux.</li>
    <li>Designed a custom PySide6 interface with a Python-based backend architecture.</li>
    <li>Built a streamlined, intuitive UI offering essential editing tools and a low-friction installation experience.</li>
    <li>Integrated offline image-processing algorithms and AI modules, including upscaling, text extraction, and enhancement utilities.</li>
    <li>Implemented secure, fully local inference pipelines to ensure user privacy and reliable performance without cloud dependency.</li>
    <li>Optimized model handling, caching, and memory usage to support smooth operation on both high-end and low-spec systems.</li>
    <li>Engineered a modular, plugin-ready system enabling straightforward extension with new tools, filters, and AI capabilities.</li>
    <li>Added automated update handling and a fault-tolerant saving mechanism to improve stability and prevent data loss.</li>
</ul>




</section>


<!-- TECH STACK -->
<section class="section" transition:fade>
  <h2>Tech Stack</h2>

  <div class="tech-grid">

    <div class="tech-category">
      <h3>Languages</h3>
      <p>Python • TypeScript • JavaScript • SQL</p>
    </div>

    <div class="tech-category">
      <h3>Frameworks & Libraries</h3>
      <p>SvelteKit • React • Node.js • FastAPI • PyTorch • TensorFlow • Scikit-learn • Hugging Face Transformers • LangChain</p>
    </div>

    <div class="tech-category">
      <h3>AI & ML</h3>
      <p>LSTM • Prophet • RAG • Vector Databases (FAISS) • Local LLMs • Model Quantization • Computer Vision (OpenCV) • Embedding Models</p>
    </div>

    <div class="tech-category">
      <h3>Data & Backend</h3>
      <p>PostgreSQL • Redis • Pandas • NumPy • REST APIs • WebSockets • Microservices Architecture</p>
    </div>

    <div class="tech-category">
      <h3>DevOps & Tools</h3>
      <p>Docker • Git • CI/CD • Linux Systems • Containerization & Deployment</p>
    </div>

  </div>
</section>



<!-- THANK YOU -->
<section class="section center" transition:fade>
  <h2>Thank you for reading</h2>
  <p class="muted">Appreciate you scrolling this far.
    I wish you a very good day :)
  </p>
  <p class="muted"></p>
</section>


<style>
  /* .title {
    font-size: 3rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
  } */

  .subtitle {
    font-size: 1.2rem;
    opacity: 0.8;
    margin-bottom: 1rem;
  }

  .intro {
    max-width: 700px;
    line-height: 1.6;
    opacity: 0.85;
  }

  h2 {
    margin-bottom: 0.5rem;
  }

  ul {
    opacity: 0.85;
    line-height: 1.7;
  }

  .muted {
    color: var(--muted);
  }

.degree {
  margin-bottom: 0.2rem;
}

.edu-row {
  display: flex;
  align-items: center;
  width: 100%;
}

.school {
  font-weight: 600;
}

.year {
  margin-left: auto;
  opacity: 0.8;
  white-space: nowrap;
}

.exp-row {
  display: flex;
  align-items: center;
  width: 100%;
}

.exp-row h4 {
  margin: 0;
}

.date {
  margin-left: auto;
  white-space: nowrap;
  opacity: 0.8;
}

.exp-row h4 a {
  color: var(--text);       /* keep normal text color */
  text-decoration: none;    /* remove underline */
  font-style: italic;       /* make it italic */
}

.exp-row h4 a:hover {
  color: var(--accent);     /* optional hover color */
}
.tech-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.2rem 2rem;
  margin-top: 1rem;
}

.tech-category h3 {
  margin: 0 0 0.3rem 0;
  font-size: 1.1rem;
}

.tech-category p {
  margin: 0;
  opacity: 0.9;
  line-height: 1.5;
  font-size: 0.97rem;
}

/* Mobile layout */
@media (max-width: 600px) {
  .tech-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }

  .tech-category h3 {
    font-size: 1rem;
  }
}


/* MOBILE SOCIAL ICONS */
.socials-mobile {
  display: none;
}

@media (max-width: 600px) {
  .socials-mobile {
    display: flex;
    justify-content: center;
    gap: 1rem;

    margin-top: 1px; /* Just under fixed header */


    padding: 0.5rem 0;
  }

  .socials-mobile a {
    width: 42px;
    height: 42px;
    border: 1px solid var(--muted);
    border-radius: 50%;

    display: flex;
    justify-content: center;
    align-items: center;

    color: var(--text);
    transition: 0.2s ease;
  }

  .socials-mobile a:hover {
    background: var(--muted);
    color: var(--bg);
  }
}
/* FLOATING ICONS (mobile only) */
.socials-floating {
  position: fixed;
  right: 12px;
  bottom: 110px;

  display: flex;
  flex-direction: column;
  gap: 0.6rem;

  z-index: 999;

  /* Smooth fade */
  animation: fadeIn 0.3s ease forwards;
}

.socials-floating a {
  width: 28px;
  height: 28px;

  background: var(--bg);
  border: 1px solid var(--muted);
  border-radius: 50%;

  display: flex;
  justify-content: center;
  align-items: center;

  color: var(--text);
  box-shadow: 0 2px 6px rgba(0,0,0,0.3);
  transition: 0.2s ease;
}
.socials-floating a svg {
  width: 14px;
  height: 14px;
}

.socials-floating a:hover {
  background: var(--muted);
  color: var(--bg);
}

/* fade animation */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Only show floating icons below 600px */
@media (min-width: 600px) {
  .socials-floating {
    display: none;
  }
}


</style>
