<script lang="ts">
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
  <div class="middle">Suryansh maurya</div>
  <div class="right">
    <a href="/resume.pdf" download>Download PDF</a>

    <button class="theme-btn" on:click={toggleTheme}>
      {theme === "dark" ? "🌙 Dark" : "☀️ Light"}
    </button>
  </div>
</header>

<style>
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
  z-index: 999;

  box-sizing: border-box;
}

.right {
  display: flex;
  align-items: center;
  gap: 1rem;           /* keeps space even */
  flex-wrap: nowrap;   /* prevents wrapping */
  overflow: hidden;    /* prevents ugly overflow */
  max-width: 60%;      /* keeps it inside screen */
}

.left {
  flex-shrink: 0;      /* name won't get squished */
}

a {
  color: var(--text);
  text-decoration: none;
  white-space: nowrap; /* prevents line breaks */
}

.theme-btn {
  font-size: 1rem;
  padding: 0.3rem 0.6rem;
  background: none;
  border: 1px solid var(--muted);
  border-radius: 5px;
  cursor: pointer;
  color: var(--text);
  white-space: nowrap;
}

.middle {
    font-weight: 700;
    font-size: 2rem;
}

</style>
