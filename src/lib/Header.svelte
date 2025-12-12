<script lang="ts">
  import { Github, Linkedin, Mail } from "lucide-svelte";

  /* --------------------------------------------------------
     Theme Initialization + Toggle
  --------------------------------------------------------- */
  let theme = "dark";

  const toggleTheme = () => {
    theme = theme === "dark" ? "light" : "dark";
    document.documentElement.setAttribute("data-theme", theme);
    localStorage.setItem("theme", theme);
  };

  if (typeof window !== "undefined") {
    const saved = localStorage.getItem("theme");
    if (saved) {
      theme = saved;
      document.documentElement.setAttribute("data-theme", saved);
    }
  }
</script>

<header class="header">
  <div class="left">Resume</div>

  <div class="middle">Suryansh Maurya</div>

  <div class="right">

    <!-- 🔗 SOCIAL ICONS (Desktop only) -->
    <div class="socials-desktop">
      <a href="https://github.com/SuryanshMaurya" target="_blank">
        <Github size="20" />
      </a>

      <a href="https://in.linkedin.com/in/suryansh-maurya-cse" target="_blank">
        <Linkedin size="20" />
      </a>

      <a href="mailto:suryanshmaurya23@gmail.com.com">
        <Mail size="20" />
      </a>
    </div>

    <!-- Download Button -->
    <a class="pdf-link" href="/resume.pdf" download>
      <span class="pdf-text">Download PDF</span>
      <span class="pdf-icon">
        <svg 
          width="20" 
          height="20" 
          viewBox="0 0 24 24" 
          fill="currentColor"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path 
            d="M12 3v12m0 0l-4-4m4 4l4-4M5 19h14" 
            stroke="currentColor" 
            stroke-width="2" 
            stroke-linecap="round" 
            stroke-linejoin="round"
          />
        </svg>
      </span>
    </a>

    <!-- Theme Toggle Button -->
    <button class="theme-btn" on:click={toggleTheme}>
      <span class="icon">{theme === "dark" ? "🌙" : "☀️"}</span>
      <span class="label">{theme === "dark" ? "Dark" : "Light"}</span>
    </button>
  </div>
</header>

<style>
/* ==========================================================
   HEADER LAYOUT
   ========================================================== */
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;

  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 1rem 1.2rem;
  font-size: 1.1rem;

  background: var(--bg);
  border-bottom: 1px solid var(--muted);
  box-sizing: border-box;
  z-index: 999;
}

.left {
  font-weight: 600;
  flex-shrink: 0;
}

.middle {
  font-weight: 700;
  font-size: 2rem;
  text-align: center;
}

/* ==========================================================
   RIGHT SECTION
   ========================================================== */
.right {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  flex-shrink: 0;
}

/* ------------------------- */
/* SOCIAL ICONS (DESKTOP)   */
/* ------------------------- */
.socials-desktop {
  display: flex;
  gap: 0.6rem;
}

.socials-desktop a {
  width: 34px;
  height: 34px;

  border: 1px solid var(--muted);
  border-radius: 50%;

  display: flex;
  justify-content: center;
  align-items: center;

  color: var(--text);
  transition: 0.2s ease;
}

.socials-desktop a:hover {
  background: var(--muted);
  color: var(--bg);
}

/* ==========================================================
   BUTTONS — GLOBAL
   ========================================================== */
a {
  color: var(--text);
  text-decoration: none;
  white-space: nowrap;
}

/* Theme Toggle Button */
.theme-btn {
  font-size: 1.05rem;
  padding: 0.3rem 0.6rem;
  background: none;
  border: 1px solid var(--muted);
  border-radius: 6px;
  cursor: pointer;
  color: var(--text);
  white-space: nowrap;
}

/* PDF Button */
.pdf-link {
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;

  padding: 0.3rem 0.6rem;
  border: 1px solid var(--muted);
  border-radius: 6px;

  transition: background 0.2s ease, border-color 0.2s ease;
}

.pdf-link:hover {
  background: var(--muted);
  border-color: var(--text);
  color: white;
}
.pdf-link .pdf-icon svg {
  vertical-align: middle;
  margin-top: 1.5px;   /* This is the exact correction needed */
}

/* ==========================================================
   MOBILE — under 600px
   ========================================================== */
@media (max-width: 600px) {
  .socials-desktop {
    display: none;
  }

  .header {
    padding: 0.7rem 0.9rem;
  }

  .middle {
    font-size: 1.3rem;
  }

  .pdf-text {
    display: none;
  }

  .pdf-link {
    padding: 0.25rem 0.45rem;
  }

  .theme-btn .label {
    display: none;
  }
}

/* ==========================================================
   VERY SMALL PHONES — under 400px
   ========================================================== */
@media (max-width: 400px) {
  .left {
    display: none;
  }

  .middle {
    font-size: 1.25rem;
  }
}
</style>

