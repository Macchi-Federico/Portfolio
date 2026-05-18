<script>
  import { onMount } from 'svelte';
  let visible = $state(false);
  onMount(() => setTimeout(() => visible = true, 80));
</script>

<section id="hero" class:visible>
  <!-- decorative blobs -->
  <div class="blob blob-1" aria-hidden="true"></div>
  <div class="blob blob-2" aria-hidden="true"></div>
  <div class="blob blob-3" aria-hidden="true"></div>

  <div class="container hero-inner">
    <div class="badge">
      <span class="dot"></span>
      Portfolio · Esame di Maturità 2026
    </div>

    <h1>
      Portfolio<br />
      <em>Educazione Civica</em>
    </h1>



  </div>

  <!-- year jump cards -->
  <div class="container">
    <div class="year-cards">
      <a href="#year3" class="ycard ycard-3">
        <span class="ycard-num">3°</span>
        <span class="ycard-label">Anno · 2023/24</span>
        <span class="ycard-arrow">↓</span>
      </a>
      <a href="#year4" class="ycard ycard-4">
        <span class="ycard-num">4°</span>
        <span class="ycard-label">Anno · 2024/25</span>
        <span class="ycard-arrow">↓</span>
      </a>
      <a href="#year5" class="ycard ycard-5">
        <span class="ycard-num">5°</span>
        <span class="ycard-label">Anno · 2025/26</span>
        <span class="ycard-arrow">↓</span>
      </a>
    </div>
  </div>
</section>

<style>
  section {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-top: 120px;
    padding-bottom: 80px;
    position: relative;
    overflow: hidden;
    opacity: 0;
    transition: opacity .7s ease;
  }

  section.visible { opacity: 1; }

  /* blobs */
  .blob {
    position: absolute;
    border-radius: 50%;
    filter: blur(80px);
    pointer-events: none;
  }
  .blob-1 {
    width: 500px; height: 500px;
    top: -120px; right: -100px;
    background: radial-gradient(circle, #ede8ff 0%, transparent 70%);
  }
  .blob-2 {
    width: 360px; height: 360px;
    bottom: 100px; left: -80px;
    background: radial-gradient(circle, #fff0ea 0%, transparent 70%);
  }
  .blob-3 {
    width: 240px; height: 240px;
    top: 40%; left: 40%;
    background: radial-gradient(circle, #e4faf0 0%, transparent 70%);
  }

  .hero-inner {
    position: relative;
    z-index: 1;
    margin-bottom: 56px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 6px 14px;
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 99px;
    font-size: 0.78rem;
    font-family: var(--mono);
    color: var(--text-2);
    margin-bottom: 28px;
    box-shadow: var(--shadow-sm);
    animation: fadeUp .6s .1s both;
  }

  .dot {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--green);
    box-shadow: 0 0 0 3px var(--green-light);
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { box-shadow: 0 0 0 3px var(--green-light); }
    50%       { box-shadow: 0 0 0 6px var(--green-light); }
  }

  h1 {
    font-size: clamp(3rem, 8vw, 6rem);
    font-weight: 800;
    line-height: 1.05;
    letter-spacing: -0.04em;
    color: var(--text);
    margin-bottom: 24px;
    animation: fadeUp .6s .2s both;
  }

  h1 em {
    font-style: normal;
    background: linear-gradient(135deg, var(--violet) 0%, var(--orange) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  /* Year jump cards */
  .year-cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
    position: relative;
    z-index: 1;
    animation: fadeUp .6s .72s both;
  }

  .ycard {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 24px;
    border-radius: 16px;
    border: 1px solid var(--border);
    background: var(--bg-card);
    box-shadow: var(--shadow-sm);
    transition: transform .2s, box-shadow .2s;
    text-decoration: none;
  }

  .ycard:hover {
    transform: translateY(-4px);
    box-shadow: var(--shadow-md);
  }

  .ycard-num {
    font-size: 2rem;
    font-weight: 800;
    letter-spacing: -0.04em;
    line-height: 1;
  }

  .ycard-label {
    font-family: var(--mono);
    font-size: 0.72rem;
    color: var(--text-3);
    letter-spacing: 0.04em;
  }

  .ycard-arrow {
    font-size: 1.2rem;
    opacity: .4;
  }

  .ycard-3 .ycard-num { color: var(--violet); }
  .ycard-3 { border-top: 3px solid var(--violet); }

  .ycard-4 .ycard-num { color: var(--orange); }
  .ycard-4 { border-top: 3px solid var(--orange); }

  .ycard-5 .ycard-num { color: var(--green); }
  .ycard-5 { border-top: 3px solid var(--green); }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @media (max-width: 680px) {
    .year-cards { grid-template-columns: 1fr; }
  
  }
</style>